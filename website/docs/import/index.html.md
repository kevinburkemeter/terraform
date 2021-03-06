---
layout: "docs"
page_title: "Import"
sidebar_current: "docs-import"
description: |-
  Terraform is able to import existing infrastructure. This allows you take
  resources you've created by some other means and bring it under Terraform
  management.
---

# Import

Terraform is able to import existing infrastructure. This allows you take
resources you've created by some other means and bring it under Terraform
management.

This is a great way to slowly transition infrastructure to Terraform, or
to be able to be confident that you can use Terraform in the future if it
potentially doesn't support every feature you need today.

## Currently State Only

The current implementation of Terraform import can only import resources
into the [state](/docs/state). It does not generate configuration. A future
version of Terraform will also generate configuration.

Because of this, prior to running `terraform import` it is necessary to write
manually a `resource` configuration block for the resource, to which the
imported object will be mapped.

While this may seem tedious, it still gives Terraform users an avenue for
importing existing resources.

You can follow the [Terraform Import guide](https://learn.hashicorp.com/terraform/state/import?utm_source=WEBSITE&utm_medium=WEB_IO&utm_offer=ARTICLE_PAGE&utm_content=DOCS) on HashiCorp learn for a hands-on
introduction to using the `terraform import` command.
