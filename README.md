Prerequisites

- Docker

To run the playbook:

```bash
docker run -i -t --rm --name agnosticd-runner --entrypoint /usr/local/bin/ansible-playbook \
-v $PWD:/runner \
-v ${KUBECONFIG}:/home/runner/.kube/config \
quay.io/agnosticd/ee-multicloud:v0.0.11 \
playbooks/ocp4_workload_cloud_architecture_workshop.yml
```

Remove workload

```bash
docker run -i -t --rm --name agnosticd-runner --entrypoint /usr/local/bin/ansible-playbook \
-v $PWD:/runner \
-v ${KUBECONFIG}:/home/runner/.kube/config \
quay.io/agnosticd/ee-multicloud:v0.0.11 \
playbooks/ocp4_workload_cloud_architecture_workshop.yml \
-e="ACTION=remove"
```