## kubectl create clusterrole

Create a ClusterRole.

### Synopsis

Create a ClusterRole.

```
kubectl create clusterrole NAME --verb=verb --resource=resource.group [--resource-name=resourcename] [--dry-run]
```

### Examples

```
  # Create a ClusterRole named "pod-reader" that allows user to perform "get", "watch" and "list" on pods
  kubectl create clusterrole pod-reader --verb=get,list,watch --resource=pods
  
  # Create a ClusterRole named "pod-reader" with ResourceName specified
  kubectl create clusterrole pod-reader --verb=get --resource=pods --resource-name=readablepod --resource-name=anotherpod
  
  # Create a ClusterRole named "foo" with API Group specified
  kubectl create clusterrole foo --verb=get,list,watch --resource=rs.extensions
  
  # Create a ClusterRole named "foo" with SubResource specified
  kubectl create clusterrole foo --verb=get,list,watch --resource=pods,pods/status
  
  # Create a ClusterRole name "foo" with NonResourceURL specified
  kubectl create clusterrole "foo" --verb=get --non-resource-url=/logs/*
  
  # Create a ClusterRole name "monitoring" with AggregationRule specified
  kubectl create clusterrole monitoring --aggregation-rule="rbac.example.com/aggregate-to-monitoring=true"
```

### Options

```
      --aggregation-rule mapStringString   An aggregation label selector for combining ClusterRoles.
      --allow-missing-template-keys        If true, ignore any errors in templates when a field or map key is missing in the template. Only applies to golang and jsonpath output formats. (default true)
      --dry-run                            If true, only print the object that would be sent, without sending it.
  -h, --help                               help for clusterrole
      --non-resource-url strings           A partial url that user should have access to.
  -o, --output string                      Output format. One of: json|yaml|name|templatefile|template|go-template|go-template-file|jsonpath|jsonpath-file.
      --resource strings                   Resource that the rule applies to
      --resource-name stringArray          Resource in the white list that the rule applies to, repeat this flag for multiple items
      --save-config                        If true, the configuration of current object will be saved in its annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to perform kubectl apply on this object in the future.
      --template string                    Template string or path to template file to use when -o=go-template, -o=go-template-file. The template format is golang templates [http://golang.org/pkg/text/template/#pkg-overview].
      --validate                           If true, use a schema to validate the input before sending it (default true)
      --verb strings                       Verb that applies to the resources contained in the rule
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --as string                        Username to impersonate for the operation
      --as-group stringArray             Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --cache-dir string                 Default HTTP cache directory (default "/Users/vici/.kube/http-cache")
      --certificate-authority string     Path to a cert file for the certificate authority
      --client-certificate string        Path to a client certificate file for TLS
      --client-key string                Path to a client key file for TLS
      --cluster string                   The name of the kubeconfig cluster to use
      --context string                   The name of the kubeconfig context to use
      --insecure-skip-tls-verify         If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string                Path to the kubeconfig file to use for CLI requests.
      --log-backtrace-at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log-dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files
      --match-server-version             Require server version to match client version
  -n, --namespace string                 If present, the namespace scope for this CLI request
      --request-timeout string           The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
  -s, --server string                    The address and port of the Kubernetes API server
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
      --token string                     Bearer token for authentication to the API server
      --user string                      The name of the kubeconfig user to use
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kubectl create](kubectl_create.md)	 - Create a resource from a file or from stdin.

###### Auto generated by spf13/cobra on 15-Nov-2018
