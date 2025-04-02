# Kubelet

Core component on each kubernetes node

https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-reconfigure/

## Option 1:

Update kubeletConfiguration:

```bash
kubectl edit cm -n kube-system kubelet-config
```

Refect kubelet change

```bash
kubeadm upgrade node phase kubelet-config
```

## Option 2:

Edit /var/lib/kubelet/config.yaml

Restart kubelet:

```bash
sudo systemctl daemon-reload
sudo systemctl restart kubelet
```

See how it is started:

```bash
sudo systemctl cat kubelet
```