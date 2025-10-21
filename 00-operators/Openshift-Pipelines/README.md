# Openshift Pipelines

## 

### Install

> oc apply -f 01-Subscription.yaml

### Verify

> oc get tektonconfig config

> oc get tektonpipeline,tektontrigger,tektonchain,tektonaddon,pac

### Install tkn CLI 
[For more info](https://docs.redhat.com/en/documentation/red_hat_openshift_pipelines/1.20/html-single/pipelines_cli_tkn_reference/index#installing-tkn)

> subscription-manager register

> subscription-manager refresh

> subscription-manager list --available --matches '*pipelines*'

> subscription-manager attach --pool=<pool_id_from_l=previous_cmd>

> subscription-manager repos --enable="pipelines-1.20-for-rhel-8-x86_64-rpms"

> dnf install openshift-pipelines-client -y

> tkn version

or download from https://mirror.openshift.com/pub/openshift-v4/clients/pipelines/1.20.0/

> tar xvzf <file>

> sudo mv tkn /usr/local/bin/tkn

> sudo chmod +x /usr/local/bin/tkn

> tkn --help

#### Tab completion

> tkn completion bash > tkn_bash_completion

> sudo cp tkn_bash_completion /etc/bash_completion.d/


### debug cmds

> oc get pod --selector="app=openshift-pipelines-operator" --namespace openshift-operators

> for DEPLOYMENT in $(oc get deployment -n openshift-pipelines | grep -v NAME | awk '{print $1}'); do oc get deployment -n openshift-pipelines $DEPLOYMENT  -ojson | jq -r '.metadata.ownerReferences';done

> oc patch pipelinerun pipelinerun-name -p '{"metadata":{"finalizers":null}}' --type=merge -n namespace
