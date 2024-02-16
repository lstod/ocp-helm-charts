# ocp-helm-charts

## How to:

### Install

- sign in to openshift and select project
- check to see if repo is connected
    `helm search repo`
    - if not present or you want to add a new repo
    `helm repo add <name> <url>`
    - example for this repo:
        `helm repo add helm_charts https://lstod.github.io/ocp-helm-charts`
    - search again and confirm
- install the desired chart
    `helm install <chart-name> <chart-path-in-repo>`
    - example
        `helm install my-metabase-name helm_charts/metabase`
        - configure yaml in oc to get up and running

### Upgrade

- push changes to repo
    - ensure version number increases with each update
- update repo in oc
    `helm repo update`
- upgrade specific helm release
    `helm upgrade <helm-name> <chart-path>`
    - example:
    `helm upgrade my-metabase-name helm_charts/metabase`