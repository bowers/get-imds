# get-imds
Bash script to read common Instance MetaData Service (IMDS) values from multiple public clouds.

Returns just the text string of the value. Auto-detects which cloud an instance is running on (AWS, Microsoft Azure, Google Cloud, or Oracle Cloud). For AWS and Oracle Cloud, get-imds uses IMDSv1.


Usage: get-imds [key]

Key           | Value Returned
------------- | -------------
cloud         | Name of cloud the instance is running on (aws, azure, google, oracle)
region        | Region or zone the instances is running on
instance_type | Instance machine type / shape
image_name    | Name of the image (e.g. AMI)
vm_id         | Identifier assigned by the cloud
private_ip    | Private IP address for the first network interface (X.X.X.X) 
public_ip     | Not available from all clouds

Getting Started
```
curl https://raw.githubusercontent.com/bowers/get-imds/main/get-imds > get-imds && chmod +x ./get-imds
./get-imds cloud
./get-imds instance_type
```




