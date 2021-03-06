
Uploads the currently used configuration for kubeadm to a ConfigMap

### Synopsis

Uploads the kubeadm init configuration of your cluster to a ConfigMap called kubeadm-config in the kube-system namespace. This enables correct configuration of system components and a seamless user experience when upgrading. 

Alternatively, you can use kubeadm config. 

Alpha Disclaimer: this command is currently alpha.

```
kubeadm alpha phase upload-config [flags]
```

### Examples

```
  # uploads the configuration of your cluster
  kubeadm alpha phase upload-config --config=myConfig.yaml
```

### Options

```
      --config string       Path to a kubeadm config file. WARNING: Usage of a configuration file is experimental
  -h, --help                help for upload-config
      --kubeconfig string   The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/etc/kubernetes/admin.conf")
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

