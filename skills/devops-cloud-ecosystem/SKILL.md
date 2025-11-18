---
name: devops-cloud-ecosystem
description: Master DevOps, cloud infrastructure, containerization, and Kubernetes. Use when deploying applications, building CI/CD pipelines, managing cloud resources, or implementing infrastructure automation.
---

# DevOps & Cloud Infrastructure Skill

## Quick Start

Build, deploy, and manage scalable cloud infrastructure with containerization and modern DevOps practices.

### Essential DevOps Stack

```yaml
# Docker Dockerfile example
FROM python:3.11-slim

WORKDIR /app

# Dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Application
COPY src/ .

EXPOSE 8000

# Health check
HEALTHCHECK --interval=30s --timeout=3s --start-period=40s --retries=3 \
  CMD curl -f http://localhost:8000/health || exit 1

CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:8000", "app:app"]
```

```yaml
# Kubernetes deployment example
apiVersion: apps/v1
kind: Deployment
metadata:
  name: app-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: app
        image: myapp:1.0.0
        ports:
        - containerPort: 8000
        resources:
          requests:
            cpu: 100m
            memory: 128Mi
          limits:
            cpu: 500m
            memory: 512Mi
        livenessProbe:
          httpGet:
            path: /health
            port: 8000
          initialDelaySeconds: 30
          periodSeconds: 10
```

## Learning Domains

### 🐳 **Containerization**

**Docker**
- Dockerfile best practices
- Multi-stage builds
- Image optimization
- Docker Compose for multi-container apps
- Container networking and volumes
- Docker registry and pushing images

**Container Security**
- Vulnerability scanning
- Rootless containers
- Container runtime options
- Image signing and verification

### ☸️ **Kubernetes**

**Core Concepts**
- Pods and containers
- Deployments and ReplicaSets
- Services and Ingress
- ConfigMaps and Secrets
- Persistent Volumes

**Advanced Topics**
- StatefulSets for stateful applications
- DaemonSets for node operations
- Jobs and CronJobs
- Custom Resource Definitions (CRDs)
- Operators and Helm charts

**Networking & Security**
- Network policies
- Service mesh (Istio, Linkerd)
- RBAC and Pod Security Policies
- Secrets management (Vault, sealed-secrets)
- Ingress controllers (Nginx, Traefik)

**Scaling & Performance**
- Horizontal Pod Autoscaling (HPA)
- Vertical Pod Autoscaling (VPA)
- Cluster autoscaling
- Resource limits and requests
- Performance optimization

### ☁️ **Cloud Platforms**

**AWS**
- EC2 and networking (VPC, subnets, security groups)
- RDS for managed databases
- S3 for object storage
- Lambda for serverless
- ECS/EKS for container orchestration
- CloudFront for CDN
- IAM for identity and access

**Azure**
- Azure Virtual Machines
- Azure Kubernetes Service (AKS)
- Azure Database services
- Azure App Service
- Azure DevOps for CI/CD
- Azure Monitor for observability

**Google Cloud**
- Compute Engine
- Google Kubernetes Engine (GKE)
- Cloud Run for serverless
- Cloud Storage
- BigQuery for analytics
- Cloud IAM and security

**Multi-Cloud & Hybrid**
- Cloud-agnostic deployments
- Terraform for multi-cloud
- Cost optimization across clouds

### 🏗️ **Infrastructure as Code**

**Terraform**
- HCL syntax and structure
- Modules and reusability
- State management
- Plan and apply workflow
- Remote state with Terraform Cloud

**Ansible**
- Playbooks and roles
- Configuration management
- Orchestration
- Error handling and retries

**CloudFormation / ARM Templates**
- Template syntax
- Stacks and change sets
- Parameters and outputs
- Custom resources

### 🔄 **CI/CD Pipelines**

**Build Automation**
- GitHub Actions workflows
- Jenkins pipelines
- GitLab CI
- CircleCI configuration
- Build optimization and caching

