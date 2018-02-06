# temas.ticnsp.org 
## Blogging website built with hugo

This static website holds the lectures given at TIC. This material is for coordinators to read and then explain to children.

### Instructions

First, install hugo on your system, follow the [Getting Started](https://gohugo.io/getting-started/) guide.


Clone this repo:

```bash
$ git clone https://github.com/ticnsp/temasblog
```

And you are done! To compile run the hugo command:

```bash
$ hugo
```

or use the hugo server to view:

```bash
$ hugo server -D
```

### Deploying

If you will deploy to AWS S3, install the [awscli](https://docs.aws.amazon.com/cli/latest/userguide/installing.html) as well.

Using the aws cli, apply website.json configuration to your bucket:

```bash
aws s3api put-bucket-website --bucket <BUCKET_NAME> --website-configuration file://website.json
```

<strong>Note:</strong> When deploying with Cloudfront, use the bucket website url and deploy as custom origin instead of an S3 bucket origin.

Refer to this blog [post](https://lustforge.com/2016/02/27/hosting-hugo-on-aws/) for more information.
