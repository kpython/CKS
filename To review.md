# Must-know topics

# Check current curriculum
https://github.com/cncf/curriculum/blob/master/CKS_Curriculum%20v1.32.pdf

# To review before the exam
- [x] Inject service account token in a deployment.
- [x] Create/override a Falco rule (e.g., to monitor pods accessing sensitive files/directories).
- [x] Load an AppArmor profile and apply it in a pod/deployment.
- [x] Load a Seccomp profile and use it in the pod definition.
- [x] Auditing rules (https://kubernetes.io/docs/tasks/debug/debug-cluster/audit/).
- [x] Use `seccompProfile` in `securityContext`.
- [x] SecurityContexts in Pod vs Container.
- [x] Analyze static YAML files with KubeSec.
- [x] TLS Ingress and TLS SSL redirects.
- [x] How to restart kubelet.
- [x] How kubelet is started and how to start it with new parameters.
- [x] Linux: Remove a user from a specific group.
- [x] PSA -> How to ensure a pod respects it (securityContexts). All securityContext requirements for "restricted" need to be known by heart.
- [x] ImagePolicyWebhook.
- [x] Cilium Network Policies (see examples in the official documentation for Layer 3 and 4).
- [x] Startup settings for the Docker daemon.
- [x] Enable a custom Admission Controller for a Kubernetes cluster (e.g., ImagePolicyWebhook).
- [x] Kubelet config is not the same as kubelet ConfigMap → `/var/lib/kubelet/config.yaml` takes precedence over the ConfigMap.
- [x] Cilium mutual authentication.
- [x] Worker/Control plane node upgrade.