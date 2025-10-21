## Install operators form CLI

**Red Hat Openshift Pipelines**  
[for more](https://docs.redhat.com/en/documentation/red_hat_openshift_pipelines/1.20)

> oc create -f 00-operators/Openshift-Pipelines/01-Subscription.yaml

**Red Hat Openshift Pipelines**  
[for more](https://docs.redhat.com/en/documentation/red_hat_openshift_gitops/1.18)

> oc create ns openshift-gitops-operator

> oc label namespace openshift-gitops-operator openshift.io/cluster-monitoring=true

> oc create -f 00-operators/Openshift-GitOps/01-OperatorGroup.yaml

> oc create -f 00-operators/Openshift-GitOps/02-Subscription.yaml

**Red Hat Openshift Dev Spaces**  
[For more](https://docs.redhat.com/en/documentation/red_hat_openshift_dev_spaces/3.23/html/administration_guide/index)

> oc create -f 00-operators/Openshift-DevSpaces/01-Subscription.yaml
