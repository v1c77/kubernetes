
Installs all addons to a Kubernetes cluster

### Synopsis

Installs the CoreDNS and the kube-proxy addons components via the API server. Please note that although the DNS server is deployed, it will not be scheduled until CNI is installed. 

Alpha Disclaimer: this command is currently alpha.

```
kubeadm alpha phase addon all [flags]
```

### Examples

```
  # Installs the CoreDNS and the kube-proxy addons components via the API server,
  # functionally equivalent to what installed by kubeadm init.
  
  kubeadm alpha phase selfhosting from-staticpods
```

### Options

```
      --apiserver-advertise-address string   The IP address the API server is accessible on
      --apiserver-bind-port int32            The port the API server is accessible on (default 6443)
      --config string                        Path to a kubeadm config file. WARNING: Usage of a configuration file is experimental
      --feature-gates string                 A set of key=value pairs that describe feature gates for various features. Options are:
                                             Auditing=true|false (ALPHA - default=false)
                                             CoreDNS=true|false (default=true)
                                             DynamicKubeletConfig=true|false (BETA - default=false)
  -h, --help                                 help for all
      --image-repository string              Choose a container registry to pull control plane images from (default "k8s.gcr.io")
      --kubeconfig string                    The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/etc/kubernetes/admin.conf")
      --kubernetes-version string            Choose a specific Kubernetes version for the control plane (default "stable-1")
      --pod-network-cidr string              The range of IP addresses used for the Pod network
      --service-cidr string                  The range of IP address used for service VIPs (default "10.96.0.0/12")
      --service-dns-domain string            Alternative domain for services (default "cluster.local")
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

