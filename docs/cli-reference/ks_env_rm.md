## ks env rm

Delete an environment from a ksonnet project

### Synopsis


Delete an environment from a ksonnet project. This is the same
as removing the <env-name> environment directory and all files contained. If the
project exists in a hierarchy (e.g., 'us-east/staging') and deleting the
environment results in an empty environments directory (e.g., if deleting
'us-east/staging' resulted in an empty 'us-east/' directory), then all empty
parent directories are subsequently deleted.

```
ks env rm <env-name>
```

### Examples

```
  # Remove the directory 'us-west/staging' and all contents
  #	in the 'environments' directory. This will also remove the parent directory
  # 'us-west' if it is empty.
  ks env rm us-west/staging
```

### Options inherited from parent commands

```
      --as string                      Username to impersonate for the operation
      --certificate-authority string   Path to a cert. file for the certificate authority
      --client-certificate string      Path to a client certificate file for TLS
      --client-key string              Path to a client key file for TLS
      --cluster string                 The name of the kubeconfig cluster to use
      --context string                 The name of the kubeconfig context to use
      --insecure-skip-tls-verify       If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string              Path to a kube config. Only required if out-of-cluster
  -n, --namespace string               If present, the namespace scope for this CLI request
      --password string                Password for basic authentication to the API server
      --request-timeout string         The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
      --server string                  The address and port of the Kubernetes API server
      --token string                   Bearer token for authentication to the API server
      --user string                    The name of the kubeconfig user to use
      --username string                Username for basic authentication to the API server
  -v, --verbose count[=-1]             Increase verbosity. May be given multiple times.
```

### SEE ALSO
* [ks env](ks_env.md)	 - Manage ksonnet environments
