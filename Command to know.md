# Command to know
Just some random commands that may help a lot..


## Linux basic stuff

Create aliases to be faster
```bash
alias ll='ls -l’
```

Curl:
- curl -k (allow insecure)
- curl -v (verbose)

grep OR / AND:

```bash
grep -E “this|orThis”
grep "error" logfile.txt | grep "database"
```

netstat:
list active network connections and listening ports

```bash
sudo netstat -tuln
```

See permission of a file (numeric) :

```bash
stat -c "%a"
```

Checksum

```bash
sha512sum file.txt
```


## Containers and Kubernetes

Podman:

```
podman build -t registry.killer.sh:5000/image-verify:v2 .
podman run registry.killer.sh:5000/image-verify:v2 # to test your changes
podman push registry.killer.sh:5000/image-verify:v2
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
command: ["echo"]      # executed command
args: ["Hello, World"] # arguments
```

```bash
command: ["/bin/sh", "-c"]
args: ["echo 'Nginx Started'; nginx -g 'daemon off;'"]
```


grep all image used in a namespace / in a deployment

```bash
k get pods -n nato -o yaml | grep "image: "
k get deploy xym -o yaml | grep "image: "
```

Get all field of a security context:

```bash
kubectl explain pod.spec.securityContext --recursive
```

Crictl:
interacting with Container Runtime Interface (CRI)-compatible container runtimes
```bash
crictl ps
crictl inspect <container id>
```