
Generates the client certificate for liveness probes to healtcheck etcd

### Synopsis

Generates the client certificate for liveness probes to healtcheck etcd, and saves them into etcd/healthcheck-client.cert and etcd/healthcheck-client.key files. 

If both files already exist, kubeadm skips the generation step and existing files will be used. 

Alpha Disclaimer: this command is currently alpha.

```
kubeadm alpha phase certs etcd-healthcheck-client [flags]
```

### Options

```
      --cert-dir string   The path where to save the certificates (default "/etc/kubernetes/pki")
      --config string     Path to kubeadm config file (WARNING: Usage of a configuration file is experimental)
  -h, --help              help for etcd-healthcheck-client
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

