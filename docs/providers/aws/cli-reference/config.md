<!--
title: Serverless Framework Commands - AWS Lambda - Config
menuText: Config
menuOrder: 1
description: Configure Serverless.
layout: Doc
-->

<!-- DOCS-SITE-LINK:START automatically generated  -->
### [Read this on the main serverless docs site](https://www.serverless.com/framework/docs/providers/aws/cli-reference/config)
<!-- DOCS-SITE-LINK:END -->

# Config

This plugin helps you to configure Serverless.

## Configure credentials

```bash
serverless config credentials --provider provider --key key --secret secret
```

### Options

- `--provider` or `-p` The provider (in this case `aws`). **Required**.
- `--key` or `-k` The `aws_access_key_id`. **Required**.
- `--secret` or `-s` The `aws_secret_access_key`. **Required**.
- `--profile` or `-n` The name of the profile which should be created.

### Provided lifecycle events

- `config:credentials:config`

### Examples

#### Configure the `default` profile

```bash
serverless config credentials --provider aws --key 1234 --secret 5678
```

This example will configure the `default` profile with the `aws_access_key_id` of `1234` and the `aws_secret_access_key` of `5678`.

#### Configure a custom profile

```bash
serverless config credentials --provider aws --key 1234 --secret 5678 --profile custom-profile
```

This example create and configure a `custom-profile` profile with the `aws_access_key_id` of `1234` and the `aws_secret_access_key` of `5678`.
