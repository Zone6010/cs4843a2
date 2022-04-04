## CS4843 - Assignment 1 by Zachary Bowman (raq506)

# Overview:
This is a project for Cloud Computing at UTSA by Zachary Bowman, made with
the intent of deploying a website using Amazon's command-line compatability
and EC2 servers.

# AWS Deployment Using Command-Line Interface

The progam is ran through a file ran in a linux interface called create.sh, which takes in 3 arguments.

Example:

        ./create.sh myStack Network.yml networkparams.json

    Argument 1: What you wish to name your cloudFormation.

    Argument 2: The yml file that contains resources that will call upon argument 3 for definitions.

    Argument 3: The parameter's values in a JSON file.

# Network.yml
This file creates the "Networks": 

    The VPC, 
  
    the Internet Gateway, 
  
    Public subnets 1 and 2, 
  
    NAT gateways for the public subnets,
  
    Private subnets 1 and 2,
  
    Public and private route tables.
  


# Hosting Via Cloudfront


