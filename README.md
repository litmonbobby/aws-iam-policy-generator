# AWS IAM Policy Generator

This project is a simple Python CLI tool that helps generate AWS IAM policies for common use cases using pre-defined templates. It supports generating least-privilege access for S3, EC2, and Lambda.

## Features
- Generate IAM policies for:
  - Read-only S3 access
  - EC2 start/stop access
  - Lambda invoke-only access
- Outputs valid AWS policy JSON
- Simple CLI interface
- Easily extendable to more AWS services

## Skills Demonstrated
- Python scripting
- AWS IAM policy structure
- Security by least privilege
- JSON file creation

## Example Usage
```bash
$ python iam_policy_gen.py --service s3 --access read-only
```

## Example Output (S3 Read-Only)
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": "*"
    }
  ]
}
```

## Setup
```bash
git clone https://github.com/your-username/aws-iam-policy-generator.git
cd aws-iam-policy-generator
python iam_policy_gen.py --help
```

## Future Ideas
- Add IAM role trust policy templates
- Export to AWS via boto3
- Web interface using Flask

---

**Author:** Bobby Litmon  
**Contact:** litmonbobby@gmail.com
