# build-push-docker-gcp-artifacts-registry
GitHub composite action to build, update version and push docker images to GCP artifacts repository.

## Assumptions ##
This composite action assumes the following:
1. That you have a functioning GCP account
2. Artifacts Respositry is enabled in your GCP account
3. [Wokload Identity Federation](https://cloud.google.com/iam/docs/configuring-workload-identity-federation#github-actions) is properly set in your GCP account, to access the artifacts repository. See [here](https://cloud.google.com/blog/products/identity-security/enabling-keyless-authentication-from-github-actions) and [here](https://gist.github.com/palewire/12c4b2b974ef735d22da7493cf7f4d37#how-to-push-tagged-docker-releases-to-google-artifact-registry-with-a-github-action).


## Prerequisites ##
This action uses the suggested [Wokload Identity Federation](https://cloud.google.com/iam/docs/configuring-workload-identity-federation#github-actions) 
to facilitate authentication with GCP, and uses the official [auth](https://github.com/google-github-actions/auth) action to perform the authentication.  
It's important to pay attention to the [prerequisites](https://github.com/google-github-actions/auth#prerequisites) mentioned in the auth action.
