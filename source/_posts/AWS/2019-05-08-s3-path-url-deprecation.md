---
layout: post
title: Amazon S3 Path (URL) deprecation plan on September 39, 2020
date: 2019-05-08
categories: AWS
tags: [featured, s3, path, url]
---

AWS S3 bucket addresses are changing from `https://s3.amazonaws.com/<bucket>` to `https://<bucket>.s3.amazonaws.com`.

**Service:** Amazon S3

**Function:** Path / Address / URL

## Timeline

Support for the path-style model continues for buckets created on or before September 30, 2020. Buckets created after that date must be referenced using the virtual-hosted model.

## Extract

Old vs. New
S3 currently supports two different addressing models: path-style and virtual-hosted style. Let’s take a quick look at each one. The path-style model looks like either this (the global S3 endpoint):

`https://s3.amazonaws.com/jbarr-public/images/ritchie_and_thompson_pdp11.jpeg`
`https://s3.amazonaws.com/jeffbarr-public/classic_amazon_door_desk.png`

Or this (one of the regional S3 endpoints):

`https://s3-us-east-2.amazonaws.com/jbarr-public/images/ritchie_and_thompson_pdp11.jpeg`
`https://s3-us-east-2.amazonaws.com/jeffbarr-public/classic_amazon_door_desk.png`

In this example, `jbarr-public` and `jeffbarr-public` are bucket names; `/images/ritchie_and_thompson_pdp11.jpeg` and `/classic_amazon_door_desk.png` are object keys.

Even though the objects are owned by distinct AWS accounts and are in different S3 buckets (and possibly in distinct AWS regions), both of them are in the DNS subdomain s3.amazonaws.com. Hold that thought while we look at the equivalent virtual-hosted style references (although you might think of these as “new,” they have been around since at least 2010):

`https://jbarr-public.s3.amazonaws.com/images/ritchie_and_thompson_pdp11.jpeg`
`https://jeffbarr-public.s3.amazonaws.com/classic_amazon_door_desk.png`

These URLs reference the same objects, but the objects are now in distinct DNS subdomains (`jbarr-public.s3.amazonaws.com` and `jeffbarr-public.s3.amazonaws.com`, respectively). The difference is subtle, but very important. When you use a URL to reference an object, DNS resolution is used to map the subdomain name to an IP address. With the path-style model, the subdomain is always `s3.amazonaws.com` or one of the regional endpoints; with the virtual-hosted style, the subdomain is specific to the bucket. This additional degree of endpoint specificity is the key that opens the door to many important improvements to S3.

## More Information

Link: <https://aws.amazon.com/blogs/aws/amazon-s3-path-deprecation-plan-the-rest-of-the-story/>
