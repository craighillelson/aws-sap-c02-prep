# AWS Solutions Architect Professional Notes

[AWS Certified Solutions Architect - Professional (SAP-C02) Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS-Certified-Solutions-Architect-Professional_Exam-Guide.pdf)

# Domains
- Domain 1: Design Solutions for Organizational Complexity (26% of
scored content)
- Domain 2: Design for New Solutions (29% of scored content)
- Domain 3: Continuous Improvement for Existing Solutions (25% of
scored content)
- Domain 4: Accelerate Workload Migration and Modernization (20% of
scored content)

# Security Groups vs NACLs

| Security Groups                                                                                                                   | NACLs                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| operate at the instance level and act as a virtual firewall, controlling inbound and outbound traffic to individual EC2 instances | operate at the subnet level and control inbound and outbound traffic for the entire subnet |
| default deny all policy                                                                                                           | default allow all policy                                                                   |
| allow rules only, stateful                                                                                                        | allow and deny rules, stateless                                                            |
| evaluate rules in order of precedence                                                                                             | evaluate rules in the order they are listed, from lowest to highest rule number            |
| automatically associated with an EC2 instance when it is launched                                                                 | automatically associated with a subnet when the subnet is created                          |
