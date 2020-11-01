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
