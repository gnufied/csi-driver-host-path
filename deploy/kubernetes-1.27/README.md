The deployment for Kubernetes 1.21 uses the CSI snapshotter sidecar
4.x and thus is incompatible with Kubernetes clusters where older
snapshotter CRDs are installed.

The health-monitor-agent is no longer getting deployed because its
functionality was moved into kubelet in Kubernetes 1.21.


** TO deploy custom snapshotter **

export CSI_SNAPSHOTTER_RBAC="https://raw.githubusercontent.com/kubernetes-csi/external-snapshotter/refs/heads/master/deploy/kubernetes/csi-snapshotter/rbac-csi-snapshotter.yaml"
./deploy.sh