**Deployment Automation**
- Blue-green deployments
- Canary releases
- Rolling updates
- Automated rollbacks
- Feature flags

**Artifact Management**
- Container registries
- Artifact repositories (Artifactory, Nexus)
- Version tagging
- Scan for vulnerabilities

### 📊 **Monitoring & Observability**

**Logging**
- ELK Stack (Elasticsearch, Logstash, Kibana)
- Splunk and DataDog
- Structured logging
- Log aggregation and analysis

**Metrics**
- Prometheus for metrics collection
- Grafana for visualization
- Custom dashboards
- Alert rules and thresholds

**Tracing**
- Distributed tracing (Jaeger, Zipkin)
- OpenTelemetry
- Performance analysis
- Latency optimization

**Alerting**
- Alert configuration
- Escalation policies
- On-call management
- Incident response procedures

### 🔐 **Security & Compliance**

**Infrastructure Security**
- Firewalls and WAF (Web Application Firewalls)
- Network segmentation
- DDoS protection
- VPN and secure communication

**Secrets Management**
- HashiCorp Vault
- Cloud-native solutions (AWS Secrets Manager)
- Encryption at rest and in transit
- Key rotation policies

**Compliance & Governance**
- HIPAA, GDPR, SOC 2 compliance
- Audit logging and monitoring
- Backup and disaster recovery
- Incident response planning

## Skill Development Checklist

- [ ] Build and optimize Docker images
- [ ] Deploy multi-container application with Docker Compose
- [ ] Deploy application to Kubernetes cluster
- [ ] Setup CI/CD pipeline (push to deployment)
- [ ] Implement monitoring with Prometheus/Grafana
- [ ] Create infrastructure with Terraform
- [ ] Setup SSL/TLS certificates
- [ ] Implement disaster recovery
- [ ] Perform security audit

## Real-World Scenarios

**Production-Ready Kubernetes Setup**
```bash
# 1. Build and push Docker image
docker build -t myapp:1.0.0 .
docker tag myapp:1.0.0 registry.example.com/myapp:1.0.0
docker push registry.example.com/myapp:1.0.0

# 2. Create Kubernetes cluster (GKE example)
gcloud container clusters create production-cluster \
  --zone us-central1-a \
  --num-nodes 3 \
  --machine-type n1-standard-2

# 3. Deploy application
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml

# 4. Setup monitoring
kubectl apply -f prometheus.yaml
kubectl apply -f grafana.yaml

# 5. Configure autoscaling
kubectl autoscale deployment myapp --min=2 --max=10
```

## Practice Projects

1. **Containerize Legacy Application**
   - Create Dockerfile
   - Multi-environment configuration
   - Docker Compose for dependencies

2. **Kubernetes Cluster Setup**
   - Create production cluster
   - Deploy application
   - Setup networking and security

3. **CI/CD Pipeline**
   - GitHub Actions workflow
   - Test and build stages
   - Automated deployment
   - Rollback capabilities

4. **Monitoring Stack**
   - Prometheus metrics
   - Grafana dashboards
   - Alert rules
   - Log aggregation

## Resources

- **10+ DevOps & Cloud Roadmaps** - Docker, Kubernetes, AWS, Azure, GCP
- **120+ Content Modules** - Theory and hands-on practices
- **Platform Guides** - AWS, Azure, GCP specific resources
- **Infrastructure as Code** - Terraform, Ansible examples
- **CI/CD** - GitHub Actions, Jenkins, GitLab CI
- **Monitoring Tools** - Prometheus, Grafana, ELK Stack

## Assessment Criteria

You've mastered this skill when you can:

✓ Create optimized Docker images
✓ Deploy and manage Kubernetes clusters
✓ Design scalable cloud infrastructure
✓ Setup complete CI/CD pipelines
✓ Implement comprehensive monitoring
✓ Manage secrets and security
✓ Scale applications automatically
✓ Recover from disasters
✓ Optimize cloud costs
