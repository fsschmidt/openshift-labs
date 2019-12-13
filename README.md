# openshift-labs
Openshift labs

cd $HOME/cakephp-ex/openshift/multi-project-templates
patch -p0 cakephp-namespaces.yml < cakephp-namespaces.patch

cd ..

oc process --local --param-file=openshift/multi-project-templates/parameters.yml --ignore-unknown-parameters -f openshift/multi-project-templates/cakephp-namespaces.yml | oc apply -f -

