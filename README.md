Commands use:

helm install arc     --namespace "${NAMESPACE}"     --create-namespace     oci://ghcr.io/actions/actions-runner-controller-charts/gha-runner-scale-set-controller --version 0.13.1


kubectl create secret generic arc-secrets \
  --namespace=gha-maven-runner \
  --from-literal=github_app_id=id \
  --from-literal=github_app_installation_id=id \
  --from-file=github_app_private_key=/home/deivid.andrade/


 INSTALLATION_NAME="maven-runner"
    NAMESPACE="gha-maven-runner"
    GITHUB_CONFIG_URL="https://github.com/deivid-andrade"
    GITHUB_PAT=""
    helm install "${INSTALLATION_NAME}" -f  values.yaml --namespace "${NAMESPACE}" --create-namespace .