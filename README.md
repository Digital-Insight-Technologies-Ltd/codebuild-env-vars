# codebuild-env-vars

Echo back all environment variables listed in this document: https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-env-vars.html

## Usage

Add the following command to the `install` or `pre_build` phase of your buildspec:

```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/solsglasses/codebuild-env-vars/master/install.sh)"
```

## Why not just `printenv | grep ^CODEBUILD`?

I want to see the value of all of these environment variables, even if they were not set. `printenv` will only print environment variables that are declared (obviously). In certain scenarios, especially when running [aws-codebuild-local](https://aws.amazon.com/blogs/devops/announcing-local-build-support-for-aws-codebuild/), many of these environment variables do not get set.
