# aws-mfa

Source this in the bash or zsh profile scripts:

    source aws-mfa

This will enable the following commands in the shell environment.

## aws-mfa-login

Retrieve temporary credentials and set them as environment variables. The caller identity
and connected MFA device are auto-detected using API calls to AWS.

    aws-mfa-login

A specific profile can be selected in the script and will set the AWS_PROFILE environment
variable.

    aws-mfa-login --profile myprofile

The duration of the temporay credentials can be specified as a parameter. The default in
the aws-mfa script is 7200 seconds (2 hours). The shortest duration supported by AWS is
900 seconds.

    aws-mfa-login --duration-seconds 900

## aws-mfa-clear

Remove the temporary credentials from the environment.

    aws-mfa-clear

## aws-mfa-whoami

Display account information and caller identity.


## Examples

https://github.com/Nike-Inc/gimme-aws-creds

AWS_DEFAULT_DURATION

aws_default_duration = This is optional. Lifetime for temporary credentials, in seconds. Defaults to 1 hour (3600)

gimme-aws-creds --action-configure --profile profileName


aws-mfa login --profile profileName

aws-mfa help

aws-mfa whoami

aws-mfa clear

aws-mfa clipboard export

aws-mfa show export
aws-mfa show redshift
aws-mfa show snowflake
