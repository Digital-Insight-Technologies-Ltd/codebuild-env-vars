# codebuild-env-vars

Echo back all environment variables listed in this document: https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-env-vars.html

## Usage

Add the following command to the `install` or `pre_build` phase of your buildspec:

```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/solsglasses/codebuild-env-vars/master/install.sh)"
```