# terraform-aws-acm-certificate

[![Lint Status](https://github.com/DNXLabs/terraform-aws-acm-certificate/workflows/Lint/badge.svg)](https://github.com/DNXLabs/terraform-aws-acm-certificate/actions)
[![LICENSE](https://img.shields.io/github/license/DNXLabs/terraform-aws-acm-certificate)](https://github.com/DNXLabs/terraform-aws-acm-certificate/blob/master/LICENSE)


## Usage

```hcl
module "acm_certificate" {
  source = "git::https://github.com/DNXLabs/terraform-aws-acm-certificate?ref=0.2.2"

  domain_names             = ["example.com", "*.example.com"]
  validation_method        = "DNS"
  create_validation_record = false
}
```

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
| hosted\_zone\_id | Route53 hosted zone to create validation records. For use when validation\_method is DNS. Leave it blank to validate manually. | `string` | `""` | no |
| validation\_method | DNS, EMAIL or NONE | `string` | `"DNS"` | no |

## Outputs

| Name | Description |
|------|-------------|
| arn | n/a |
| dns\_validation\_records | n/a |
| id | n/a |

<!--- END_TF_DOCS --->

## Authors

Module managed by [DNX Solutions](https://github.com/DNXLabs).

## License

Apache 2 Licensed. See [LICENSE](https://github.com/DNXLabs/terraform-aws-acm-certificate/blob/master/LICENSE) for full details.