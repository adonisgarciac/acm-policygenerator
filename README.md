# acm-policygenerator

## policy-generator file config reference.
https://github.com/open-cluster-management-io/policy-generator-plugin/blob/main/docs/policygenerator-reference.yaml

## Create ManagedClusterSetBinding

```
oc apply -f managedclustersetbinding.yaml
```

## Create placement

```
oc apply -f placement-global.yaml
```

## Patch ArgoCD Instance to enable alpha kustomize plugins

```
oc patch ArgoCD openshift-gitops --patch-file argocd-patch.yaml -n openshift-gitops --type merge
```

## Create argocd app to apply policies

```
oc apply -f argocd-app.yaml
```