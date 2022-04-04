## CS4843 - Assignment 1 by Zachary Bowman (raq506)

# Overview:
This is a project for Cloud Computing at UTSA by Zachary Bowman, made with
the intent of deploying a website using Amazon's command-line compatability
and EC2 servers.



# AWS Deployment Using Command-Line Interface

The progam is ran through a file ran in a linux interface called create.sh, which takes in 3 arguments.

    Argument 1: What you wish to name your cloudFormation.

    Argument 2: The yml file that contains resources that will call upon argument 3 for definitions.

    Argument 3: The parameter's values in a JSON file.
    
# Example

    ./create.sh myStack network.yml networkParams.json

# Network.yml
This file creates the "Networks": 

    The VPC, 
        >>This is the mediator to connect the autobalancer to the webservers.
        >>This will accept an IP range described by the user for in/out.
    The Internet Gateway, 
        >>This is the way the program connects to the internet, without it there is no in/out traffic.
    Public subnets 1 and 2, 
        >>This is where our VPC will live, and with it an elastic (unchanging) IP address.
    NAT gateways for the public subnets,
        
    Private subnets 1 and 2,
        
    Public and private route tables.
        


# Server-And-Security.yml
This file brings the server live, and put it into the private subnet, connecting to the VPC for in/out control.
This also creates our "Auto-Scaling Group" in the diagram.



# Storage-and-Database.yml
This file sets up the storage bucket into the private subnet to be accessed by only the servers whitelisted in the project.

