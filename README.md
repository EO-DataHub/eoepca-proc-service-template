# The Workflow Service Template Used by the Workflow Runner

This repository is cloned by the Workflow Runner and used to deploy new workflows to the ADES, it defines pre- and post-processing steps when executing workflows. Edits can be made to this repository and then the branch, `cookiecutter.templateBranch`, in the ZOO Project helm chart will need to be updated to configure the branch you wish to clone.

mamba env create -f .devcontainer/environment.yml

mamba activate env_zoo_calrissian

export PYTHONPATH=/data/work/eoepca/eoepca-proc-service-template/tests/water_bodies/

kubectl --namespace zoo port-forward s3-service-7fbbc44d98-wjqsp 9000:9000 9001:9001

Create a file `tests/.env` with:

```
CLIENT_ID = "..."
CLIENT_SECRET = "..."
OIDC_ENDPOINT = "https://auth.demo.eoepca.org/.well-known/openid-configuration"
USER_NAME = "eric"
PASSWORD = "..."
```

Run the tests with:

```
nose2
```
