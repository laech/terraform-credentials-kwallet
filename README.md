# terraform-credentials-kwallet

A Terraform credentials helper backed by `kwalletcli`.

## Installation

1. Make sure `kwalletcli` is installed.
1. Copy or link the script `terraform-credentials-kwallet` to
`~/.terraform.d/plugins/` with the same file name, make it executable.
1. Edit `~/.terraformrc` to use the helper:
   ```hcl
   credentials_helper "kwallet" {}
   ```
1. Check `terraform-login` is using it:
   ```
   $ terraform login
   Terraform will request an API token for app.terraform.io using your browser.

   If login is successful, Terraform will store the token in the configured
   "kwallet" credentials helper for use by subsequent commands.

   Do you want to proceed?
   ```
## Reference
* [Terraform Credentials
  Helpers](https://developer.hashicorp.com/terraform/internals/credentials-helpers)
