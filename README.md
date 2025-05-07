# devops
provider "aws" {
  region = "us-east-1"  # Change to your preferred region
}

resource "aws_instance" "my_vm" {
  ami           = "ami-0c02fb55956c7d316" # Amazon Linux 2 AMI (Free-tier eligible, as of May 2025)
  instance_type = "t2.micro"             # Free-tier instance type

  tags = {
    Name = "my-terraform-vm"
  }
}

