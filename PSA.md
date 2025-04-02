# PSA

https://kubernetes.io/docs/concepts/security/pod-security-admission/

To enforce a PSA in a namespace:

```bash
apiVersion: v1
kind: Namespace
metadata:
  name: my-baseline-namespace
  labels:
    pod-security.kubernetes.io/enforce: baseline
```


Required Security Context for a Restricted PSA Namespace

 ```bash
apiVersion: v1
kind: Pod
metadata:
  name: restricted-pod
  namespace: restricted-psa
spec:
  securityContext:  
    runAsNonRoot: true  # Ensures the container does not run as root
    seccompProfile:
      type: RuntimeDefault  # Enforces syscall restrictions
  containers:
    - name: app
      image: nginx
      securityContext:
        allowPrivilegeEscalation: false  # Prevents privilege escalation
        capabilities:
          drop: ["ALL"]  # Drops all Linux capabilities
        privileged: false  # Ensures the container is not privileged
        readOnlyRootFilesystem: true  # Enforces a read-only filesystem
        runAsUser: 1000  # Specifies a non-root UID
        runAsGroup: 1000  # Specifies a non-root GID
```