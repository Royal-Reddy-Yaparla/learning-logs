📅 Date: 2025-03-11 
🔹 Topic: Jenkin Connect to EKS Cluster
🛠️ Problem Faced: Error "
    aws eks update-kubeconfig --region us-east-1 --name <cluster_name>
    Unable to locate credentials. You can configure credentials by running "aws configure".
    "  
🧐 Debugging Steps: 
  1. Checked IAM permissions ✅  
💡 Solution:   
  1. Provide AWS credentials 
  2. Attach IAM role for EC2 instance
        - AmazonEKS_CNI_Policy
        - AmazonEKSWorkerNodePolicy
        - AmazonEC2ContainerRegistryReadOnly