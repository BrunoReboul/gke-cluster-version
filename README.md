# gke-cluster-version

## Export GKE cluster assets

```shell
gcloud asset export --organization=<yourorgnumber> --asset-types=container.googleapis.com/Cluster --content-type=resource --output-path=gs://<yourBucketName>/gke.json
```

Download the export result file

## Install go

https://go.dev/doc/install

## Parse the export to output a CSV file name / version

```shell
go run tool.go
```

by default the input is named gke.json  
by default the output is named result.csv  

Example

```text
//container.googleapis.com/projects/<theProjectID>/zones/us-central1-c/clusters/cluster-1,1.18.20-gke.901
//container.googleapis.com/projects/<theProjectID>/zones/europe-west1-b/clusters/cluster-2,1.20.12-gke.1500
```
