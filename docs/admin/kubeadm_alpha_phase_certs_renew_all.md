
renew all available certificates

### Synopsis

Renews all known certificates necessary to run the control plan. Renewals are run unconditionally, regardless of expiration date. Renewals can also be run individually for more control.

```
kubeadm alpha phase certs renew all [flags]
```

### Options

```
      --cert-dir string     The path where to save the certificates (default "/etc/kubernetes/pki")
      --config string       Path to kubeadm config file (WARNING: Usage of a configuration file is experimental)
  -h, --help                help for all
      --kubeconfig string   The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/etc/kubernetes/admin.conf")
      --use-api             Use the Kubernetes certificate API to renew certificates
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

