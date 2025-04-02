# strace

See system calls..

..by attaching a process or multiple 

```bash
sudo strace -p 1234 -p 1235
```

..by running a command

```bash
sudo strace ls
```

I can execute it directly from outside the container

```bash
kubectl exec -it my-pod -c my-container -- strace ls
```

Example of utilization:

You look for a process that is doing a non authorized syscall in multiples containers

## Exercice to find out which process is accessing /dev/mem

strace available inside the pod ?

```bash
kubectl exec -it my-pod -c my-container -- strace ls
```