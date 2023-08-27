

## MY AWESOME TERRAFORM MODULE TO PROVISION EKS CLUSTER WITH CUSTOM NETWORKING  ----->

# Sample usage:


module "gfakx-module" {  
  source = "github.com/gfakx/eks-module"  
  region        = "Enter your preffered region "  
  vpc_cidr      = "10.0.0.0/16"  
  dns_hostnames = "true"  
  dns_support   = "true"  
  pub_one_cidr  = "10.0.1.0/24"  
  pub_two_cidr  = "10.0.2.0/24"  
  priv_one_cidr = "10.0.3.0/24"  
  priv_two_cidr = "10.0.4.0/24"  
  az_one = "Enter your first  az"   
  az_two = "Enter your second az"  
  public_ip_launch = true  
  eks_version  = "1.26"  
  desired_size = 3  
  max_size     = 5  
  min_size     = 1  
  ami_type       = "AL2_x86_64"   
  instance_types = ["t3.small", "t3.medium", "t3.large"]  
  capacity_type  = "ON_DEMAND"  
  max_unavailable = 1  
  
}
