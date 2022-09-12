# K8s architecture concerns

### MicorVMs or Containers:
- Although this is bit early to comment, key concerns when choosing a VM or container based solution, following are the options:
  - [Google's gVisior](https://gvisor.dev/)
  - [Amazon Firecracker](https://firecracker-microvm.github.io/) - MicroVM manager
  - [Kata containers](https://katacontainers.io/) - Containers + MicroVMs + OCI + CRI-O - all supported
*Pros*:
  - Unlike containers which use ```cgroups``` to maintain the isolation, all containers still use same underlying host kernel, this leaves the security risk especially in multi-tenant environment.
  - MicroVMs are a great for running multi-tenant servless functions due to - higher security, lower resource footprints, faster startup time due. Mainly uses KVM (Linux Kernel Virtual machines) based architecture, keeps the footprints much lower. Firecracker enables AWS Lambda and Fargate, which is a testimony in itself.
  
### External DNS
  - Tooling
  - Issues on syncrhonization
  - 
### External Secrets/Valut Management/Key Management Solutions
  - Namespace level
  - Cluster level
  - 
### RBAC
 - Endpoint security
 - Data base
### Security
  - Transport security
  - RBAC for MS
  - Data authorization based on roles
  - Secrets Management
  - Certificate Management
### Traffic Design
  - Ingress & Outgress
  - EAST/WEST. NORTH/SOUTH patterns

### Storage

### Observability - Logging, Tracing, Metrics

### DevOPs
  - Deployment
  - Tracebility
  - 
### Storage
