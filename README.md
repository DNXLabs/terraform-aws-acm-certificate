# terraform-aws-acm-certificate

[![Lint Status](https://github.com/DNXLabs/terraform-aws-acm-certificate/workflows/Lint/badge.svg)](https://github.com/DNXLabs/terraform-aws-acm-certificate/actions)
[![LICENSE](https://img.shields.io/github/license/DNXLabs/terraform-aws-acm-certificate)](https://github.com/DNXLabs/terraform-aws-acm-certificate/blob/master/LICENSE)

<!--- BEGIN_TF_DOCS --->

## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.13.0 |
| aws | >= 2.7.0 |

## Providers

| Name | Version |
|------|---------|
| aws | >= 2.7.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| domain\_names | Domain names for this certificate - the first is the main domain and others are subject alternative names | `any` | n/a | yes |
| hosted\_zone\_id | Route53 hosted zone to create validation records. Must be set when validation\_method is DNS | `string` | `""` | no |
| validation\_method | DNS, EMAIL or NONE | `string` | `"DNS"` | no |

## Outputs

| Name | Description |
|------|-------------|
| arn | n/a |
| id | n/a |

<!--- END_TF_DOCS --->

## Authors

Module managed by [DNX Solutions](https://github.com/DNXLabs).

## License

Apache 2 Licensed. See [LICENSE](https://github.com/DNXLabs/terraform-aws-acm-certificate/blob/master/LICENSE) for full details.