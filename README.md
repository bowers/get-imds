# get-imds
Script to read common Instance MetaData Service (IMDS) values from multiple public clouds

Returns just the text string of the value. Auto-detects which cloud an instance is running on (AWS, Microsoft Azure, Google Cloud, or Oracle Cloud). 

Usage:
get-imds [key]

Valid keys:
cloud - Name of cloud the instance is running on (aws, azure, google, oracle)

region - Region or zone the instances is running on

instance_type - Instance machine type / shape

image_name - Name of the image (e.g. AMI)

vm_id - Identifier assigned by the cloud

private_ip - Private IP address for the first network interface (X.X.X.X) 

public_ip - Not available from all clouds


get-imds uses wget to fetch the IMDS information.  It will install wget if not available.
For AWS and Oracle Cloud, get-imds uses IMDSv1.


