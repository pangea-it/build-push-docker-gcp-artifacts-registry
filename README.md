# build-push-docker-gcp-artifacts-registry
GitHub composite action to build, update version and push docker images to GCP artifacts repository.

## Assumptions ##
This composite action assumes the following:
1. That you have a functioning GCP account
2. Artifacts Respositry is enabled in your GCP account

## Prerequisites ##
This action uses the suggested [Wokload Identity Federation](https://cloud.google.com/iam/docs/configuring-workload-identity-federation#github-actions) 
to facilitate authentication with GCP, and uses the official [auth](https://github.com/google-github-actions/auth) action to perform the authentication.  
It's important to pay attention to the [prerequisites](https://github.com/google-github-actions/auth#prerequisites) mentioned in the auth action.
