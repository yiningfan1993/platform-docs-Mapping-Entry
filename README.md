# alpaca-docs-teamwork

This repo is for the documents of Ecopia Map Platform - Workflow Assembler Application.

## order of titles
```
#*=~-"
```

## Build
```bash
make html
```

## Deployment

### For main branch
```bash
cd build
aws sts get-session-token --serial-number 'arn:aws:iam::xxx:mfa/xxx' --token-code xxx
AWS_ACCESS_KEY_ID=xxx AWS_SECRET_ACCESS_KEY=xxx AWS_SESSION_TOKEN=xxx aws s3 sync --delete ./ s3://ecopia-platform-resource/docs/workflow-assembler/main/
