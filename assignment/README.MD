### Assignment

## Cluster Architecture Requirements

- [ ] There are three master nodes working

- [ ] There are two worker nodes

- [ ] There are two infra nodes

- [ ] Image registry is running on one of the infra nodes

- [ ] Routers (two replicas) are running on two infra nodes

- [ ] Logging and monitoring are running on the infra nodes

- [ ] Elasticsearch should run on two nodes and have SingleRedundancy

## Sizing Requirements

- [ ] Masters: instance size .xlarge (m4.xlarge or m5.xlarge)

- [ ] Infra nodes: instance size .xlarge (m4.xlarge or m5.xlarge)

- [ ] Workers: instance size .large (m4.large or m5.large)

- [ ] Elasticsearch: make storage volume 20G, memory request 4Gi, CPU request 500m

*Hint: you will have to edit the clusterlogging object to change the requests*
