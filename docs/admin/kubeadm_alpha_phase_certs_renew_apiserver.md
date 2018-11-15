
Generates the certificate for serving the kubernetes API

### Synopsis

Renews the certificate for serving the kubernetes API, and saves them into apiserver.cert and apiserver.key files. 

Extra attributes such as SANs will be based on the existing certificates, there is no need to resupply them.

```
kubeadm alpha phase certs renew apiserver [flags]
```

### Options

```
      --cert-dir string     The path where to save the certificates (default "/etc/kubernetes/pki")
      --config string       Path to kubeadm config file (WARNING: Usage of a configuration file is experimental)
  -h, --help                help for apiserver
      --kubeconfig string   The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/etc/kubernetes/admin.conf")
      --use-api             Use the Kubernetes certificate API to renew certificates
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

