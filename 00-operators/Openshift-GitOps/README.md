# Openshift GitOps

## 

### Install

> oc create -f 01-OperatorGroup.yaml

> oc create -f 02-Subscription.yaml

### Verify

> oc get pods -n openshift-gitops
> oc get pods -n openshift-gitops-operator

### Install Argocd form CLI

> subscription-manager register

> subscription-manager refresh

> subscription-manager list --available --matches '*gitops*'

> subscription-manager attach --pool=<pool_id>

> subscription-manager repos --enable="gitops-<gitops_version>-for-rhel-<rhel_version>-x86_64-rpms"

> dnf install openshift-gitops-argocd-cli -y

or  

Download from https://developers.redhat.com/content-gateway/rest/browse/pub/openshift-v4/clients/openshift-gitops/latest/

> tar xvzf <file>

> sudo mv argocd /usr/local/bin/argocd

> sudo chmod +x /usr/local/bin/argocd

Verify

> argocd version --client
