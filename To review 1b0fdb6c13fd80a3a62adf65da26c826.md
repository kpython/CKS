# To review

- [x]  Configure service account in a pod without mounting token ? Purpose ?
- [x]  create a falco rule to see a pod accessing /dev/mem file
- [x]  Auditing → rules
- [x]  Inject SA in a deployment
- [x]  Use seccompProfile in securityContext.
- [x]  In a deployment → which securityContext belongs to what ? Pod or Container level
- [x]  Static analyze ? **(e.g. Kubesec, KubeLinter) ?**
- [x]  Create an alias for ll command !

```bash
alias ll='ls -l’
```

- [x]  TLS Ingress
- [x]  How restart kubelet
- [x]  How is kubelet started and how to start it with new parameter
- [x]  Remove a user from a specific group ?
- [x]  PSA - > how make sure a pod respect it
- [x]  ImagePolicyWebhook
- [x]  FileOrCreate vs File
- [x]  dev/mem….
- [x]  Static analyse → Docker file user (dbcouch)
    - [x]  See RUN adduser -D **myuser command in the file !**
- [x]  CiliumNetPol Layer 4
- [x]  deamon docker change something on the startup
- [x]  TLS Ssl redirect
- [x]  la vitesse encore et encore
- [x]  Possible de copier tout un block pour assurer le schedule en restricted PSA ?
- [x]  See how I can improve window handling and copy paste in this testing env
- [x]  ImagePolicyAdmission
    - [x]  why it didn’t work
    - [x]  Use existing volumes or volumes mounts
- [x]  To read: [https://arekborucki.medium.com/how-to-pass-cks-kubernetes-security-specialist-exam-part-7-c76c3cc5eafa](https://arekborucki.medium.com/how-to-pass-cks-kubernetes-security-specialist-exam-part-7-c76c3cc5eafa)
- [x]  kubelet config not same as kubelet cm… → **/var/lib/kubelet/config.yaml has precedence on config-map**
- [x]  Startup settings docker daemon
- [ ]  ImagePolicyWebhook once again did not work , vulnerable could be deployed
- [ ]  All securitycontext requirement for restricted need to be known by hearth
- [ ]  Security context on pod/container level.. During exam it didn’t work readOnlyRootFilesystem on container level, no idea why
- [ ]  Know cilium mutual auth by hearth
- [ ]  Docker deamon user need to be part of a group ??
- [ ]  Attention !! Ugprade is on a worker node
- [ ]  Add user -u 5235 -g couchdb couchdb

3 topic i need to review:

- Monitoring, Logging and Runtime Security
- Minimize Microservice Vulnerabilities
- Cluster Hardening

- 

Very important topics:

- Enable a custom Admission Controller for a Kubernetes cluster (ex: ImagePolicyWebhook).
- Configure an Audit Policy against your Kubernetes cluster.
- Load an AppArmor profile and apply it in a pod/deployment.
- Load a Seccomp profile and use it in the pod definition.
- Customize Falco logs and configurations.
- Scan images with Aqua Trivy.