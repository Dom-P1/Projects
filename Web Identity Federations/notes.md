# Notes

## IAM Role Example
- Trust policy includes Google as identity provider
- Permissions: S3 access only (no admin rights)

## Web Identity Providers Configured
- Google OAuth App ID: (example placeholder)
- Facebook App ID: (example placeholder)

## STS
- AssumeRoleWithWebIdentity tested via AWS CLI and Console

## Security Notes
- Temporary credentials expire after 1 hour
- Logging enabled for all API actions via CloudTrail
