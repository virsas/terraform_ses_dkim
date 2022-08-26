# terraform_ses_dkim

Terraform module to register DKIM for domain identity and create records to route53.

##  Dependencies

- Route53 - <https://github.com/virsas/terraform_route53>
- SES Domain - <https://github.com/virsas/terraform_ses_domain>

## Files

- None

## Terraform example

``` terraform
##############
# Variable
##############
# Not needed

##############
# Module
##############
module "ses_dkim_example" {
  source = "git::https://github.com/virsas/terraform_ses_dkim.git?ref=v1.0.0"
  domain = module.ses_domain_example.domain
  zone = module.route53_example_org.zone_id
}
```

## Outputs

- None