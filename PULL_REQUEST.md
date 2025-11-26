## Pull Request

### Title: Add Azure microservice communication samples (scaffold)

### Body:
This PR scaffolds Azure-specific microservice communication samples:

- Azure Service Bus: Queue and Topic/Subscription samples (producer + worker consumers)
- Azure Event Hubs: producer and EventProcessorClient consumer sample
- Azure Durable Functions: saga/orchestrator with compensation pattern
- Azure SignalR Service: hub + ServiceBus-to-SignalR bridge sample
- YARP BFF sample and docs
- Dockerfiles and docker-compose for local components (note: Service Bus & Event Hubs require real Azure resources)
- ARM/Bicep templates to provision Service Bus, Event Hubs, SignalR, Storage, and Key Vault
- GitHub Actions workflows: CI to build/test projects; commented deploy workflow for optional deployment

### Notes:
All projects target .NET 10. Applications use DefaultAzureCredential to read secrets from Key Vault. 
The PR requests reviewer "meas". Do NOT auto-merge when checks pass.

Required repository secrets and instructions are listed in the top-level README added in this branch. Please review the changes and let me know any adjustments you want.