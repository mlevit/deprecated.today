---
layout: post
title: AWS Lambda runtime support ends for Node.js 6.10 on April 30, 2019
date: 2019-04-30
categories: AWS
tags: [lambda, node.js, 6.10, runtime]
---

Support is being ended for Node.js 6.10 AWS Lambda runtimes on April 30, 2019.

<!--more-->

**Service:** AWS Lambda

**Function:** Runtime

## Timeline

| End of Life    | Deprecation (Create) | Deprecation (Update) |
| -------------- | -------------------- | -------------------- |
| April 30, 2019 | April 30, 2019       | June 30, 2019        |

## Extract

AWS Lambda runtimes are built around a combination of operating system, programming language, and software libraries that are subject to maintenance and security updates. When a component of a runtime is no longer supported for security updates, Lambda deprecates the runtime.

Deprecation occurs in two phases. During the first phase, you can no longer create functions that use the deprecated runtime. For at least 30 days, you can continue to update existing functions that use the deprecated runtime. After this period, both function creation and updates are disabled permanently. However, the function continues to be available to process invocation events.

| Name         | Identifier | End of Life    | Deprecation (Create) | Deprecation (Update) |
| ------------ | ---------- | -------------- | -------------------- | -------------------- |
| Node.js 6.10 | nodejs6.10 | April 30, 2019 | April 30, 2019       | June 30, 2019        |

## More Information

- <https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html>
