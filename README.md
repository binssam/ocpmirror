# ocpmirror
openshift mirror

Steps to run the oc-mirror

oc-mirror --config /mirror/ocpmirior/imageset.yaml file:///mirror/ --v2 --authfile /Iun/user/1000/containers/auth.json --parallel-images 10 --parallel-layers 10 --image-timeout 60m --retry-delay 10s --retry-times 2
