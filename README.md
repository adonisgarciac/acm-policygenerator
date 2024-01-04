# acm-policygenerator

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