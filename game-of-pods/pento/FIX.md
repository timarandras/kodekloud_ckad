# Fixing API-server
`--client-ca-file=/etc/kubernetes/pki/ca.crt`

# Fix CoreDNS image version
`k -n kube-system edit deployments.apps coredns`

- Change image (kubedns:x.x.x) to coredns:1.6.7
- Deployment will automatically restart.

# Make node01 schedule pods
- uncordon node01 by `k uncordon node01`

