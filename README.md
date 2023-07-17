
# Bucket-S3-Python
Creating bucket S3 AWS with Python version 3.10 and Boto3 tools

# Import Tools 
import Boto3

# defining the variable client to create bucket S3
client = boto3.client('s3') 

# Creating bucket S3
client.create_bucket(Bucket='padzxlearningboto3')

# Listing All Buckets 

client = boto3.client('s3')
response = client.list_buckets()

response['Buckets']

# Listing Files and Uploading Files 

bucket_name = "padzxlearningboto3"

s3 = boto3.client('s3')

# List all object inside of bucket chosen

response = s3.list_objects_v2(Bucket=bucket_name)

for obj in response["Contents"]:
    
    print(obj)


# Uploading files from local to send AWS

with open("C:\\Users\\Padzx\\Desktop\\Boto3\\morales.jpg", "rb") as f:
    s3.upload_fileobj(f, bucket_name, "morales.jpg") 






# Documentation Boto3 Python AWS
https://boto3.amazonaws.com/v1/documentation/api/latest/index.html
