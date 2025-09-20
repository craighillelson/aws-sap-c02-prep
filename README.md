# AWS Solutions Architect Professional SAP-C02 Notes

[AWS Certified Solutions Architect - Professional (SAP-C02) Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS-Certified-Solutions-Architect-Professional_Exam-Guide.pdf)

# Domains
- **Domain 1**: Design Solutions for Organizational Complexity (26% of
scored content)
- **Domain 2**: Design for New Solutions (29% of scored content)
- **Domain 3**: Continuous Improvement for Existing Solutions (25% of
scored content)
- **Domain 4**: Accelerate Workload Migration and Modernization (20% of
scored content)

# Resources
- [Service Quotas](https://docs.aws.amazon.com/general/latest/gr/aws-service-information.html)
- [The Well Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)
# Permissions Boundaries
- do not grant permissions
- define maximum permissions for IAM roles

# Security Groups vs NACLs

| Security Groups                                                                                                                   | NACLs                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| operate at the instance level and act as a virtual firewall, controlling inbound and outbound traffic to individual EC2 instances | operate at the subnet level and control inbound and outbound traffic for the entire subnet |
| default deny all policy                                                                                                           | default allow all policy                                                                   |
| allow rules only, stateful                                                                                                        | allow and deny rules, stateless                                                            |
| evaluate rules in order of precedence                                                                                             | evaluate rules in the order they are listed, from lowest to highest rule number            |
| automatically associated with an EC2 instance when it is launched                                                                 | automatically associated with a subnet when the subnet is created                          |

# Services
- [Amazon CloudWatch Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html)
    
    **Metrics Retention**
    - data points with a period of less than 60 seconds are available for 3 hours (high-resolution custom metrics only)
    - data points with a period of 60 seconds (1 minute) are available for 15 days
    - data points with a period of 300 seconds (5 minutes) are available for 63 days
    - data points with a period of 3600 seconds (1 hour) are available for 455 days (15 months)

- [AWS DataSync](https://aws.amazon.com/datasync/)
- [AWS Elastic Disaster Recovery](https://aws.amazon.com/disaster-recovery/)
- [Amazon Forecast](https://aws.amazon.com/forecast/): ML based time series forecasting service
- [AWS Global Accelerator](https://aws.amazon.com/global-accelerator/)
- [Amazon Polly](https://aws.amazon.com/polly/)
- [Amazon Site to Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html)
- [Amazon Transcribe](https://aws.amazon.com/transcribe/)
- [Amazon Translate](https://aws.amazon.com/translate/): ML based language translation service

# Terms
- **ASN**: Autonomous System Number
- **BGP**: Border Gateway Protocol, used by some AWS services such as Direct Connect and Dynamic Site to Site VPNs, BGP uses the shortest path first (SPF) algorithm to determine the best path to route traffic
- **Deployment Strategies**
    - **Blue/Green Deployment**: two identical environments, one (blue) running the current application version and the other (green) running the new version. After testing, traffic is switched to the green environment.
    - **Canary Deployment**: new version is rolled out to a small subset of users first
    - **Rolling Deployment**: new version is gradually rolled out to all instances in the environment, replacing the old version incrementally
    - **Immutable Deployment**: new version is deployed to a new set of instances, and once verified, the old instances are terminated
    - **All-at-once Deployment**: new version is deployed to all instances simultaneously
- **Forward Web Proxy Server**: accepts requests from your private network and forwards them to the internet, acting as an intermediary for clients
- **IPSEC VPN**
    - group of protocols
    - sets up secure tunnels across insecure networks
    - provides authentication and encryption
    - peers exchange public keys and then use a combination of each other's public keys ad their private keys to produce a symmetrical IPSEC key