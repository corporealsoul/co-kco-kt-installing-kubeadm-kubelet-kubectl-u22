### Installing kubeadm, kubelet and kubectl , Red Hat 9 , https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/#installing-kubeadm-kubelet-and-kubectl

<br>

**Update the apt package index and install packages needed to use the Kubernetes apt repository ,**

`anup@ubuntu-22042-08:~$ sudo apt-get update`

`anup@ubuntu-22042-08:~$ sudo apt-get install -y apt-transport-https ca-certificates curl`

<br>

**Download the Google Cloud public signing key ,**

`anup@ubuntu-22042-08:~$ curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-archive-keyring.gpg`

<br>

**Add the Kubernetes apt repository ,**

`anup@ubuntu-22042-08:~$ echo "deb [signed-by=/etc/apt/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list`

<br>

**Update apt package index, install kubelet, kubeadm and kubectl, and pin their version ,**

`anup@ubuntu-22042-08:~$ sudo apt-get update`

`anup@ubuntu-22042-08:~$ sudo apt-get install -y kubelet kubeadm kubectl`

`anup@ubuntu-22042-08:~$ sudo apt-mark hold kubelet kubeadm kubectl`

<br>

`anup@ubuntu-22042-08:~$ kubelet --version`

`anup@ubuntu-22042-08:~$ kubeadm version`

`anup@ubuntu-22042-08:~$ kubectl version`

<br>
