# Platform setup in RHOCP
Get all products details [here](https://docs.redhat.com/en/products)


```shell script
oc get catalogsource -A
```

```shell script
oc get packagemanifests -n openshift-marketplace

oc get packagemanifests -n openshift-marketplace | grep redhat-operators
```

```shell script
oc describe packagemanifest <operator_name> -n openshift-marketplace
```

<!-- oc get packagemanifests -n openshift-marketplace -o json | jq -r '.items[] | select(.status.catalogSource=="redhat-operators") | .metadata.name' -->

<!-- oc get packagemanifest openshift-gitops-operator -n openshift-marketplace -o jsonpath='{range .status.channels[*]}{.name}{"\t"}{.currentCSV}{"\n"}{end}' -->

- [GitLab CE]()
- [Quay Registry]()

- [Red Hat 3scale Intergration + API gateway]()

- [Red Hat Openshift DevSpaces]()
- [Red Hat Developer Hub]()
- [Streams for Apache Kafka + console]()
- [Red Hat Build of Keycloak]()

- [Openshift Pipelines]()
- [Openshift GitOps]()

- [Red Hat OpenTelemetry]()
- [Red Hat LokiStack]()
- [Red Hat TemoStack]()
- [Cluster Observability Operator]()

- [Red Hat Openshift ServiceMesh 3]()

- [Red Hat OADP]()

- [Red Hat Advanced Cluster Manager]()
- [Red Hat Advanced Cluster Security]()
