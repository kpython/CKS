# kube-bench

run `kube-bench` against the controlplane or node components:

```bash
kube-bench run --targets=master > bench.txt
kube-bench run --targets=node > bench.txt
```

check a specific CIS numb:

```bash
kube-bench run --targets=master --check='1.3.2'
```