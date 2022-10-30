<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_S3"></a> [S3](#module\_S3) | ../../../modules/S3/1.0 | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/caller_identity) | data source |
| [aws_region.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/region) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ACL"></a> [ACL](#input\_ACL) | Accepted values are 'private','public-read','public-read-write','aws-exec-read','authenticated-read','log-delivery-write' | `string` | `"private"` | no |
| <a name="input_BUCKET_NAME"></a> [BUCKET\_NAME](#input\_BUCKET\_NAME) | n/a | `string` | `""` | no |
| <a name="input_BUCKET_POLICY"></a> [BUCKET\_POLICY](#input\_BUCKET\_POLICY) | n/a | `string` | `""` | no |
| <a name="input_KMS_KEY_ARN"></a> [KMS\_KEY\_ARN](#input\_KMS\_KEY\_ARN) | n/a | `string` | `""` | no |
| <a name="input_LIFECYCLE_RULE"></a> [LIFECYCLE\_RULE](#input\_LIFECYCLE\_RULE) | n/a | <pre>list(object({<br>        rule_name = string<br>        prefix = string<br>        transition = list(object({<br>            days = number<br>            storage_class = string<br>        }))<br>        expiration = object({<br>            days = number<br>        })<br>      }))</pre> | `[]` | no |
| <a name="input_REGION"></a> [REGION](#input\_REGION) | n/a | `string` | `""` | no |
| <a name="input_SSE_ALGORITHM"></a> [SSE\_ALGORITHM](#input\_SSE\_ALGORITHM) | Server Side Encryption Values i-e AES256 or aws:kms | `string` | `"aws:kms"` | no |
| <a name="input_TAGS"></a> [TAGS](#input\_TAGS) | n/a | `map` | <pre>{<br>  "TagKey": "TagValue"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_S3_BUCKET"></a> [S3\_BUCKET](#output\_S3\_BUCKET) | n/a |
| <a name="output_S3_BUCKET_NAME"></a> [S3\_BUCKET\_NAME](#output\_S3\_BUCKET\_NAME) | n/a |
<!-- END_TF_DOCS -->
