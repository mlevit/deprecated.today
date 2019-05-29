---
layout: post
title: AWS Lambda Linux execution environment update on June 16, 2019
date: 2019-05-14
categories: AWS
tags: [featured, lambda, runtime, linux, ami, execution]
---

AWS Lambda execution environment is being updated to version [2018.03](https://aws.amazon.com/amazon-linux-ami/2018.03-release-notes/) of Amazon Linux.

<!--more-->

**Service:** AWS Lambda

**Function:** Execution environment

## Timeline

![Timeline](https://d2908q01vomqb2.cloudfront.net/1b6453892473a467d07372d45eb05abc2031647a/2019/05/23/Screen-Shot-2019-05-23-at-3.11.35-PM-1024x178.png)

## Extract

AWS Lambda and AWS Lambda@Edge run on top of the Amazon Linux operating system distribution and maintain updates to both the core OS and managed language runtimes. We are updating the Lambda execution environment AMI to version [2018.03](https://aws.amazon.com/amazon-linux-ami/2018.03-release-notes/) of Amazon Linux. This newer AMI brings updates that offer improvements in capabilities, performance, security, and updated packages that your application code might interface with.

May 14, 2019 – Begin Testing: You can begin testing your functions for the new execution environment locally with AWS SAM CLI or using an Amazon EC2 instance running on Amazon Linux [2018.03](https://aws.amazon.com/amazon-linux-ami/2018.03-release-notes/). You can also proactively enable the new environment in AWS Lambda using the opt-in mechanism described in the original announcement post.

June 11, 2019 – New Function Create: All newly created functions will result in those functions running on the new execution environment, unless they have a delayed-update layer configured.

June 25, 2019 – Existing Function Update: All newly created functions or existing functions that you update will result in those functions running on the new execution environment, unless they have a delayed-update layer configured.

July 16, 2019 – General Update: Existing functions begin using the new execution environment on invoke, unless they have a delayed-update layer configured.

July 23, 2019 – Delayed Update End: All functions with a delayed-update layer configured start being migrated automatically.

July 29, 2019 – Migration End: All functions have been migrated over to the new execution environment.

## More Information

Link: <https://aws.amazon.com/blogs/compute/upcoming-updates-to-the-aws-lambda-execution-environment/>
