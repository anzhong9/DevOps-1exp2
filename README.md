#hello world
Example readme file for my repo

# Define the provider and AWS region
provider "aws" {
  region = "us-east-1"  # Replace with your desired AWS region
}

# Create an EC2 instance
resource "aws_instance" "example_instance" {
  ami           = "ami-0c55b159cbfafe1f0"  # Replace with your desired AMI ID
  instance_type = "t2.micro"               # Replace with your desired instance type
  key_name      = "your-key-pair-name"     # Replace with your SSH key pair name

  tags = {
    Name = "ExampleInstance"
  }
}



answrer .tf
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}




answer lambda

def lambda_handler(event, context):
    print("FIRST LAMBDA FUNCTION")
    if event['planet'] == 'Earth':
        return 'Moon'
    elif event['planet'] == 'Sun':
        return 'Not a planet'
    else:
        return 'No need'
