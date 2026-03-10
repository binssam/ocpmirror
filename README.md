Download the disconnected tools from the below URL

https://console.redhat.com/openshift/downloads

tar xvzf oc-mirror.tar.gz

chmod +x oc-mirror

sudo mv oc-mirror /usr/local/bin/.

oc mirror --v2 --help

Get the registry.redhat.io pull secret from https://console.redhat.com/openshift/install/pull-secret

cat ./pull-secret | jq . > '/opt/openshift-install/'

mkdir -p $XDG_RUNTIME_DIR/containers

Save the pull secret file as $XDG_RUNTIME_DIR/containers/auth.json

Generate the base64-encoded user name and password or token for the mirror registry by running the following command:

echo -n '<user_name>:<password>' | base64 -w0




# ocpmirror
openshift mirror

Steps to run the oc-mirror

oc-mirror --config /mirror/ocpmirior/imageset.yaml file:///mirror/ --v2 --authfile /Iun/user/1000/containers/auth.json --parallel-images 10 --parallel-layers 10 --image-timeout 60m --retry-delay 10s --retry-times 2
