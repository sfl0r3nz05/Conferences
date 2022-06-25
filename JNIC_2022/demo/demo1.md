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

3. Define cluster

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
    kubectl create namespace verify-pod-security
    ```

7. Label the namespace to enforce the restricted Pod Security Standard

    ```console
    kubectl label namespace verify-pod-security pod-security.kubernetes.io/enforce=restricted
    kubectl get ns verify-pod-security -o yaml
    ```

8. Test the creation of a test Pod and confirm that is no admited

    ```console
    kubectl -n verify-pod-security run test --dry-run=server --image=busybox --privileged
    ```

9. If you receive Forbiden error from server the test is successfull

10. Clean up

    ```console
    kubectl delete namespace verify-pod-security
    ```