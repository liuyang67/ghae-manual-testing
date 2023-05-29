This document is adapted from [GHES Actions test plan](https://github.com/github/pe-releases/blob/master/qa/ghes-manifests/actions/actions.md).
# Installation and Configuration
  - [ ] create an instance with `--enable-actions` 
  - [ ] Appliance administrators can enable and disable Actions and [set policies](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/access-policy.md)
    - [ ] Enterprise admins can adjust actions policies to enable/disable actions for all orgs or specific orgs
    - [ ] Org admins can enable/disable actions for all repos or specific repos in the org
    - [ ] Repo admins can choose actions policies that are more restrictive than org policies
  * _Pre-requisite:_ Customers will need to configure a self-hosted runner to run workflows
    - [ ] Users with repo write access can configure self-hosted runner on the repo and manage it's settings
    - [ ] Org owners and admins can configure org level runners and manage their policies 
    - [ ] Enterprise admins can configure enterprise level runners and manage their policies 
# Running Actions
  * [ ] Users see an Actions tab on the repositories when actions is enabled on the appliance
  * [ ] Clicking on the Actions tab in a new repo shows starter workflows
  * [ ] Users can edit and commit the "blank" workflow file and it should work out of the box.
  * [ ] Users can use `actions/checkout@v2` and other first party actions which pulls that Action from the GHAE instance - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/first-party-actions.md)
  * [ ] Users can pull other 3rd party actions from https://github.com - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/third-party-actions.md)
  * [ ] Users can use the API against the GHAE instance in a workflow - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/github-api.md)
  * [ ] Users can set secrets, use the secrets in Actions, and delete secrets - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/secret.md)
  * [ ] Users can cancel a build - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/cancel.md)
  * [ ] Users can request re-runs - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/re-run.md)
  * [ ] Logs stream to the user as they run the build.
  * [ ] Logs are accessible to the user once the build has completed.
  * [ ] Artifacts are accessible to the user once the build has completed and also can be deleted - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/artifacts.md)
  * [ ] Logs can be deleted - [docs](https://help.github.com/en/actions/configuring-and-managing-workflows/managing-a-workflow-run#deleting-logs)
  * [ ] Workflow runs can be deleted
# API
  * [ ] The Actions API works and is accessible to the user - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/actions-api.md)
  * [ ] Runner APIs can be used to scale up or scale down - [test manifest](https://github.com/github/c2c-actions/tree/master/docs/test-manifests/runners-api.md)

Additional test manifests for Actions features will be uploaded [here](https://github.com/github/c2c-actions/tree/master/docs/test-manifests). 
