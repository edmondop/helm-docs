nginx-ingress
=============
A simple wrapper around the stable/nginx-ingress chart that adds a few of our conventions

This chart's source code can be found [here](https://github.com/norwoodj/helm-docs)


## Chart Requirements

| Repository | Name | Version |
|------------|------|---------|
| @stable | nginx-ingress | 0.22.1 |


## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| controller.extraVolumes[0].configMap.name | string | "nginx-ingress-config" | Uses the name of the configmap created by this chart |
| controller.extraVolumes[0].name | string | "config-volume" |  |
| controller.image.repository | string | "nginx-ingress-controller" |  |
| controller.image.tag | string | "18.0831" |  |
| controller.ingressClass | string | "nginx" | Name of the ingress class to route through this controller |
| controller.name | string | "controller" |  |
| controller.persistentVolumeClaims | list | [] | List of persistent volume claims to create |
| controller.podLabels | object | {} | The labels to be applied to instances of the controller pod |
| controller.publishService.enabled | bool | false | Whether to expose the ingress controller to the public world |
| controller.replicas | int | \<nil\> | Number of nginx-ingress pods to load balance between |