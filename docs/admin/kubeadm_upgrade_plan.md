
Check which versions are available to upgrade to and validate whether your current cluster is upgradeable. To skip the internet check, pass in the optional [version] parameter.

### Synopsis

Check which versions are available to upgrade to and validate whether your current cluster is upgradeable. To skip the internet check, pass in the optional [version] parameter.

```
kubeadm upgrade plan [version] [flags]
```

### Options

```
      --allow-experimental-upgrades        Show unstable versions of Kubernetes as an upgrade alternative and allow upgrading to an alpha/beta/release candidate versions of Kubernetes.
      --allow-release-candidate-upgrades   Show release candidate versions of Kubernetes as an upgrade alternative and allow upgrading to a release candidate versions of Kubernetes.
      --config string                      Path to kubeadm config file (WARNING: Usage of a configuration file is experimental)
      --feature-gates string               A set of key=value pairs that describe feature gates for various features. Options are:
                                           Auditing=true|false (ALPHA - default=false)
                                           CoreDNS=true|false (default=true)
                                           DynamicKubeletConfig=true|false (BETA - default=false)
  -h, --help                               help for plan
      --ignore-preflight-errors strings    A list of checks whose errors will be shown as warnings. Example: 'IsPrivilegedUser,Swap'. Value 'all' ignores errors from all checks.
      --kubeconfig string                  The KubeConfig file to use when talking to the cluster. If the flag is not set, a set of standard locations are searched for an existing KubeConfig file. (default "/Users/vici/.kube/config")
      --print-config                       Specifies whether the configuration file that will be used in the upgrade should be printed or not.
```

### Options inherited from parent commands

```
      --rootfs string   [EXPERIMENTAL] The path to the 'real' host root filesystem.
```

