
Delete bootstrap tokens on the server.

### Synopsis


This command will delete a given bootstrap token for you.

The [token-value] is the full Token of the form "[a-z0-9]{6}.[a-z0-9]{16}" or the
Token ID of the form "[a-z0-9]{6}" to delete.


```
kubeadm token delete [token-value]
```

### Options

```
  -h, --help   help for delete
```

### Options inherited from parent commands

```
      --dry-run             Whether to enable dry-run mode or not
      --kubeconfig string   The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/etc/kubernetes/admin.conf")
      --rootfs string       [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

