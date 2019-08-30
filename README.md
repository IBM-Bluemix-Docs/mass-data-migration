# IBM Cloud Mass Data Migration
This repository stores documentation source files for the IBM Cloud Mass Data Migration service.

- [Jenkins build](https://wcp-ace-docs-jenkins.swg-devops.com/job/docs/job/build/job/cloud-docs/job/mass-data-migration)
- Slack channel: `#docs-mass-data-migrat`

## Publishing

Start in the `draft` branch of this repository. Commits to `draft` run a build, lint your content, and publish changes to the [IBM Cloud stage docs](https://test.cloud.ibm.com/docs/infrastructure/mass-data-migration). After you're happy with the changes, commit to the `publish` branch to publish them externally. Validate the changes in the [IBM Cloud production docs](https://cloud.ibm.com/docs/infrastructure/mass-data-migration).

### Staging

1. Commit to `draft`. Check that [the build](https://wcp-ace-docs-jenkins.swg-devops.com/job/docs/job/build/job/cloud-docs/job/key-protect) passes linting. 
2. Validate your changes in [staging](https://test.cloud.ibm.com/docs/infrastructure/mass-data-migration).

### Production

1. Work in `draft` branch until you're happy with the changes. 
2. Commit to the `publish` branch.
3. Validate your changes in [production](https://cloud.ibm.com/docs/infrastructure/mass-data-migration).
    

