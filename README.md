**CFN-GUARD (CLOUDFORMATION GUARD)**:

This README explains how to write and test `cfn-guard` rules.

1. To check S3 Block Public Access:

cfn-guard file: `s3-public-access-check.guard`
cfn-guard unit test file: `s3_bucket_public_access_check_tests.yaml

- cfn-guard command: `cfn-guard validate --data s3-bucket.yaml --output-format yaml --rules s3-public-access-check.guard --show-summary pass,fail --type CFNTemplate`

- cfn-guard unit test command: `cfn-guard test --rules-file s3-public-access-check.guard --test-data s3_bucket_public_access_check_tests.yaml`

