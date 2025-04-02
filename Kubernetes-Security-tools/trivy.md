# trivy

See available image localy

```bash
crictl images
```

Just scan an image to get CVE..

```bash
trivy image nginx:1.16.1-alpine
```

Only see critical and high CVE:

```bash
trivy image --severity HIGH,CRITICAL ginx:1.16.1-alpine
```

Genarate a CycloneDX SBOM image

```bash
trivy image --format cyclonedx --output /opt/course/18/sbom2.json registry.k8s.io/kube-controller-manager:v1.31.0
```

Scan an existing SBOM to know vulnerabilities

```bash
trivy sbom /opt/course/18/sbom_check.json
```