# GCP VPC 

## Using module
You can use this module like as below example.

```
provider "google" {
  region      = "us-central1"
  project     = "${var.your_proj}"
  credentials = "${file("key.json")}"
}

module "vpc" {
  source          = "${var.module_url}"
  vpc_name        = "test_vpc_gcp"
  regions         = "${var.regions}"
  private_subnets = "${var.private_subnets}"
  public_subnets  = "${var.public_subnets}"
}
```
