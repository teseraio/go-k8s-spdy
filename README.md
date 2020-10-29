
# Go-k8s-api

Go-k8s-api is a helper library to interact with the SPDY protocol in Kubernetes. This code is based on the official go-client library for Kubernetes.

Usage:

```
remoteCommand := spdy.RemoteCommand{
	URL:       "https://.../pods/redis",
	TLSConfig: tlsConf,
}
args := &spdy.Args{
	Container: "redis",
    Command:   []string{"redis-cli", "info"},
}
out, err := remoteCommand.Execute(args)
if err != nil {
	panic(err)
}
fmt.Println(string(out))
```
