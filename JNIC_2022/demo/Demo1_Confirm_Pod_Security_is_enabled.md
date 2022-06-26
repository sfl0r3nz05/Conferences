# Confirm Pod Security is enabled

1. Download kind

    ```console
    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64
    ```

2. Install kind

    ```console
    sudo mv ./kind /usr/local/bin/kind
    chmod 0755 /usr/local/bin/kind
    ```

3. Cluster definition

    ```console
    nano kind-config.yaml
    ```

    ```console
    kind: Cluster
    apiVersion: kind.x-k8s.io/v1alpha4
    featureGates:
    PodSecurity: true
    nodes:
    - role: control-plane
    - role: worker
    ```

4. Create a cluster

    ```console
    kind create cluster --image=kindest/node:v1.22.0@sha256:b8bda84bb3a190e6e028b1760d277454a72267a5454b57db34
    437c34a588d047 --config kind-config.yaml
    ```

5. Check the API server flag

    ```console
    kubectl -n kube-system exec kube-apiserver-kind-control-plane -it -- kube-apiserver -h | grep "default enabled ones"
    ```

6. Create a namespace to run the test

    ```console
    kubectl create namespace jnic2022-pod-security
    ```

7. Label the namespace to enforce the restricted Pod Security Standard

    ```console
    kubectl label namespace jnic2022-pod-security pod-security.kubernetes.io/enforce=restricted
    ```

8. Verify policy labeled

    ```console
    kubectl get ns jnic2022-pod-security -o yaml
    ```

9. Test the creation of a test Pod and confirm that is no admited

    ```console
    kubectl -n jnic2022-pod-security run test --dry-run=server --image=busybox --privileged
    ```

10. If you receive Forbiden error from server the test is successfull. E.g.:

    ```console
    Error from server (Forbidden): pods "test" is forbidden: error looking up service account jnic2022-pod-security/default: serviceaccount "default" not found
    ```

11. Clean up

    ```console
    kubectl delete namespace jnic2022-pod-security
    ```