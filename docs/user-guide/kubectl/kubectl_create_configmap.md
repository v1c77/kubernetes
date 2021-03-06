## kubectl create configmap

Create a configmap from a local file, directory or literal value

### Synopsis

Create a configmap based on a file, directory, or specified literal value. 

A single configmap may package one or more key/value pairs. 

When creating a configmap based on a file, the key will default to the basename of the file, and the value will default to the file content.  If the basename is an invalid key, you may specify an alternate key. 

When creating a configmap based on a directory, each file whose basename is a valid key in the directory will be packaged into the configmap.  Any directory entries except regular files are ignored (e.g. subdirectories, symlinks, devices, pipes, etc).

```
kubectl create configmap NAME [--from-file=[key=]source] [--from-literal=key1=value1] [--dry-run]
```

### Examples

```
  # Create a new configmap named my-config based on folder bar
  kubectl create configmap my-config --from-file=path/to/bar
  
  # Create a new configmap named my-config with specified keys instead of file basenames on disk
  kubectl create configmap my-config --from-file=key1=/path/to/bar/file1.txt --from-file=key2=/path/to/bar/file2.txt
  
  # Create a new configmap named my-config with key1=config1 and key2=config2
  kubectl create configmap my-config --from-literal=key1=config1 --from-literal=key2=config2
  
  # Create a new configmap named my-config from the key=value pairs in the file
  kubectl create configmap my-config --from-file=path/to/bar
  
  # Create a new configmap named my-config from an env file
  kubectl create configmap my-config --from-env-file=path/to/bar.env
```

### Options

```
      --allow-missing-template-keys   If true, ignore any errors in templates when a field or map key is missing in the template. Only applies to golang and jsonpath output formats. (default true)
      --append-hash                   Append a hash of the configmap to its name.
      --dry-run                       If true, only print the object that would be sent, without sending it.
      --from-env-file string          Specify the path to a file to read lines of key=val pairs to create a configmap (i.e. a Docker .env file).
      --from-file strings             Key file can be specified using its file path, in which case file basename will be used as configmap key, or optionally with a key and file path, in which case the given key will be used.  Specifying a directory will iterate each named file in the directory whose basename is a valid configmap key.
      --from-literal stringArray      Specify a key and literal value to insert in configmap (i.e. mykey=somevalue)
      --generator string              The name of the API generator to use. (default "configmap/v1")
  -h, --help                          help for configmap
  -o, --output string                 Output format. One of: json|yaml|name|template|go-template|go-template-file|templatefile|jsonpath|jsonpath-file.
      --save-config                   If true, the configuration of current object will be saved in its annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to perform kubectl apply on this object in the future.
      --template string               Template string or path to template file to use when -o=go-template, -o=go-template-file. The template format is golang templates [http://golang.org/pkg/text/template/#pkg-overview].
      --validate                      If true, use a schema to validate the input before sending it (default true)
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
