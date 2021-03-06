# Ingress Controller Command-line Arguments

```
Usage of ./nginx-ingress:
  -alsologtostderr
    	log to standard error as well as files
  -default-server-tls-secret string
    	A Secret with a TLS certificate and key for TLS termination of the default server. Format: <namespace>/<name>.
	If not set, certificate and key in the file "/etc/nginx/secrets/default" are used. If a secret is set,
	but the Ingress controller is not able to fetch it from Kubernetes API or a secret is not set and
	the file "/etc/nginx/secrets/default" does not exist, the Ingress controller will fail to start
  -health-status
    	Add a location "/nginx-health" to the default server. The location responds with the 200 status code for any request.
	Useful for external health-checking of the Ingress controller
  -ingress-class string
    	A class of the Ingress controller. The Ingress controller only processes Ingress resources that belong to its class
	- i.e. have the annotation "kubernetes.io/ingress.class" equal to the class. Additionally,
	the Ingress controller processes Ingress resources that do not have that annotation,
	which can be disabled by setting the "-use-ingress-class-only" flag (default "nginx")
  -log_backtrace_at value
    	when logging hits line file:N, emit a stack trace
  -log_dir string
    	If non-empty, write log files in this directory
  -logtostderr
    	log to standard error instead of files
  -nginx-configmaps string
    	A ConfigMap resource for customizing NGINX configuration. If a ConfigMap is set,
	but the Ingress controller is not able to fetch it from Kubernetes API, the Ingress controller will fail to start.
	Format: <namespace>/<name>
  -nginx-plus
    	Enable support for NGINX Plus
  -proxy string
    	Use a proxy server to connect to Kubernetes API started by "kubectl proxy" command. For testing purposes only.
	The Ingress controller does not start NGINX and does not write any generated NGINX configuration files to disk
  -stderrthreshold value
    	logs at or above this threshold go to stderr
  -use-ingress-class-only
    	Ignore Ingress resources without the "kubernetes.io/ingress.class" annotation
  -v value
    	log level for V logs
  -version
    	Print the version and git-commit hash and exit
  -vmodule value
    	comma-separated list of pattern=N settings for file-filtered logging
  -watch-namespace string
    	Namespace to watch for Ingress resources. By default the Ingress controller watches all namespaces
```