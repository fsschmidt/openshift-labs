# openshift-labs
# 10_1_Network_Policy

## 2.3

### 1
`cd $HOME/cakephp-ex/openshift/multi-project-templates`

`patch -p0 cakephp-namespaces.yml < cakephp-namespaces.patch`

`cd ../../`

`oc process --local --param-file=openshift/multi-project-templates/parameters.yml --ignore-unknown-parameters -f openshift/multi-project-templates/cakephp-namespaces.yml | oc apply -f -`

### 3

`cd $HOME/cakephp-ex/openshift/multi-project-templates`

`patch -p0 cakephp-mysql-frontend.yml < cakephp-mysql-frontend.patch`

`cd ../../`

`oc process --local \
--param=VERSION=0.1 \
--param-file=openshift/multi-project-templates/parameters.yml \
--ignore-unknown-parameters \
-f openshift/multi-project-templates/cakephp-mysql-frontend.yml \
| oc apply -f -`

### 4

`patch -p0 cakephp-mysql-persistent.yml < cakephp-mysql-persistent.patch`

`cd $HOME/cakephp-ex/openshift/multi-project-templates`

`oc process --local --param-file=openshift/multi-project-templates/parameters.yml --ignore-unknown-parameters -f openshift/multi-project-templates/cakephp-mysql-persistent.yml | oc apply -f -`

## Confirm that you can still access the CakePHP example application in your web browser using the same route hostname as before.
