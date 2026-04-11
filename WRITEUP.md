# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
  VM cost can be efficient if you fully utilize the machine, but it’s easy to overpay when the VM is oversized or always-on for a small app, to get higher availability and scale benefits, you often need multiple instances, which increases cost and operational complexity. Whereas for App service cost is usually predictable because it maps to the App Service Plan you pick. Free/Shared have strict quotas; paid tiers avoid CPU/bandwidth quota stops, which plays important role for availability,
- *Choose the appropriate solution (VM or App Service) for deploying the app*
For CMS app, chose App service 
- *Justify your choice*
App Service is my choice for the CMS app, offers an SLA on paid tiers, and scales easily through plan and instance configuration without VM management overhead - requiring the additional operational effort of configuring, monitoring, and maintaining VM-level availability architectures

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
    Accept higher operational responsibility, including patching, monitoring, scaling, and designing availability. Scalability and availability would rely on VM sizing, load balancers, and multi‑VM architecture, rather than platform-managed scaling. The deployment workflow would be custom VM-based deployment and runtime management.
