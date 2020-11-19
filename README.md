# helm-chart

## Requirement
You have to install [helm](https://helm.sh/docs/intro/install/).  

## HOWTO

First you have to create a subfolder under `helm-chart-source`. Folder name should be the same as the name of your service.  
Then you have to package and push the new service to the repo:
```
helm package helm-chart-sources/<servicename>
helm repo index --url https://informasjonsforvaltning.github.io/helm-chart/ .
git add *
git commit -m"<beskrivelse av endring>"
git push
```
Example:
```
helm package helm-chart-sources/fdk-harvest-scheduler
helm repo index --url https://informasjonsforvaltning.github.io/helm-chart/ .
git add *
git commit -m"added helm template for harvest scheduler service"
git push
```
