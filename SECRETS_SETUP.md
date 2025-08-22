# GitHub Secrets Setup Instructions

============================================================
⚠️ GITHUB SECRETS SETUP REQUIRED
============================================================

The GitHub Actions workflow requires AWS credentials.

## AWS IAM User: github-actions-amplify

Access Key IDs found:

- AKIAVPEYWTPUQYALNZFN
- AKIAVPEYWTPUY6WTA3XV

The IAM user has existing access keys, but the secret key cannot be retrieved.
You need to either:

1. Use previously saved credentials if you have them
2. Create new access keys (this will create a third set):
   ```bash
   aws iam create-access-key --user-name github-actions-amplify
   ```

## GitHub Secrets Page

URL: https://github.com/kjetilgeirbo/auth-test-v5/settings/secrets/actions

Add these two secrets:

1. **AWS_ACCESS_KEY_ID** - Your AWS access key ID
2. **AWS_SECRET_ACCESS_KEY** - Your AWS secret access key

============================================================

## After Adding Secrets

Once you've added the secrets, push code to trigger the pipeline:

```bash
git push
```
