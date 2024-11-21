# github_action_website_terraform

# Step 1: Define Jobs with a Manual Approval Step

GitHub Actions does not natively support manual approval prompts within a job, but you can achieve this by splitting the workflow into multiple jobs and using the workflow_run or environment approval feature.

### Using environment with Required Approval

## Set Up Environment with Approval:
* Go to your GitHub repository.
* Navigate to Settings > Environments.
* Create a new environment, e.g., prod-destroy, and configure it to __require manual approval__.

## Set up aws credentials :
Use AWS Access Key and Secret Key (Not Recommended for Production I recommand you to use __vault__)

If you prefer using access keys for authentication:
### Store Secrets in GitHub
1. Go to your repository on GitHub.
2. Navigate to Settings > Secrets and Variables > Actions > New repository secret.
3. Add the following secrets:
    * AWS_ACCESS_KEY_ID: Your AWS Access Key ID.
    * AWS_SECRET_ACCESS_KEY: Your AWS Secret Access Key.

