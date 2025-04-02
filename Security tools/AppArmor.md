# AppArmor

See loaded profile:

```bash
sudo apparmor_status
```

Install a profile:

```bash
sudo apparmor_parser -r ./profile
sudo apparmor_paser -h (for other operation)
```

Enforce a profile

```bash
sudo aa-enforce /path/to/bin
```

In the deployment:

```bash
spec:
      nodeSelector:                          # add
        security: apparmor                   # add
      containers:
      - image: nginx:1.27.1
        name: c1                             # change
        securityContext:                     # add
          appArmorProfile:                   # add
            type: Localhost                  # add
            localhostProfile: very-secure    # add
```