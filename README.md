# etcd

Setup an [`etcd`](https://coreos.com/etcd/docs/latest/) instance.

## Preconditions

Debian stretch doesn't offer a package for `etcd`. Make sure to install a
repository on the target host which contains the `etcd` package before applying
this role.

## Configuration

| Variable name | Default value | Description |
|---------------|---------------|-------------|
| `etcd_ip` | `127.0.0.1` | The address to run this instance on |
| `etcd_cluster_token` | `etcd-cluster` | The token to use for this cluster |
| `etcd_tls` | `False` | Connect clients and peers via TLS |
| `etcd_peer_ca` | `''` | Path to the file containing the key. Required for
`etcd_tls` |
| `etcd_peer_cert` | `''` | " |
| `etcd_peer_key` | `''` | " |
| `etcd_client_ca` | `''` | " |
| `etcd_client_cert` | `''` | " |
| `etcd_client_key` | `''` | " |
| `etcd_peers` | `[]` | The list of peers with a custom `name` and `ip` set |
