# Falco

Configuration files:

location: /etc/falco/

Show falco output

```bash
falco
```

Speed up (because falco output is buffered)

```bash
falco -U/--unbuffered
```

See available field for output:

```bash
falco --list | grep user
```

Rules and the order how they loaded:

```
rules_files:
  - /etc/falco/falco_rules.yaml
  - /etc/falco/falco_rules.local.yaml
  - /etc/falco/rules.d
```

Validate:

```bash
falco --dry-run -c /etc/falco/falco.yaml
```

Restart falco

```bash
systemctl restart falco
```