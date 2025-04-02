# Command to remember

Curl:

- curl -k (allow insecure)
- curl -v (verbose)

Podman:

```
podman build -t registry.killer.sh:5000/image-verify:v2 .
podman run registry.killer.sh:5000/image-verify:v2 # to test your changes
podman push registry.killer.sh:5000/image-verify:v2
```

grep:

```bash
grep -E “this|orThis”
```

netstat:

```bash
sudo netstat -tuln
```

Check user RBAC

```bash
k auth can-i list secret --as gianna
```

How add a command into a pod:

```bash
command: ["sleep", "10"]
```

```bash
command: ["echo"]      # Commande exécutée
args: ["Hello, World"] # Arguments de la commande
```

```bash
command: ["/bin/sh", "-c"]
args: ["echo 'Nginx Started'; nginx -g 'daemon off;'"]
```

See permission of a file in numb:

```bash
stat -c "%a"
```

Checksum

```bash
sha512sum file.txt
```

grep all image used in a namespace / in a deployment

```bash
k get pods -n nato -o yaml | grep "image: "
k get deploy xym -o yaml | grep "image: "
```

Get all field of a secuity context:

```bash
kubectl explain pod.spec.securityContext --recursive
```

Crictl:

```bash
crictl ps
crictl inspect <container id>
```