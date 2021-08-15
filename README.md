# terratest-shell-e2e-poc
Proof of Concept for a shell-based E2E test using Terratest for an ephemeral EC2 instance

This project uses Terratest to spin up a Terraform instance and run SSH commands inside it, then tear everything down afterward. Terraform code is in [./tf](./tf) and test is in [./test](./test)

## Usage

```shell
# Recommend using aws-vault to pass creds. Friends don't let friends use unencrypted AWS creds.

# Run the test
aws-vault exec myprofile -- go test -v ./...

# Or you can use `task`
aws-vault exec myprofile -- task test
```
