<!-- BEGIN MUNGE: GENERATED_TOC -->
- [v1.8.8](#v188)
  - [Changelog since v1.8.7](#changelog-since-v187)
    - [Other notable changes](#other-notable-changes)
- [v1.8.7](#v187)
  - [Changelog since v1.8.6](#changelog-since-v186)
    - [Other notable changes](#other-notable-changes-1)
- [v1.8.6](#v186)
  - [Changelog since v1.8.5](#changelog-since-v185)
    - [Other notable changes](#other-notable-changes-2)
- [v1.8.5](#v185)
  - [Changelog since v1.8.4](#changelog-since-v184)
    - [Other notable changes](#other-notable-changes-3)
- [v1.8.4](#v184)
  - [Changelog since v1.8.3](#changelog-since-v183)
    - [Other notable changes](#other-notable-changes-4)
- [v1.8.3](#v183)
  - [Changelog since v1.8.2](#changelog-since-v182)
    - [Other notable changes](#other-notable-changes-5)
- [v1.8.2](#v182)
  - [Changelog since v1.8.1](#changelog-since-v181)
    - [Other notable changes](#other-notable-changes-6)
- [v1.8.1](#v181)
  - [Changelog since v1.8.0](#changelog-since-v180)
    - [Action Required](#action-required)
    - [Other notable changes](#other-notable-changes-7)
- [v1.8.0](#v180)
  - [Introduction to v1.8.0](#introduction-to-v180)
  - [Major Themes](#major-themes)
    - [SIG API Machinery](#sig-api-machinery)
    - [SIG Apps](#sig-apps)
    - [SIG Auth](#sig-auth)
    - [SIG Autoscaling](#sig-autoscaling)
    - [SIG Cluster Lifecycle](#sig-cluster-lifecycle)
    - [SIG Instrumentation](#sig-instrumentation)
    - [SIG Multi-cluster (formerly known as SIG Federation)](#sig-multi-cluster-formerly-known-as-sig-federation)
    - [SIG Node](#sig-node)
    - [SIG Network](#sig-network)
    - [SIG Scalability](#sig-scalability)
    - [SIG Scheduling](#sig-scheduling)
    - [SIG Storage](#sig-storage)
  - [Before Upgrading](#before-upgrading)
  - [Known Issues](#known-issues)
  - [Deprecations](#deprecations)
    - [Apps](#apps)
    - [Auth](#auth)
    - [Autoscaling](#autoscaling)
    - [Cluster Lifecycle](#cluster-lifecycle)
    - [OpenStack](#openstack)
    - [Scheduling](#scheduling)
  - [Notable Features](#notable-features)
    - [Workloads API (apps/v1beta2)](#workloads-api-appsv1beta2)
      - [API Object Additions and Migrations](#api-object-additions-and-migrations)
      - [Behavioral Changes](#behavioral-changes)
      - [Defaults](#defaults)
    - [Workloads API (batch)](#workloads-api-batch)
      - [CLI Changes](#cli-changes)
      - [Scheduling](#scheduling-1)
      - [Storage](#storage)
    - [Cluster Federation](#cluster-federation)
      - [[alpha] Federated Jobs](#alpha-federated-jobs)
      - [[alpha] Federated Horizontal Pod Autoscaling (HPA)](#alpha-federated-horizontal-pod-autoscaling-hpa)
    - [Node Components](#node-components)
      - [Autoscaling and Metrics](#autoscaling-and-metrics)
        - [Cluster Autoscaler](#cluster-autoscaler)
      - [Container Runtime Interface (CRI)](#container-runtime-interface-cri)
      - [kubelet](#kubelet)
    - [Auth](#auth-1)
    - [Cluster Lifecycle](#cluster-lifecycle-1)
      - [kubeadm](#kubeadm)
      - [kops](#kops)
      - [Cluster Discovery/Bootstrap](#cluster-discoverybootstrap)
      - [Multi-platform](#multi-platform)
      - [Cloud Providers](#cloud-providers)
    - [Network](#network)
      - [network-policy](#network-policy)
      - [kube-proxy ipvs mode](#kube-proxy-ipvs-mode)
    - [API Machinery](#api-machinery)
      - [kube-apiserver](#kube-apiserver)
      - [Dynamic Admission Control](#dynamic-admission-control)
      - [Custom Resource Definitions (CRDs)](#custom-resource-definitions-crds)
      - [Garbage Collector](#garbage-collector)
      - [Monitoring/Prometheus](#monitoringprometheus)
      - [Go Client](#go-client)
  - [External Dependencies](#external-dependencies)
- [v1.8.0-rc.1](#v180-rc1)
  - [Changelog since v1.8.0-beta.1](#changelog-since-v180-beta1)
    - [Action Required](#action-required-1)
    - [Other notable changes](#other-notable-changes-8)
- [v1.8.0-beta.1](#v180-beta1)
  - [Changelog since v1.8.0-alpha.3](#changelog-since-v180-alpha3)
    - [Action Required](#action-required-2)
    - [Other notable changes](#other-notable-changes-9)
- [v1.8.0-alpha.3](#v180-alpha3)
  - [Changelog since v1.8.0-alpha.2](#changelog-since-v180-alpha2)
    - [Action Required](#action-required-3)
    - [Other notable changes](#other-notable-changes-10)
- [v1.8.0-alpha.2](#v180-alpha2)
  - [Changelog since v1.7.0](#changelog-since-v170)
    - [Action Required](#action-required-4)
    - [Other notable changes](#other-notable-changes-11)
- [v1.8.0-alpha.1](#v180-alpha1)
  - [Changelog since v1.7.0-alpha.4](#changelog-since-v170-alpha4)
    - [Action Required](#action-required-5)
    - [Other notable changes](#other-notable-changes-12)
<!-- END MUNGE: GENERATED_TOC -->

<!-- NEW RELEASE NOTES ENTRY -->


# v1.8.8

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.7

### Other notable changes

* Configurable etcd quota backend bytes in GCE ([#59259](https://github.com/kubernetes/kubernetes/pull/59259), [@wojtek-t](https://github.com/wojtek-t))
* Cluster Autoscaler 1.0.4 ([#59271](https://github.com/kubernetes/kubernetes/pull/59271), [@mwielgus](https://github.com/mwielgus))
* Prevent kubelet from getting wedged if initialization of modules returns an error. ([#59020](https://github.com/kubernetes/kubernetes/pull/59020), [@brendandburns](https://github.com/brendandburns))
* Updates Calico version to v2.6.7 (Fixed a bug where Felix would crash when parsing a NetworkPolicy with a named port. See https://github.com/projectcalico/calico/releases/tag/v2.6.7) ([#59130](https://github.com/kubernetes/kubernetes/pull/59130), [@caseydavenport](https://github.com/caseydavenport))
* Configurable etcd compaction frequency in GCE ([#59106](https://github.com/kubernetes/kubernetes/pull/59106), [@wojtek-t](https://github.com/wojtek-t))
* [GCE] Apiserver uses `InternalIP` as the most preferred kubelet address type by default. ([#59019](https://github.com/kubernetes/kubernetes/pull/59019), [@MrHohn](https://github.com/MrHohn))
* Updated priority of mirror pod according to PriorityClassName. ([#58485](https://github.com/kubernetes/kubernetes/pull/58485), [@k82cn](https://github.com/k82cn))
* Fix kubelet to correctly umounts mount points for glusterfs when transport endpoint is not connected and nfs when there is a stale file handle ([#58660](https://github.com/kubernetes/kubernetes/pull/58660), [@humblec](https://github.com/humblec))
* Detach and clear bad disk URI ([#58345](https://github.com/kubernetes/kubernetes/pull/58345), [@rootfs](https://github.com/rootfs))
* Expose Metrics Server metrics via /metric endpoint. ([#57456](https://github.com/kubernetes/kubernetes/pull/57456), [@kawych](https://github.com/kawych))
* Access to externally managed IP addresses via the kube-apiserver service proxy subresource is no longer allowed by default. This can be re-enabled via the `ServiceProxyAllowExternalIPs` feature gate, but will be disallowed completely in 1.11 ([#57265](https://github.com/kubernetes/kubernetes/pull/57265), [@brendandburns](https://github.com/brendandburns))
* Add apiserver metric for number of requests dropped because of inflight limit. ([#58340](https://github.com/kubernetes/kubernetes/pull/58340), [@gmarek](https://github.com/gmarek))
* Add apiserver metric for current inflight-request usage. ([#58342](https://github.com/kubernetes/kubernetes/pull/58342), [@gmarek](https://github.com/gmarek))
* Update Calico version to v2.6.6 ([#58482](https://github.com/kubernetes/kubernetes/pull/58482), [@tmjd](https://github.com/tmjd))
* Correctly handle transient connection reset errors on GET requests from client library. ([#58520](https://github.com/kubernetes/kubernetes/pull/58520), [@porridge](https://github.com/porridge))
* Fixes an issue where the resourceVersion of an object in a DELETE watch event was not the resourceVersion of the delete itself, but of the last update to the object. This could disrupt the ability of clients clients to re-establish watches properly. ([#58547](https://github.com/kubernetes/kubernetes/pull/58547), [@liggitt](https://github.com/liggitt))
* Fix a bug affecting nested data volumes such as secret, configmap, etc. ([#57422](https://github.com/kubernetes/kubernetes/pull/57422), [@joelsmith](https://github.com/joelsmith))
* Fix garbage collection and resource quota when the controller-manager uses --leader-elect=false ([#57340](https://github.com/kubernetes/kubernetes/pull/57340), [@jmcmeek](https://github.com/jmcmeek))
* Fixed encryption key and encryption provider rotation ([#58375](https://github.com/kubernetes/kubernetes/pull/58375), [@liggitt](https://github.com/liggitt))



# v1.8.7

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.6

### Other notable changes

* fix device name change issue for azure disk: add remount logic ([#57953](https://github.com/kubernetes/kubernetes/pull/57953), [@andyzhangx](https://github.com/andyzhangx))
* GCE: Allows existing internal load balancers to continue using an outdated subnetwork  ([#57861](https://github.com/kubernetes/kubernetes/pull/57861), [@nicksardo](https://github.com/nicksardo))
* fix azure disk not available issue when device name changed ([#57549](https://github.com/kubernetes/kubernetes/pull/57549), [@andyzhangx](https://github.com/andyzhangx))
* Allow kubernetes components to react to SIGTERM signal and shutdown gracefully. ([#57756](https://github.com/kubernetes/kubernetes/pull/57756), [@mborsz](https://github.com/mborsz))
* fix incorrect error info when creating an azure file PVC failed ([#56550](https://github.com/kubernetes/kubernetes/pull/56550), [@andyzhangx](https://github.com/andyzhangx))
* GCE: Fixes ILB creation on automatic networks with manually created subnetworks. ([#57351](https://github.com/kubernetes/kubernetes/pull/57351), [@nicksardo](https://github.com/nicksardo))
* Configurable liveness probe initial delays for etcd and kube-apiserver in GCE ([#57749](https://github.com/kubernetes/kubernetes/pull/57749), [@wojtek-t](https://github.com/wojtek-t))
* Fixes a bug where if an error was returned that was not an `autorest.DetailedError` we would return `"not found", nil` which caused nodes to go to `NotReady` state. ([#57484](https://github.com/kubernetes/kubernetes/pull/57484), [@brendandburns](https://github.com/brendandburns))



# v1.8.6

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.5

### Other notable changes

* change default azure file/dir mode to 0755 ([#56551](https://github.com/kubernetes/kubernetes/pull/56551), [@andyzhangx](https://github.com/andyzhangx))
* Retry 'connection refused' errors when setting up clusters on GCE. ([#57394](https://github.com/kubernetes/kubernetes/pull/57394), [@mborsz](https://github.com/mborsz))
* enable flexvolume on Windows node ([#56921](https://github.com/kubernetes/kubernetes/pull/56921), [@andyzhangx](https://github.com/andyzhangx))
* Add prometheus metrics for the PodSecurityPolicy admission controller ([#57346](https://github.com/kubernetes/kubernetes/pull/57346), [@tallclair](https://github.com/tallclair))
* fix CreateVolume func: use search mode instead ([#54687](https://github.com/kubernetes/kubernetes/pull/54687), [@andyzhangx](https://github.com/andyzhangx))
* remove time waiting after create storage account (save 25s) ([#56679](https://github.com/kubernetes/kubernetes/pull/56679), [@andyzhangx](https://github.com/andyzhangx))
* Add pvc as part of equivalence hash ([#56577](https://github.com/kubernetes/kubernetes/pull/56577), [@resouer](https://github.com/resouer))
* fix azure disk storage account init issue ([#55927](https://github.com/kubernetes/kubernetes/pull/55927), [@andyzhangx](https://github.com/andyzhangx))
* falls back to parse Docker runtime version as generic if not semver ([#54040](https://github.com/kubernetes/kubernetes/pull/54040), [@dixudx](https://github.com/dixudx))
* BUG FIX: Check both name and ports for azure health probes ([#56918](https://github.com/kubernetes/kubernetes/pull/56918), [@feiskyer](https://github.com/feiskyer))



# v1.8.5

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.4

### Other notable changes

* Fix scheduler cache panic when updating pod conditions. ([#56731](https://github.com/kubernetes/kubernetes/pull/56731), [@bsalamat](https://github.com/bsalamat))
* Add new Prometheus metric that monitors the remaining lifetime of certificates used to authenticate requests to the API server. ([#50387](https://github.com/kubernetes/kubernetes/pull/50387), [@jcbsmpsn](https://github.com/jcbsmpsn))
* scheduler: Fix issue were a new pod with affinity gets stuck at `creating` because the node had been deleted but the pod still exists. ([#56835](https://github.com/kubernetes/kubernetes/pull/56835), [@wenlxie](https://github.com/wenlxie))
* Updated Dashboard add-on to version 1.8.0: The Dashboard add-on now deploys with https enabled. The Dashboard can be accessed via kubectl proxy at http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/. The /ui redirect is deprecated and will be removed in 1.10. ([#53046](https://github.com/kubernetes/kubernetes/pull/53046), [@maciaszczykm](https://github.com/maciaszczykm))
* Fix issue where masquerade rules are flushed in GCE k8s clusters. ([#56729](https://github.com/kubernetes/kubernetes/pull/56729), [@dnardo](https://github.com/dnardo))
* kubelet: Fix bug where `runAsUser: MustRunAsNonRoot` strategy didn't reject a pod with a non-numeric `USER`. ([#56708](https://github.com/kubernetes/kubernetes/pull/56708), [@php-coder](https://github.com/php-coder))
* Add iptables rules to allow Pod traffic even when default iptables policy is to reject. ([#52569](https://github.com/kubernetes/kubernetes/pull/52569), [@tmjd](https://github.com/tmjd))
* Fix a bug in GCE multizonal clusters where PersistentVolumes were sometimes created in zones without nodes. ([#52322](https://github.com/kubernetes/kubernetes/pull/52322), [@davidz627](https://github.com/davidz627))
* If a non-absolute mountPath is passed to the kubelet, prefix it with the appropriate root path. ([#55665](https://github.com/kubernetes/kubernetes/pull/55665), [@brendandburns](https://github.com/brendandburns))
* add GRS, RAGRS storage account type support for azure disk ([#55931](https://github.com/kubernetes/kubernetes/pull/55931), [@andyzhangx](https://github.com/andyzhangx))
* Fix a typo in prometheus-to-sd configuration, that drops some stackdriver metrics. ([#56473](https://github.com/kubernetes/kubernetes/pull/56473), [@loburm](https://github.com/loburm))
* Fixes server name verification of aggregated API servers and webhook admission endpoints ([#56415](https://github.com/kubernetes/kubernetes/pull/56415), [@liggitt](https://github.com/liggitt))
* Update jquery and bootstrap dependencies ([#56445](https://github.com/kubernetes/kubernetes/pull/56445), [@dashpole](https://github.com/dashpole))
* Fix CRI localhost seccomp path in format localhost//profileRoot/profileName. ([#55450](https://github.com/kubernetes/kubernetes/pull/55450), [@feiskyer](https://github.com/feiskyer))
* support mount options in azure file ([#54674](https://github.com/kubernetes/kubernetes/pull/54674), [@andyzhangx](https://github.com/andyzhangx))
* kube-apiserver: fixed --oidc-username-prefix and --oidc-group-prefix flags which previously weren't correctly enabled ([#56175](https://github.com/kubernetes/kubernetes/pull/56175), [@ericchiang](https://github.com/ericchiang))
* fluentd-gcp addon: Fix fluentd deployment on GCP when custom resources are set. ([#55950](https://github.com/kubernetes/kubernetes/pull/55950), [@crassirostris](https://github.com/crassirostris))
* API discovery failures no longer crash the kube controller manager via the garbage collector. ([#55259](https://github.com/kubernetes/kubernetes/pull/55259), [@ironcladlou](https://github.com/ironcladlou))
* Fix bug where master startup script on GCP failed randomly due to concurrent iptables invocations. ([#55945](https://github.com/kubernetes/kubernetes/pull/55945), [@x13n](https://github.com/x13n))



# v1.8.4

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.3

### Other notable changes

* Cluster Autoscaler 1.0.3 ([#55947](https://github.com/kubernetes/kubernetes/pull/55947), [@aleksandra-malinowska](https://github.com/aleksandra-malinowska))
* - Add PodSecurityPolicies for cluster addons ([#55509](https://github.com/kubernetes/kubernetes/pull/55509), [@tallclair](https://github.com/tallclair))
    * - Remove SSL cert HostPath volumes from heapster addons
* Fix session affinity issue with external load balancer traffic when ExternalTrafficPolicy=Local. ([#55519](https://github.com/kubernetes/kubernetes/pull/55519), [@MrHohn](https://github.com/MrHohn))
* Addon manager supports HA masters. ([#55782](https://github.com/kubernetes/kubernetes/pull/55782), [@x13n](https://github.com/x13n))
* ScaleIO persistent volumes now support referencing a secret in a namespace other than the bound persistent volume claim's namespace; this is controlled during provisioning with the `secretNamespace` storage class parameter; StoragePool and ProtectionDomain attributes no longer defaults to the value `default` ([#54013](https://github.com/kubernetes/kubernetes/pull/54013), [@vladimirvivien](https://github.com/vladimirvivien))
* Allow HPA to read custom metrics. ([#54854](https://github.com/kubernetes/kubernetes/pull/54854), [@kawych](https://github.com/kawych))
* Add masquerading rules by default to GCE/GKE ([#55178](https://github.com/kubernetes/kubernetes/pull/55178), [@dnardo](https://github.com/dnardo))
* kubeadm now produces error during preflight checks if swap is enabled. Users, who can setup kubelet to run in unsupported environment with enabled swap, will be able to skip that preflight check. ([#55399](https://github.com/kubernetes/kubernetes/pull/55399), [@kad](https://github.com/kad))
* GCE: provide an option to disable docker's live-restore on COS/ubuntu ([#55260](https://github.com/kubernetes/kubernetes/pull/55260), [@yujuhong](https://github.com/yujuhong))
* Fix hyperkube kubelet --experimental-dockershim ([#55250](https://github.com/kubernetes/kubernetes/pull/55250), [@ivan4th](https://github.com/ivan4th))
* ScaleIO driver completely removes dependency on drv_cfg binary so a Kubernetes cluster can easily run a containerized kubelet. ([#54956](https://github.com/kubernetes/kubernetes/pull/54956), [@vladimirvivien](https://github.com/vladimirvivien))



# v1.8.3

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.2

### Other notable changes

* Fixed 'Schedulercache is corrupted' error in kube-scheduler ([#55262](https://github.com/kubernetes/kubernetes/pull/55262), [@liggitt](https://github.com/liggitt))
* Add support for PodSecurityPolicy on GCE: `ENABLE_POD_SECURITY_POLICY=true` enables the admission controller, and installs policies for default addons. ([#52367](https://github.com/kubernetes/kubernetes/pull/52367), [@tallclair](https://github.com/tallclair))
* Azure cloudprovider: Fix controller manager crash issue on a manually created k8s cluster. ([#53694](https://github.com/kubernetes/kubernetes/pull/53694), [@andyzhangx](https://github.com/andyzhangx))
* Cluster Autoscaler 1.0.2 ([#55161](https://github.com/kubernetes/kubernetes/pull/55161), [@mwielgus](https://github.com/mwielgus))
* - fluentd-gcp runs with a dedicated fluentd-gcp service account ([#54175](https://github.com/kubernetes/kubernetes/pull/54175), [@tallclair](https://github.com/tallclair))
    * - Stop mounting the host certificates into fluentd's prometheus-to-sd container
* Fix a bug where pod address is not removed from endpoints object while pod is in graceful termination. ([#54828](https://github.com/kubernetes/kubernetes/pull/54828), [@freehan](https://github.com/freehan))
* fix warning messages due to GetMountRefs func not implemented in windows ([#52401](https://github.com/kubernetes/kubernetes/pull/52401), [@andyzhangx](https://github.com/andyzhangx))
* allow windows mount path ([#51240](https://github.com/kubernetes/kubernetes/pull/51240), [@andyzhangx](https://github.com/andyzhangx))
* Reduce log noise produced by prometheus-to-sd, by bumping it to version 0.2.2. ([#54635](https://github.com/kubernetes/kubernetes/pull/54635), [@loburm](https://github.com/loburm))
* Fix clustered datastore name to be absolute. ([#54438](https://github.com/kubernetes/kubernetes/pull/54438), [@pshahzeb](https://github.com/pshahzeb))
* Fix `kubeadm upgrade plan` for offline operation: ignore errors when trying to fetch latest versions from dl.k8s.io ([#54016](https://github.com/kubernetes/kubernetes/pull/54016), [@praseodym](https://github.com/praseodym))
* Add openssh-client back into the hyperkube image. This allows the gitRepo volume plugin to work properly. ([#54250](https://github.com/kubernetes/kubernetes/pull/54250), [@ixdy](https://github.com/ixdy))
* Fix an issue where pods were briefly transitioned to a "Pending" state during the deletion process. ([#54593](https://github.com/kubernetes/kubernetes/pull/54593), [@dashpole](https://github.com/dashpole))
* Add a label which prevents a node from being added to a cloud load balancer ([#53146](https://github.com/kubernetes/kubernetes/pull/53146), [@brendandburns](https://github.com/brendandburns))
* Add a new feature gate for enabling an alpha annotation which, if present, excludes the annotated node from being added to a service load balancers. ([#54644](https://github.com/kubernetes/kubernetes/pull/54644), [@brendandburns](https://github.com/brendandburns))
* Support German cloud for azure disk mount feature ([#50673](https://github.com/kubernetes/kubernetes/pull/50673), [@clement-buchart](https://github.com/clement-buchart))
* Fix overlay2 container disk metrics for Docker and CRI-O ([#54827](https://github.com/kubernetes/kubernetes/pull/54827), [@dashpole](https://github.com/dashpole))
* API machinery's httpstream/spdy calls now support CIDR notation for NO_PROXY ([#54413](https://github.com/kubernetes/kubernetes/pull/54413), [@kad](https://github.com/kad))
* fix a bug where disk pressure could trigger prematurely when using overlay2 ([#53684](https://github.com/kubernetes/kubernetes/pull/53684), [@dashpole](https://github.com/dashpole))
* PodSecurityPolicy: when multiple policies allow a submitted pod, priority is given to ones which do not require any fields in the pod spec to be defaulted. If the pod must be defaulted, the first policy (ordered by name) that allows the pod is used. ([#52849](https://github.com/kubernetes/kubernetes/pull/52849), [@liggitt](https://github.com/liggitt))
* Fixes discovery information for scale subresources in the apps API group ([#54683](https://github.com/kubernetes/kubernetes/pull/54683), [@liggitt](https://github.com/liggitt))
* BugFix: Exited containers are not Garbage Collected by the kubelet while the pod is running ([#53167](https://github.com/kubernetes/kubernetes/pull/53167), [@dashpole](https://github.com/dashpole))
* fix azure pv crash due to volumeSource.ReadOnly value nil ([#54607](https://github.com/kubernetes/kubernetes/pull/54607), [@andyzhangx](https://github.com/andyzhangx))
* kubeadm init: fix a bug that prevented the --token-ttl flag and tokenTTL configuration value from working as expected for infinite (0) values. ([#54640](https://github.com/kubernetes/kubernetes/pull/54640), [@mattmoyer](https://github.com/mattmoyer))
* [fluentd-gcp addon] Fluentd now runs in its own network, not in the host one. ([#54395](https://github.com/kubernetes/kubernetes/pull/54395), [@crassirostris](https://github.com/crassirostris))
* fix azure disk mount failure on coreos and some other distros ([#54334](https://github.com/kubernetes/kubernetes/pull/54334), [@andyzhangx](https://github.com/andyzhangx))
* Fix for service controller so that it won't retry on doNotRetry service update failure. ([#54184](https://github.com/kubernetes/kubernetes/pull/54184), [@MrHohn](https://github.com/MrHohn))
* BulkVerifyVolumes() implementation for vSphere ([#52131](https://github.com/kubernetes/kubernetes/pull/52131), [@BaluDontu](https://github.com/BaluDontu))
* Added option lb-provider to OpenStack cloud provider config ([#54176](https://github.com/kubernetes/kubernetes/pull/54176), [@gonzolino](https://github.com/gonzolino))



# v1.8.2

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.1

### Other notable changes

* Allow for configuring etcd hostname in the manifest ([#54403](https://github.com/kubernetes/kubernetes/pull/54403), [@wojtek-t](https://github.com/wojtek-t))
* Allow standard flags in client-gen. ([#53999](https://github.com/kubernetes/kubernetes/pull/53999), [@sttts](https://github.com/sttts))
* Cluster Autoscaler 1.0.1 ([#54298](https://github.com/kubernetes/kubernetes/pull/54298), [@mwielgus](https://github.com/mwielgus))
* Resolves forbidden error when accessing replicasets and daemonsets via the apps API group ([#54309](https://github.com/kubernetes/kubernetes/pull/54309), [@liggitt](https://github.com/liggitt))
* kubelet: prevent removal of default labels from Node API objects on startup ([#54073](https://github.com/kubernetes/kubernetes/pull/54073), [@liggitt](https://github.com/liggitt))
* Fix a bug that prevents client-go metrics from being registered in prometheus in multiple components. ([#53434](https://github.com/kubernetes/kubernetes/pull/53434), [@crassirostris](https://github.com/crassirostris))
* Webhook always retries connection reset error. ([#53947](https://github.com/kubernetes/kubernetes/pull/53947), [@crassirostris](https://github.com/crassirostris))
* Adjust batching audit webhook default parameters: increase queue size, batch size, and initial backoff. Add throttling to the batching audit webhook. Default rate limit is 10 QPS. ([#53417](https://github.com/kubernetes/kubernetes/pull/53417), [@crassirostris](https://github.com/crassirostris))
* Address a bug which allowed the horizontal pod autoscaler to allocate `desiredReplicas` > `maxReplicas` in certain instances. ([#53690](https://github.com/kubernetes/kubernetes/pull/53690), [@mattjmcnaughton](https://github.com/mattjmcnaughton))
* Fix metrics API group name in audit configuration ([#53493](https://github.com/kubernetes/kubernetes/pull/53493), [@piosz](https://github.com/piosz))
* Use separate client for leader election in scheduler to avoid starving leader election by regular scheduler operations. ([#53793](https://github.com/kubernetes/kubernetes/pull/53793), [@wojtek-t](https://github.com/wojtek-t))
* kubeadm: Strip bootstrap tokens from the `kubeadm-config` ConfigMap ([#53559](https://github.com/kubernetes/kubernetes/pull/53559), [@fabriziopandini](https://github.com/fabriziopandini))



# v1.8.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.0

### Action Required

* PodSecurityPolicy: Fixes a compatibility issue that caused policies that previously allowed privileged pods to start forbidding them, due to an incorrect default value for `allowPrivilegeEscalation`. PodSecurityPolicy objects defined using a 1.8.0 client or server that intended to set `allowPrivilegeEscalation` to `false` must be reapplied after upgrading to 1.8.1. ([#53443](https://github.com/kubernetes/kubernetes/pull/53443), [@liggitt](https://github.com/liggitt))

### Other notable changes

* Fix to prevent downward api change break on older versions ([#53673](https://github.com/kubernetes/kubernetes/pull/53673), [@timothysc](https://github.com/timothysc))
* Ignore extended resources that are not registered with kubelet during container resource allocation. ([#53547](https://github.com/kubernetes/kubernetes/pull/53547), [@jiayingz](https://github.com/jiayingz))
* GCE: Bump GLBC version to [0.9.7](https://github.com/kubernetes/ingress/releases/tag/0.9.7). ([#53625](https://github.com/kubernetes/kubernetes/pull/53625), [@nikhiljindal](https://github.com/nikhiljindal))
* kubeadm 1.8 now properly handles upgrades from to 1.7.x to newer release in 1.7 branch ([#53338](https://github.com/kubernetes/kubernetes/pull/53338), [@kad](https://github.com/kad))
* Add generate-groups.sh and generate-internal-groups.sh to k8s.io/code-generator to easily run generators against CRD or User API Server types. ([#52186](https://github.com/kubernetes/kubernetes/pull/52186), [@sttts](https://github.com/sttts))
* Don't remove extended resource capacities that are not registered with kubelet from node status. ([#53353](https://github.com/kubernetes/kubernetes/pull/53353), [@jiayingz](https://github.com/jiayingz))
* kubeadm allows the kubelets in the cluster to automatically renew their client certificates ([#53252](https://github.com/kubernetes/kubernetes/pull/53252), [@kad](https://github.com/kad))
* Bumped Heapster version to 1.4.3 - more details https://github.com/kubernetes/heapster/releases/tag/v1.4.3. ([#53377](https://github.com/kubernetes/kubernetes/pull/53377), [@loburm](https://github.com/loburm))
* Change `kubeadm create token` to default to the group that almost everyone will want to use.  The group is system:bootstrappers:kubeadm:default-node-token and is the group that kubeadm sets up, via an RBAC binding, for auto-approval (system:certificates.k8s.io:certificatesigningrequests:nodeclient). ([#53512](https://github.com/kubernetes/kubernetes/pull/53512), [@jbeda](https://github.com/jbeda))
* GCE: Fix issue deleting internal load balancers when the firewall resource may not exist. ([#53450](https://github.com/kubernetes/kubernetes/pull/53450), [@nicksardo](https://github.com/nicksardo))
* GCE: Fixes ILB sync on legacy networks and auto networks with unique subnet names ([#53410](https://github.com/kubernetes/kubernetes/pull/53410), [@nicksardo](https://github.com/nicksardo))
* Fix the bug that query Kubelet's stats summary with CRI stats enabled results in error. ([#53107](https://github.com/kubernetes/kubernetes/pull/53107), [@Random-Liu](https://github.com/Random-Liu))
* kubelet `--cert-dir` now defaults to `/var/lib/kubelet/pki`, in order to ensure bootstrapped and rotated certificates persist beyond a reboot. resolves an issue in kubeadm with false-positive `/var/lib/kubelet is not empty` message during pre-flight checks ([#53317](https://github.com/kubernetes/kubernetes/pull/53317), [@liggitt](https://github.com/liggitt))
* Fix permissions for Metrics Server. ([#53330](https://github.com/kubernetes/kubernetes/pull/53330), [@kawych](https://github.com/kawych))
* Fixes a performance issue ([#51899](https://github.com/kubernetes/kubernetes/pull/51899)) identified in large-scale clusters when deleting thousands of pods simultaneously across hundreds of nodes, by actively removing containers of deleted pods, rather than waiting for periodic garbage collection and batching resulting pod API deletion requests. ([#53233](https://github.com/kubernetes/kubernetes/pull/53233), [@dashpole](https://github.com/dashpole))
* Fixes an issue with RBAC reconciliation that could cause duplicated subjects in some bootstrapped rolebindings on each restart of the API server. ([#53239](https://github.com/kubernetes/kubernetes/pull/53239), [@enj](https://github.com/enj))
* Change ImageGCManage to consume ImageFS stats from StatsProvider ([#53094](https://github.com/kubernetes/kubernetes/pull/53094), [@yguo0905](https://github.com/yguo0905))
* Fixes an issue with `kubectl set` commands encountering conversion errors for ReplicaSet and DaemonSet objects ([#53158](https://github.com/kubernetes/kubernetes/pull/53158), [@liggitt](https://github.com/liggitt))


# v1.8.0

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Introduction to v1.8.0

Kubernetes version 1.8 includes new features and enhancements, as well as fixes to identified issues. The release notes contain a brief overview of the important changes introduced in this release. The content is organized by Special Interest Groups ([SIGs][]).

For initial installations, see the [Setup topics][] in the Kubernetes
documentation.

To upgrade to this release from a previous version, take any actions required
[Before Upgrading](#before-upgrading).

For more information about the release and for the latest documentation,
see the [Kubernetes documentation](https://kubernetes.io/docs/home/).

[Setup topics]: https://kubernetes.io/docs/setup/pick-right-solution/
[SIGs]: https://github.com/kubernetes/community/blob/master/sig-list.md


## Major Themes

Kubernetes is developed by community members whose work is organized into
[Special Interest Groups][]. For the 1.8 release, each SIG provides the
themes that guided their work.

[Special Interest Groups]: https://github.com/kubernetes/community/blob/master/sig-list.md

### SIG API Machinery

[SIG API Machinery][] is responsible for all aspects of the API server: API registration and discovery, generic API CRUD semantics, admission control, encoding/decoding, conversion, defaulting, persistence layer (etcd), OpenAPI, third-party resources, garbage collection, and client libraries.

For the 1.8 release, SIG API Machinery focused on stability and on ecosystem enablement. Features include the ability to break large LIST calls into smaller chunks, improved support for API server customization with either custom API servers or Custom Resource Definitions, and client side event spam filtering.

[Sig API Machinery]: https://github.com/kubernetes/community/tree/master/sig-api-machinery

### SIG Apps

[SIG Apps][] focuses on the Kubernetes APIs and the external tools that are required to deploy and operate Kubernetes workloads.

For the 1.8 release, SIG Apps moved the Kubernetes workloads API to the new apps/v1beta2 group and version. The DaemonSet, Deployment, ReplicaSet, and StatefulSet objects are affected by this change. The new apps/v1beta2 group and version provide a stable and consistent API surface for building applications in Kubernetes. For details about deprecations and behavioral changes, see [Notable Features](#notable-features). SIG Apps intends to promote this version to GA in a future release.

[SIG Apps]: https://github.com/kubernetes/community/tree/master/sig-apps

### SIG Auth

[SIG Auth][] is responsible for Kubernetes authentication and authorization, and for
cluster security policies.

For the 1.8 release, SIG Auth focused on stablizing existing features that were introduced
in previous releases. RBAC was moved from beta to v1, and advanced auditing was moved from alpha
to beta. Encryption of resources stored on disk (resources at rest) remained in alpha, and the SIG began exploring integrations with external key management systems.

[SIG Auth]: https://github.com/kubernetes/community/tree/master/sig-auth

### SIG Autoscaling

[SIG Autoscaling][] is responsible for autoscaling-related components,
such as the Horizontal Pod Autoscaler and Cluster Autoscaler.

For the 1.8 release, SIG Autoscaling continued to focus on stabilizing
features introduced in previous releases: the new version of the
Horizontal Pod Autoscaler API, which supports custom metrics, and
the Cluster Autoscaler, which provides improved performance and error reporting.

[SIG Autoscaling]: https://github.com/kubernetes/community/tree/master/sig-autoscaling

### SIG Cluster Lifecycle

[SIG Cluster Lifecycle][] is responsible for the user experience of deploying,
upgrading, and deleting clusters.

For the 1.8 release, SIG Cluster Lifecycle continued to focus on expanding the
capabilities of kubeadm, which is both a user-facing tool to manage clusters
and a building block for higher-level provisioning systems. Starting
with the 1.8 release, kubeadm supports a new upgrade command and includes alpha
support for self hosting the cluster control plane.

[SIG Cluster Lifecycle]: https://github.com/kubernetes/community/tree/master/sig-cluster-lifecycle

### SIG Instrumentation

[SIG Instrumentation][] is responsible for metrics production and
collection.

For the 1.8 release, SIG Instrumentation focused on stabilizing the APIs
and components that are required to support the new version of the Horizontal Pod
Autoscaler API: the resource metrics API, custom metrics API, and
metrics-server, which is the new replacement for Heapster in the default monitoring
pipeline.

[SIG Instrumentation]: https://github.com/kubernetes/community/tree/master/sig-instrumentation

### SIG Multi-cluster (formerly known as SIG Federation)

[SIG Multi-cluster][] is responsible for infrastructure that supports
the efficient and reliable management of multiple Kubernetes clusters,
and applications that run in and across multiple clusters.

For the 1.8 release, SIG Multicluster focussed on expanding the set of
Kubernetes primitives that our Cluster Federation control plane
supports, expanding the number of approaches taken to multi-cluster
management (beyond our initial Federation approach), and preparing
to release Federation for general availability ('GA').

[SIG Multi-cluster]: https://github.com/kubernetes/community/tree/master/sig-federation

### SIG Node

[SIG Node][] is responsible for the components that support the controlled
interactions between pods and host resources, and manage the lifecycle
of pods scheduled on a node.

For the 1.8 release, SIG Node continued to focus
on a broad set of workload types, including hardware and performance
sensitive workloads such as data analytics and deep learning. The SIG also
delivered incremental improvements to node reliability.

[SIG Node]: https://github.com/kubernetes/community/tree/master/sig-node

### SIG Network

[SIG Network][] is responsible for networking components, APIs, and plugins in Kubernetes.

For the 1.8 release, SIG Network enhanced the NetworkPolicy API to support pod egress traffic policies.
The SIG also provided match criteria that allow policy rules to match a source or destination CIDR. Both features are in beta. SIG Network also improved the kube-proxy to include an alpha IPVS mode in addition to the current iptables and userspace modes.

[SIG Network]: https://github.com/kubernetes/community/tree/master/sig-network

### SIG Scalability

[SIG Scalability][] is responsible for scalability testing, measuring and
improving system performance, and answering questions related to scalability.

For the 1.8 release, SIG Scalability focused on automating large cluster
scalability testing in a continuous integration (CI) environment. The SIG
defined a concrete process for scalability testing, created
documentation for the current scalability thresholds, and defined a new set of
Service Level Indicators (SLIs) and Service Level Objectives (SLOs) for the system.
Here's the release [scalability validation report].

[SIG Scalability]: https://github.com/kubernetes/community/tree/master/sig-scalability
[scalability validation report]: https://github.com/kubernetes/features/tree/master/release-1.8/scalability_validation_report.md

### SIG Scheduling

[SIG Scheduling][] is responsible for generic scheduler and scheduling components.

For the 1.8 release, SIG Scheduling extended the concept of cluster sharing by introducing
pod priority and pod preemption. These features allow mixing various types of workloads in a single cluster, and help reach
higher levels of resource utilization and availability.
These features are in alpha. SIG Scheduling also improved the internal APIs for scheduling and made them easier for other components and external schedulers to use.

[SIG Scheduling]: https://github.com/kubernetes/community/tree/master/sig-scheduling

### SIG Storage

[SIG Storage][] is responsible for storage and volume plugin components.

For the 1.8 release, SIG Storage extended the Kubernetes storage API. In addition to providing simple
volume availability, the API now enables volume resizing and snapshotting. These features are in alpha.
The SIG also focused on providing more control over storage: the ability to set requests and
limits on ephemeral storage, the ability to specify mount options, more metrics, and improvements to Flex driver deployments.

[SIG Storage]: https://github.com/kubernetes/community/tree/master/sig-storage

## Before Upgrading

Consider the following changes, limitations, and guidelines before you upgrade:

* The kubelet now fails if swap is enabled on a node. To override the default and run with /proc/swaps on, set `--fail-swap-on=false`. The experimental flag `--experimental-fail-swap-on` is deprecated in this release, and will be removed in a future release.

* The `autoscaling/v2alpha1` API is now at `autoscaling/v2beta1`. However, the form of the API remains unchanged. Migrate the `HorizontalPodAutoscaler` resources to `autoscaling/v2beta1` to persist the `HorizontalPodAutoscaler` changes introduced in `autoscaling/v2alpha1`. The Horizontal Pod Autoscaler changes include support for status conditions, and autoscaling on memory and custom metrics.

* The metrics APIs, `custom-metrics.metrics.k8s.io` and `metrics`, were moved from `v1alpha1` to `v1beta1`, and renamed to `custom.metrics.k8s.io` and `metrics.k8s.io`, respectively. If you have deployed a custom metrics adapter, ensure that it supports the new API version. If you have deployed Heapster in aggregated API server mode, upgrade Heapster to support the latest API version.

* Advanced auditing is the default auditing mechanism at `v1beta1`. The new version introduces the following changes:

  * The `--audit-policy-file` option is required if the `AdvancedAuditing` feature is not explicitly turned off (`--feature-gates=AdvancedAuditing=false`) on the API server.
  * The audit log file defaults to JSON encoding when using the advanced auditing feature gate.
  * An audit policy file without either an `apiVersion` or a `kind` field may be treated as invalid.
  * The webhook and log file now output the `v1beta1` event format.

    For more details, see [Advanced audit](https://kubernetes.io/docs/tasks/debug-application-cluster/audit/#advanced-audit).

* The deprecated `ThirdPartyResource` (TPR) API was removed.
  To avoid losing your TPR data, [migrate to CustomResourceDefinition](https://kubernetes.io/docs/tasks/access-kubernetes-api/migrate-third-party-resource/).

* The following deprecated flags were removed from `kube-controller-manager`:

  * `replication-controller-lookup-cache-size`
  * `replicaset-lookup-cache-size`
  * `daemonset-lookup-cache-size`

  Don't use these flags. Using deprecated flags causes the server to print a warning. Using a removed flag causes the server to abort the startup.

* The following deprecated flags were removed from `kubelet`:

  * `api-servers` - add apiserver addresses to the kubeconfig file instead.

  Don't use these flags. Using deprecated flags causes the kubelet to print a warning. Using a removed flag causes the kubelet to abort the startup.

* StatefulSet: The deprecated `pod.alpha.kubernetes.io/initialized` annotation for interrupting the StatefulSet Pod management is now ignored. StatefulSets with this annotation set to `true` or with no value will behave just as they did in previous versions. Dormant StatefulSets with the annotation set to `false` will become active after upgrading.

* The CronJob object is now enabled by default at `v1beta1`. CronJob `v2alpha1` is still available, but it must be explicitly enabled. We recommend that you move any current CronJob objects to `batch/v1beta1.CronJob`. Be aware that if you specify the deprecated version, you may encounter Resource Not Found errors. These errors occur because the new controllers look for the new version during a rolling update.

* The `batch/v2alpha1.ScheduledJob` was removed. Migrate to `batch/v1beta.CronJob` to continue managing time based jobs.

* The `rbac/v1alpha1`, `settings/v1alpha1`, and `scheduling/v1alpha1` APIs are disabled by default.

* The `system:node` role is no longer automatically granted to the `system:nodes` group in new clusters. The role gives broad read access to resources, including secrets and configmaps. Use the `Node` authorization mode to authorize the nodes in new clusters. To continue providing the `system:node` role to the members of the `system:nodes` group, create an installation-specific `ClusterRoleBinding` in the installation. ([#49638](https://github.com/kubernetes/kubernetes/pull/49638))

## Known Issues

This section contains a list of known issues reported in Kubernetes 1.8 release. The content is populated via [v1.8.x known issues and FAQ accumulator](https://github.com/kubernetes/kubernetes/issues/53004).

* Kubelets using TLS bootstrapping (`--bootstrap-kubeconfig`) or certificate rotation (`--rotate-certificates`) store certificates in the directory specified by `--cert-dir`. The default location (`/var/run/kubernetes`) is automatically erased on reboot on some platforms, which can prevent the kubelet from authenticating to the API server after a reboot. Specifying a non-transient location, such as `--cert-dir=/var/lib/kubelet/pki`, is recommended.

For more information, see [#53288](https://issue.k8s.io/53288).

* `kubeadm init` and `kubeadm join` invocations on newly installed systems can encounter a `/var/lib/kubelet is not empty` message during pre-flight checks that prevents setup. If this is the only pre-flight failure, it can be safely ignored with `--skip-preflight-checks`.

For more information, see [#53356](https://issue.k8s.io/53356#issuecomment-333748618).

* A performance issue was identified in large-scale clusters when deleting thousands of pods simultaneously across hundreds of nodes. Kubelets in this scenario can encounter temporarily increased latency of `delete pod` API calls -- above the target service level objective of 1 second. If you run clusters with this usage pattern and if pod deletion latency could be an issue for you, you might want to wait until the issue is resolved before you upgrade. 

For more information and for updates on resolution of this issue, see [#51899](https://github.com/kubernetes/kubernetes/issues/51899).

* Audit logs might impact the API server performance and the latency of large request and response calls. The issue is observed under the following conditions: if `AdvancedAuditing` feature gate is enabled, which is the default case, if audit logging uses the log backend in JSON format, or if the audit policy records large API calls for requests or responses.

For more information, see [#51899](https://github.com/kubernetes/kubernetes/issues/51899).

* Minikube version 0.22.2 or lower does not work with kubectl version 1.8 or higher. This issue is caused by the presence of an unregistered type in the minikube API server. New versions of kubectl force validate the OpenAPI schema, which is not registered with all known types in the minikube API server.

For more information, see [#1996](https://github.com/kubernetes/minikube/issues/1996).

* The `ENABLE_APISERVER_BASIC_AUDIT` configuration parameter for GCE deployments is broken, but deprecated.

For more information, see [#53154](https://github.com/kubernetes/kubernetes/issues/53154).

* `kubectl set` commands placed on ReplicaSet and DaemonSet occasionally return version errors. All set commands, including set image, set env, set resources, and set serviceaccounts, are affected.

For more information, see [#53040](https://github.com/kubernetes/kubernetes/issues/53040).

* Object quotas are not consistently charged or updated. Specifically, the object count quota does not reliably account for uninitialized objects. Some quotas are charged only when an object is initialized. Others are charged when an object is created, whether it is initialized or not. We plan to fix this issue in a future release.

For more information, see [#53109](https://github.com/kubernetes/kubernetes/issues/53109).

## Deprecations

This section provides an overview of deprecated API versions, options, flags, and arguments. Deprecated means that we intend to remove the capability from a future release. After removal, the capability will no longer work. The sections are organized by SIGs.

### Apps

- The `.spec.rollbackTo` field of the Deployment kind is deprecated in `extensions/v1beta1`.

- The `kubernetes.io/created-by` annotation is deprecated and will be removed in version 1.9.
  Use [ControllerRef](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/api-machinery/controller-ref.md) instead to determine which controller, if any, owns an object.

 - The `batch/v2alpha1.CronJob` is deprecated in favor of `batch/v1beta1`.

 - The `batch/v2alpha1.ScheduledJob` was removed. Use `batch/v1beta1.CronJob` instead.

### Auth

 - The RBAC v1alpha1 API group is deprecated in favor of RBAC v1.

 - The API server flag `--experimental-bootstrap-token-auth` is deprecated in favor of `--enable-bootstrap-token-auth`. The `--experimental-bootstrap-token-auth` flag will be removed in version 1.9.

### Autoscaling

 - Consuming metrics directly from Heapster is deprecated in favor of
   consuming metrics via an aggregated version of the resource metrics API.

   - In version 1.8, enable this behavior by setting the
     `--horizontal-pod-autoscaler-use-rest-clients` flag to `true`.

   - In version 1.9, this behavior will be enabled by default, and must be explicitly
     disabled by setting the `--horizontal-pod-autoscaler-use-rest-clients` flag to `false`.

### Cluster Lifecycle

- The `auto-detect` behavior of the kubelet's `--cloud-provider` flag is deprecated.

  - In version 1.8, the default value for the kubelet's `--cloud-provider` flag is `auto-detect`. Be aware that it works only on GCE, AWS and Azure.

  - In version 1.9, the default will be `""`, which means no built-in cloud provider extension will be enabled by default.

  - Enable an out-of-tree cloud provider with `--cloud-provider=external` in either version.

    For more information on deprecating auto-detecting cloud providers in kubelet, see PR [#51312](https://github.com/kubernetes/kubernetes/pull/51312) and [announcement](https://groups.google.com/forum/#!topic/kubernetes-dev/UAxwa2inbTA).

- The `PersistentVolumeLabel` admission controller in the API server is deprecated.

  - The replacement is running a cloud-specific controller-manager (often referred to as `cloud-controller-manager`) with the `PersistentVolumeLabel` controller enabled. This new controller loop operates as the `PersistentVolumeLabel` admission controller did in previous versions.

  - Do not use the `PersistentVolumeLabel` admission controller in the configuration files and scripts unless you are dependent on the in-tree GCE and AWS cloud providers.

  - The `PersistentVolumeLabel` admission controller will be removed in a future release, when the out-of-tree versions of the GCE and AWS cloud providers move to GA. The cloud providers are marked alpha in version 1.9.

### OpenStack

- The `openstack-heat` provider for `kube-up` is deprecated and will be removed
  in a future release. Refer to Issue [#49213](https://github.com/kubernetes/kubernetes/issues/49213)
  for background information.

### Scheduling

  - Opaque Integer Resources (OIRs) are deprecated and will be removed in
    version 1.9. Extended Resources (ERs) are a drop-in replacement for OIRs. You can use
    any domain name prefix outside of the `kubernetes.io/` domain instead of the
    `pod.alpha.kubernetes.io/opaque-int-resource-` prefix.

## Notable Features

### Workloads API (apps/v1beta2)

Kubernetes 1.8 adds the apps/v1beta2 group and version, which now consists of the
DaemonSet, Deployment, ReplicaSet and StatefulSet kinds. This group and version are part
of the Kubernetes Workloads API. We plan to move them to v1 in an upcoming release, so you might want to plan your migration accordingly.

For more information, see [the issue that describes this work in detail](https://github.com/kubernetes/features/issues/353)

#### API Object Additions and Migrations

- The DaemonSet, Deployment, ReplicaSet, and StatefulSet kinds
  are now in the apps/v1beta2 group and version.

- The apps/v1beta2 group version adds a Scale subresource for the StatefulSet
kind.

- All kinds in the apps/v1beta2 group version add a corresponding conditions
  kind.

#### Behavioral Changes

 - For all kinds in the API group version, a spec.selector default value is no longer
 available, because it's incompatible with `kubectl
 apply` and strategic merge patch. You must explicitly set the spec.selector value
 in your manifest. An object with a spec.selector value that does not match the labels in
 its spec.template is invalid.

 - Selector mutation is disabled for all kinds in the
 app/v1beta2 group version, because the controllers in the workloads API do not handle
 selector mutation in
 a consistent way. This restriction may be lifted in the future, but
 it is likely that that selectors will remain immutable after the move to v1.
 You can continue to use code that depends on mutable selectors by calling
 the apps/v1beta1 API in this release, but you should start planning for code
 that does not depend on mutable selectors.

 - Extended Resources are fully-qualified resource names outside the
 `kubernetes.io` domain. Extended Resource quantities must be integers.
 You can specify any resource name of the form `[aaa.]my-domain.bbb/ccc`
 in place of [Opaque Integer Resources](https://v1-6.docs.kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/#opaque-integer-resources-alpha-feature).
 Extended resources cannot be overcommitted, so make sure that request and limit are equal
 if both are present in a container spec.

 - The default Bootstrap Token created with `kubeadm init` v1.8 expires
 and is deleted after 24 hours by default to limit the exposure of the
 valuable credential. You can create a new Bootstrap Token with
 `kubeadm token create` or make the default token permanently valid by specifying
 `--token-ttl 0` to `kubeadm init`. The default token can later be deleted with
 `kubeadm token delete`.

 - `kubeadm join` now delegates TLS Bootstrapping to the kubelet itself, instead
 of reimplementing the process. `kubeadm join` writes the bootstrap kubeconfig
 file to `/etc/kubernetes/bootstrap-kubelet.conf`.

#### Defaults

 - The default spec.updateStrategy for the StatefulSet and DaemonSet kinds is
 RollingUpdate for the apps/v1beta2 group version. You can explicitly set
 the OnDelete strategy, and no strategy auto-conversion is applied to
 replace default values.

 - As mentioned in [Behavioral Changes](#behavioral-changes), selector
 defaults are disabled.

 - The default spec.revisionHistoryLimit for all applicable kinds in the
 apps/v1beta2 group version is 10.

 - In a CronJob object, the default spec.successfulJobsHistoryLimit is 3, and
 the default spec.failedJobsHistoryLimit is 1.

### Workloads API (batch)

- CronJob is now at `batch/v1beta1` ([#41039](https://github.com/kubernetes/kubernetes/issues/41039), [@soltysh](https://github.com/soltysh)).

- `batch/v2alpha.CronJob` is deprecated in favor of `batch/v1beta` and will be removed in a future release.

- Job can now set a failure policy using `.spec.backoffLimit`. The default value for this new field is 6. ([#30243](https://github.com/kubernetes/kubernetes/issues/30243), [@clamoriniere1A](https://github.com/clamoriniere1A)).

- `batch/v2alpha1.ScheduledJob` is removed.

- The Job controller now creates pods in batches instead of all at once. ([#49142](https://github.com/kubernetes/kubernetes/pull/49142), [@joelsmith](https://github.com/joelsmith)).

- Short `.spec.ActiveDeadlineSeconds` is properly applied to a Job. ([#48545](https://github.com/kubernetes/kubernetes/pull/48454), [@weiwei4](https://github.com/weiwei04)).


#### CLI Changes

- [alpha] `kubectl` plugins: `kubectl` now allows binary extensibility. You can extend the default set of `kubectl` commands by writing plugins
  that provide new subcommands. Refer to the documentation for more information.

- `kubectl rollout` and `rollback` now support StatefulSet.

- `kubectl scale` now uses the Scale subresource for kinds in the apps/v1beta2 group.

- `kubectl create configmap` and `kubectl create secret` subcommands now support
  the `--append-hash` flag, which enables unique but deterministic naming for
  objects generated from files, for example with `--from-file`.

- `kubectl run` can set a service account name in the generated pod
  spec with the `--serviceaccount` flag.

- `kubectl proxy` now correctly handles the `exec`, `attach`, and
  `portforward` commands.  You must pass `--disable-filter` to the command to allow these commands.

- Added `cronjobs.batch` to "all", so that `kubectl get all` returns them.

- Added flag `--include-uninitialized` to `kubectl annotate`, `apply`, `edit-last-applied`,
  `delete`, `describe`, `edit`, `get`, `label,` and `set`. `--include-uninitialized=true` makes
  kubectl commands apply to uninitialized objects, which by default are ignored
  if the names of the objects are not provided. `--all` also makes kubectl
  commands apply to uninitialized objects. See the
  [initializer documentation](https://kubernetes.io/docs/admin/extensible-admission-controllers/) for more details.

- Added RBAC reconcile commands with `kubectl auth reconcile -f FILE`. When
  passed a file which contains RBAC roles, rolebindings, clusterroles, or
  clusterrolebindings, this command computes covers and adds the missing rules.
  The logic required to properly apply RBAC permissions is more complicated
  than a JSON merge because you have to compute logical covers operations between
  rule sets. This means that we cannot use `kubectl apply` to update RBAC roles
  without risking breaking old clients, such as controllers.

- `kubectl delete` no longer scales down workload API objects before deletion.
  Users who depend on ordered termination for the Pods of their StatefulSets
  must use `kubectl scale` to scale down the StatefulSet before deletion.

- `kubectl run --env` no longer supports CSV parsing. To provide multiple environment
  variables, use the `--env` flag multiple times instead. Example: `--env ONE=1 --env TWO=2` instead of `--env ONE=1,TWO=2`.

- Removed deprecated command `kubectl stop`.

- Kubectl can now use http caching for the OpenAPI schema. The cache
  directory can be configured by passing the `--cache-dir` command line flag to kubectl.
  If set to an empty string, caching is disabled.

- Kubectl now performs validation against OpenAPI schema instead of Swagger 1.2. If
  OpenAPI is not available on the server, it falls back to the old Swagger 1.2.

- Added Italian translation for kubectl.

- Added German translation for kubectl.

#### Scheduling

* [alpha] This version now supports pod priority and creation of PriorityClasses ([user doc](https://kubernetes.io/docs/concepts/configuration/pod-priority-preemption/))([design doc](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/scheduling/pod-priority-api.md))

* [alpha] This version now supports priority-based preemption of pods ([user doc](https://kubernetes.io/docs/concepts/configuration/pod-priority-preemption/))([design doc](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/scheduling/pod-preemption.md))

* [alpha] Users can now add taints to nodes by condition ([design doc](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/scheduling/taint-node-by-condition.md))

#### Storage

* [stable] Mount options

  * The ability to specify mount options for volumes is moved from beta to stable.

  * A new `MountOptions` field in the `PersistentVolume` spec is available to specify mount options. This field replaces an annotation.

  * A new `MountOptions` field in the `StorageClass` spec allows configuration of mount options for dynamically provisioned volumes.

* [stable] Support Attach and Detach operations for ReadWriteOnce (RWO) volumes that use iSCSI and Fibre Channel plugins.

* [stable] Expose storage usage metrics

  * The available capacity of a given Persistent Volume (PV) is available by calling the Kubernetes metrics API.

* [stable] Volume plugin metrics

  * Success and latency metrics for all Kubernetes calls are available by calling the Kubernetes metrics API. You can request volume operations, including mount, unmount, attach, detach, provision, and delete.

* [stable] The PV spec for Azure File, CephFS, iSCSI, and Glusterfs is modified to reference namespaced resources.

* [stable] You can now customize the iSCSI initiator name per volume in the iSCSI volume plugin.

* [stable] You can now specify the World Wide Identifier (WWID) for the volume identifier in the Fibre Channel volume plugin.

* [beta] Reclaim policy in StorageClass

  * You can now configure the reclaim policy in StorageClass, instead of defaulting to `delete` for dynamically provisioned volumes.

* [alpha] Volume resizing

  * You can now increase the size of a volume by calling the Kubernetes API.

  * For alpha, this feature increases only the size of the underlying volume. It does not support resizing the file system.

  * For alpha, volume resizing supports only Gluster volumes.

* [alpha] Provide capacity isolation and resource management for local ephemeral storage

  * You can now set container requests, container limits, and node allocatable reservations for the new `ephemeral-storage` resource.

  * The `ephemeral-storage` resource includes all the disk space a container might consume with container overlay or scratch.

* [alpha] Mount namespace propagation

  * The `VolumeMount.Propagation` field for `VolumeMount` in pod containers is now available.

  * You can now set `VolumeMount.Propagation` to `Bidirectional` to enable a particular mount for a container to propagate itself to the host or other containers.

* [alpha] Improve Flex volume deployment

  * Flex volume driver deployment is simplified in the following ways:

    * New driver files can now be automatically discovered and initialized without requiring a kubelet or controller-manager restart.

    * A sample DaemonSet to deploy Flexvolume drivers is now available.

* [prototype] Volume snapshots

  * You can now create a volume snapshot by calling the Kubernetes API.

  * Note that the prototype does not support quiescing before snapshot, so snapshots might be inconsistent.

  * In the prototype phase, this feature is external to the core Kubernetes. It's available at https://github.com/kubernetes-incubator/external-storage/tree/master/snapshot.

### Cluster Federation

#### [alpha] Federated Jobs

Federated Jobs that are automatically deployed to multiple clusters
are now supported. Cluster selection and weighting determine how Job
parallelism and completions are spread across clusters. Federated Job
status reflects the aggregate status across all underlying cluster
jobs.

#### [alpha] Federated Horizontal Pod Autoscaling (HPA)

Federated HPAs are similar to the traditional Kubernetes HPAs, except
that they span multiple clusters. Creating a Federated HPA targeting
multiple clusters ensures that cluster-level autoscalers are
consistently deployed across those clusters, and dynamically managed
to ensure that autoscaling can occur optimially in all clusters,
within a set of global constraints on the the total number of replicas
permitted across all clusters.  If replicas are not
required in some clusters due to low system load or insufficient quota
or capacity in those clusters, additional replicas are made available
to the autoscalers in other clusters if required.

### Node Components

#### Autoscaling and Metrics

* Support for custom metrics in the Horizontal Pod Autoscaler is now at v1beta1. The associated metrics APIs (custom metrics and resource/master metrics) were also moved to v1beta1. For more information, see [Before Upgrading](#before-upgrading).

* `metrics-server` is now the recommended way to provide the resource
  metrics API. Deploy `metrics-server` as an add-on in the same way that you deploy Heapster.

##### Cluster Autoscaler

* Cluster autoscaler is now GA
* Cluster support size is increased to 1000 nodes
* Respect graceful pod termination of up to 10 minutes
* Handle zone stock-outs and failures
* Improve monitoring and error reporting

#### Container Runtime Interface (CRI)

* [alpha] Add a CRI validation test suite and CRI command-line tools. ([#292](https://github.com/kubernetes/features/issues/292), [@feiskyer](https://github.com/feiskyer))

* [stable] [cri-o](https://github.com/kubernetes-incubator/cri-o): CRI implementation for OCI-based runtimes [[@mrunalp](https://github.com/mrunalp)]

  * Passed all the Kubernetes 1.7 end-to-end conformance test suites.
  * Verification against Kubernetes 1.8 is planned soon after the release.

* [stable] [frakti](https://github.com/kubernetes/frakti): CRI implementation for hypervisor-based runtimes is now v1.1. [[@feiskyer](https://github.com/feiskyer)]

  * Enhance CNI plugin compatibility, supports flannel, calico, weave and so on.
  * Pass all CRI validation conformance tests and node end-to-end conformance tests.
  * Add experimental Unikernel support.

* [alpha] [cri-containerd](https://github.com/kubernetes-incubator/cri-containerd): CRI implementation for containerd is now v1.0.0-alpha.0, [[@Random-Liu](https://github.com/Random-Liu)]

  * Feature complete. Support the full CRI API defined in v1.8.
  * Pass all the CRI validation tests and regular node end-to-end tests.
  * An ansible playbook is provided to configure a Kubernetes cri-containerd cluster with kubeadm.

* Add support in Kubelet to consume container metrics via CRI. [[@yguo0905](https://github.com/yguo0905)]
  * There are known bugs that result in errors when querying Kubelet's stats summary API. We expect to fix them in v1.8.1.

#### kubelet

* [alpha] Kubelet now supports alternative container-level CPU affinity policies by using the new CPU manager. ([#375](https://github.com/kubernetes/features/issues/375), [@sjenning](https://github.com/sjenning), [@ConnorDoyle](https://github.com/ConnorDoyle))

* [alpha] Applications may now request pre-allocated hugepages by using the new `hugepages` resource in the container resource requests. ([#275](https://github.com/kubernetes/features/issues/275), [@derekwaynecarr](https://github.com/derekwaynecarr))

* [alpha] Add support for dynamic Kubelet configuration. ([#281](https://github.com/kubernetes/features/issues/281), [@mtaufen](https://github.com/mtaufen))

* [alpha] Add the Hardware Device Plugins API. ([#368](https://github.com/kubernetes/features/issues/368), [[@jiayingz](https://github.com/jiayingz)], [[@RenaudWasTaken](https://github.com/RenaudWasTaken)])

* [stable] Upgrade cAdvisor to v0.27.1 with the enhancement for node monitoring. [[@dashpole](https://github.com/dashpole)]

  * Fix journalctl leak
  * Fix container memory rss
  * Fix incorrect CPU usage with 4.7 kernel
  * OOM parser uses kmsg
  * Add hugepages support
  * Add CRI-O support

* Sharing a PID namespace between containers in a pod is disabled by default in version 1.8. To enable for a node, use the `--docker-disable-shared-pid=false` kubelet flag. Be aware that PID namespace sharing requires Docker version greater than or equal to 1.13.1.

* Fix issues related to the eviction manager.

* Fix inconsistent Prometheus cAdvisor metrics.

* Fix issues related to the local storage allocatable feature.

### Auth

* [GA] The RBAC API group has been promoted from v1beta1 to v1. No API changes were introduced.

* [beta] Advanced auditing has been promoted from alpha to beta. The webhook and logging policy formats have changed since alpha, and may require modification.

* [beta] Kubelet certificate rotation through the certificates API has been promoted from alpha to beta. RBAC cluster roles for the certificates controller have been added for common uses of the certificates API, such as the kubelet's.

* [beta] SelfSubjectRulesReview, an API that lets a user see what actions they can perform with a namespace, has been added to the authorization.k8s.io API group. This bulk query is intended to enable UIs to show/hide actions based on the end user, and for users to quickly reason about their own permissions.

* [alpha] Building on the 1.7 work to allow encryption of resources such as secrets, a mechanism to store resource encryption keys in external Key Management Systems (KMS) was introduced. This complements the original file-based storage and allows integration with multiple KMS. A Google Cloud KMS plugin was added and will be usable once the Google side of the integration is complete.

* Websocket requests may now authenticate to the API server by passing a bearer token in a websocket subprotocol of the form `base64url.bearer.authorization.k8s.io.<base64url-encoded-bearer-token>`. ([#47740](https://github.com/kubernetes/kubernetes/pull/47740), [@liggitt](https://github.com/liggitt))

* Advanced audit now correctly reports impersonated user info. ([#48184](https://github.com/kubernetes/kubernetes/pull/48184), [@CaoShuFeng](https://github.com/CaoShuFeng))

* Advanced audit policy now supports matching subresources and resource names, but the top level resource no longer matches the subresouce. For example "pods" no longer matches requests to the logs subresource of pods. Use "pods/logs" to match subresources. ([#48836](https://github.com/kubernetes/kubernetes/pull/48836), [@ericchiang](https://github.com/ericchiang))

* Previously a deleted service account or bootstrapping token secret would be considered valid until it was reaped. It is now invalid as soon as the `deletionTimestamp` is set. ([#48343](https://github.com/kubernetes/kubernetes/pull/48343), [@deads2k](https://github.com/deads2k); [#49057](https://github.com/kubernetes/kubernetes/pull/49057), [@ericchiang](https://github.com/ericchiang))

* The `--insecure-allow-any-token` flag has been removed from the API server. Users of the flag should use impersonation headers instead for debugging. ([#49045](https://github.com/kubernetes/kubernetes/pull/49045), [@ericchiang](https://github.com/ericchiang))

* The NodeRestriction admission plugin now allows a node to evict pods bound to itself. ([#48707](https://github.com/kubernetes/kubernetes/pull/48707), [@danielfm](https://github.com/danielfm))

* The OwnerReferencesPermissionEnforcement admission plugin now requires `update` permission on the `finalizers` subresource of the referenced owner in order to set `blockOwnerDeletion` on an owner reference. ([#49133](https://github.com/kubernetes/kubernetes/pull/49133), [@deads2k](https://github.com/deads2k))

* The SubjectAccessReview API in the `authorization.k8s.io` API group now allows providing the user uid. ([#49677](https://github.com/kubernetes/kubernetes/pull/49677), [@dims](https://github.com/dims))

* After a kubelet rotates its client cert, it now closes its connections to the API server to force a handshake using the new cert. Previously, the kubelet could keep its existing connection open, even if the cert used for that connection was expired and rejected by the API server. ([#49899](https://github.com/kubernetes/kubernetes/pull/49899), [@ericchiang](https://github.com/ericchiang))

* PodSecurityPolicies can now specify a whitelist of allowed paths for host volumes. ([#50212](https://github.com/kubernetes/kubernetes/pull/50212), [@jhorwit2](https://github.com/jhorwit2))

* API server authentication now caches successful bearer token authentication results for a few seconds. ([#50258](https://github.com/kubernetes/kubernetes/pull/50258), [@liggitt](https://github.com/liggitt))

* The OpenID Connect authenticator can now use a custom prefix, or omit the default prefix, for username and groups claims through the --oidc-username-prefix and --oidc-groups-prefix flags. For example, the authenticator can map a user with the username "jane" to "google:jane" by supplying the "google:" username prefix. ([#50875](https://github.com/kubernetes/kubernetes/pull/50875), [@ericchiang](https://github.com/ericchiang))

* The bootstrap token authenticator can now configure tokens with a set of extra groups in addition to `system:bootstrappers`. ([#50933](https://github.com/kubernetes/kubernetes/pull/50933), [@mattmoyer](https://github.com/mattmoyer))

* Advanced audit allows logging failed login attempts.
 ([#51119](https://github.com/kubernetes/kubernetes/pull/51119), [@soltysh](https://github.com/soltysh))

* A `kubectl auth reconcile` subcommand has been added for applying RBAC resources. When passed a file which contains RBAC roles, rolebindings, clusterroles, or clusterrolebindings, it will compute covers and add the missing rules. ([#51636](https://github.com/kubernetes/kubernetes/pull/51636), [@deads2k](https://github.com/deads2k))

### Cluster Lifecycle

#### kubeadm

* [beta] A new `upgrade` subcommand allows you to automatically upgrade a self-hosted cluster created with kubeadm. ([#296](https://github.com/kubernetes/features/issues/296), [@luxas](https://github.com/luxas))

* [alpha] An experimental self-hosted cluster can now easily be created with `kubeadm init`. Enable the feature by setting the SelfHosting feature gate to true: `--feature-gates=SelfHosting=true` ([#296](https://github.com/kubernetes/features/issues/296), [@luxas](https://github.com/luxas))
   * **NOTE:** Self-hosting will be the default way to host the control plane in the next release, v1.9

* [alpha] A new `phase` subcommand supports performing only subtasks of the full `kubeadm init` flow. Combined with fine-grained configuration, kubeadm is now more easily consumable by higher-level provisioning tools like kops or GKE. ([#356](https://github.com/kubernetes/features/issues/356), [@luxas](https://github.com/luxas))
   * **NOTE:** This command is currently staged under `kubeadm alpha phase` and will be graduated to top level in a future release.

#### kops

* [alpha] Added support for targeting bare metal (or non-cloudprovider) machines. ([#360](https://github.com/kubernetes/features/issues/360), [@justinsb](https://github.com/justinsb)).

* [alpha] kops now supports [running as a server](https://github.com/kubernetes/kops/blob/master/docs/api-server/README.md). ([#359](https://github.com/kubernetes/features/issues/359), [@justinsb](https://github.com/justinsb))

* [beta] GCE support is promoted from alpha to beta. ([#358](https://github.com/kubernetes/features/issues/358), [@justinsb](https://github.com/justinsb)).

#### Cluster Discovery/Bootstrap

* [beta] The authentication and verification mechanism called Bootstrap Tokens is improved. Use Bootstrap Tokens to easily add new node identities to a cluster. ([#130](https://github.com/kubernetes/features/issues/130), [@luxas](https://github.com/luxas), [@jbeda](https://github.com/jbeda)).

#### Multi-platform

* [alpha] The Conformance e2e test suite now passes on the arm, arm64, and ppc64le platforms. ([#288](https://github.com/kubernetes/features/issues/288), [@luxas](https://github.com/luxas), [@mkumatag](https://github.com/mkumatag), [@ixdy](https://github.com/ixdy))

#### Cloud Providers

* [alpha] Support is improved for the pluggable, out-of-tree and out-of-core cloud providers. ([#88](https://github.com/kubernetes/features/issues/88), [@wlan0](https://github.com/wlan0))

### Network

#### network-policy

* [beta] Apply NetworkPolicy based on CIDR ([#50033](https://github.com/kubernetes/kubernetes/pull/50033), [@cmluciano](https://github.com/cmluciano))

* [beta] Support EgressRules in NetworkPolicy ([#51351](https://github.com/kubernetes/kubernetes/pull/51351), [@cmluciano](https://github.com/cmluciano))

#### kube-proxy ipvs mode

[alpha] Support ipvs mode for kube-proxy([#46580](https://github.com/kubernetes/kubernetes/pull/46580), [@haibinxie](https://github.com/haibinxie))

### API Machinery

#### kube-apiserver
* Fixed an issue with `APIService` auto-registration. This issue affected rolling restarts of HA API servers that added or removed API groups being served.([#51921](https://github.com/kubernetes/kubernetes/pull/51921))

* [Alpha] The Kubernetes API server now supports the ability to break large LIST calls into multiple smaller chunks. A client can specify a limit to the number of results to return. If more results exist, a token is returned that allows the client to continue the previous list call repeatedly until all results are retrieved.  The resulting list is identical to a list call that does not perform chunking, thanks to capabilities provided by etcd3.  This allows the server to use less memory and CPU when very large lists are returned. This feature is gated as APIListChunking and is not enabled by default. The 1.9 release will begin using this by default.([#48921](https://github.com/kubernetes/kubernetes/pull/48921))

* Pods that are marked for deletion and have exceeded their grace period, but are not yet deleted, no longer count toward the resource quota.([#46542](https://github.com/kubernetes/kubernetes/pull/46542))


#### Dynamic Admission Control

* Pod spec is mutable when the pod is uninitialized. The API server requires the pod spec to be valid even if it's uninitialized. Updating the status field of uninitialized pods is invalid.([#51733](https://github.com/kubernetes/kubernetes/pull/51733))

* Use of the alpha initializers feature now requires enabling the `Initializers` feature gate. This feature gate is automatically enabled if the `Initializers` admission plugin is enabled.([#51436](https://github.com/kubernetes/kubernetes/pull/51436))

* [Action required] The validation rule for metadata.initializers.pending[x].name is tightened. The initializer name must contain at least three segments, separated by dots. You can create objects with pending initializers and not rely on the API server to add pending initializers according to `initializerConfiguration`. If you do so, update the initializer name in the existing objects and the configuration files to comply with the new validation rule.([#51283](https://github.com/kubernetes/kubernetes/pull/51283))

* The webhook admission plugin now works even if the API server and the nodes are in two separate networks,for example, in GKE.
The webhook admission plugin now lets the webhook author use the DNS name of the service as the CommonName when generating the server cert for the webhook.
Action required:
Regenerate the server cert for the admission webhooks. Previously, the CN value could be ignored while generating the server cert for the admission webhook. Now you must set it to the DNS name of the webhook service: `<service.Name>.<service.Namespace>.svc`.([#50476](https://github.com/kubernetes/kubernetes/pull/50476))


#### Custom Resource Definitions (CRDs)
* [alpha] The CustomResourceDefinition API can now optionally
  [validate custom objects](https://kubernetes.io/docs/tasks/access-kubernetes-api/extend-api-custom-resource-definitions/#validation)
  based on a JSON schema provided in the CRD spec.
  Enable this alpha feature with the `CustomResourceValidation` feature gate in `kube-apiserver`.

#### Garbage Collector
* The garbage collector now supports custom APIs added via Custom Resource Definitions
  or aggregated API servers. The garbage collector controller refreshes periodically.
  Therefore, expect a latency of about 30 seconds between when an API is added and when
  the garbage collector starts to manage it.


#### Monitoring/Prometheus
* [action required] The WATCHLIST calls are now reported as WATCH verbs in prometheus for the apiserver_request_* series.  A new "scope" label is added to all apiserver_request_* values that is either 'cluster', 'resource', or 'namespace' depending on which level the query is performed at.([#52237](https://github.com/kubernetes/kubernetes/pull/52237))


#### Go Client
* Add support for client-side spam filtering of events([#47367](https://github.com/kubernetes/kubernetes/pull/47367))


## External Dependencies

Continuous integration builds use Docker versions 1.11.2, 1.12.6, 1.13.1,
and 17.03.2. These versions were validated on Kubernetes 1.8. However,
consult an appropriate installation or upgrade guide before deciding what
versions of Docker to use.

- Docker 1.13.1 and 17.03.2

    - Shared PID namespace, live-restore, and overlay2 were validated.

    - **Known issues**

        - The default iptables FORWARD policy was changed from ACCEPT to
          DROP, which causes outbound container traffic to stop working by
          default. See
          [#40182](https://github.com/kubernetes/kubernetes/issues/40182) for
          the workaround.

        - The support for the v1 registries was removed.

- Docker 1.12.6

    - Overlay2 and live-restore are not validated.

    - **Known issues**

        - Shared PID namespace does not work properly.
          ([#207](https://github.com/kubernetes/community/pull/207#issuecomment-281870043))

        - Docker reports incorrect exit codes for containers.
          ([#41516](https://github.com/kubernetes/kubernetes/issues/41516))

- Docker 1.11.2

    - **Known issues**

        - Kernel crash with Aufs storage driver on Debian Jessie
          ([#27885](https://github.com/kubernetes/kubernetes/issues/27885)).
          The issue can be identified by using the node problem detector.

        - File descriptor leak on init/control.
          ([#275](https://github.com/containerd/containerd/issues/275))

        - Additional memory overhead per container.
          ([#21737](https://github.com/kubernetes/kubernetes/pull/21737))

        - Processes may be leaked when Docker is repeatedly terminated in a short
          time frame.
          ([#41450](https://github.com/kubernetes/kubernetes/issues/41450))
- [v1.8.0-rc.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v180-rc1)
- [v1.8.0-beta.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v180-beta1)
- [v1.8.0-alpha.3](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v180-alpha3)
- [v1.8.0-alpha.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v180-alpha2)
- [v1.8.0-alpha.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v180-alpha1)



# v1.8.0-rc.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.0-beta.1

### Action Required

* New GCE or GKE clusters created with `cluster/kube-up.sh` will not enable the legacy ABAC authorizer by default. If you would like to enable the legacy ABAC authorizer, export ENABLE_LEGACY_ABAC=true before running `cluster/kube-up.sh`. ([#51367](https://github.com/kubernetes/kubernetes/pull/51367), [@cjcullen](https://github.com/cjcullen))

### Other notable changes

* kubeadm: Use the release-1.8 branch by default ([#52085](https://github.com/kubernetes/kubernetes/pull/52085), [@luxas](https://github.com/luxas))
* PersistentVolumeLabel admission controller is now deprecated. ([#52618](https://github.com/kubernetes/kubernetes/pull/52618), [@dims](https://github.com/dims))
* Mark the LBaaS v1 of OpenStack cloud provider deprecated. ([#52821](https://github.com/kubernetes/kubernetes/pull/52821), [@FengyunPan](https://github.com/FengyunPan))
* Mark image as deliberately optional in v1 Container struct.  Many objects in the Kubernetes API inherit the container struct and only Pods require the field to be set. ([#48406](https://github.com/kubernetes/kubernetes/pull/48406), [@gyliu513](https://github.com/gyliu513))
* [fluentd-gcp addon] Update Stackdriver plugin to version 0.6.7 ([#52565](https://github.com/kubernetes/kubernetes/pull/52565), [@crassirostris](https://github.com/crassirostris))
* Remove duplicate proto errors in kubelet. ([#52132](https://github.com/kubernetes/kubernetes/pull/52132), [@adityadani](https://github.com/adityadani))
* [fluentd-gcp addon] Remove audit logs from the fluentd configuration ([#52777](https://github.com/kubernetes/kubernetes/pull/52777), [@crassirostris](https://github.com/crassirostris))
* Set defaults for successfulJobsHistoryLimit (3) and failedJobsHistoryLimit (1) in batch/v1beta1.CronJobs ([#52533](https://github.com/kubernetes/kubernetes/pull/52533), [@soltysh](https://github.com/soltysh))
* Fix: update system spec to support Docker 17.03 ([#52666](https://github.com/kubernetes/kubernetes/pull/52666), [@yguo0905](https://github.com/yguo0905))
* Fix panic in ControllerManager on GCE when it has a problem with creating external loadbalancer healthcheck ([#52646](https://github.com/kubernetes/kubernetes/pull/52646), [@gmarek](https://github.com/gmarek))
* PSP: add support for using `*` as a value in `allowedCapabilities` to allow to request any capabilities ([#51337](https://github.com/kubernetes/kubernetes/pull/51337), [@php-coder](https://github.com/php-coder))
* [fluentd-gcp addon] By default ingest apiserver audit logs written to file in JSON format. ([#52541](https://github.com/kubernetes/kubernetes/pull/52541), [@crassirostris](https://github.com/crassirostris))
* The autoscaling/v2beta1 API group is now enabled by default. ([#52549](https://github.com/kubernetes/kubernetes/pull/52549), [@DirectXMan12](https://github.com/DirectXMan12))
* Add CLUSTER_SIGNING_DURATION environment variable to cluster ([#52497](https://github.com/kubernetes/kubernetes/pull/52497), [@jcbsmpsn](https://github.com/jcbsmpsn))
    * configuration scripts to allow configuration of signing duration of
    * certificates issued via the Certificate Signing Request API.
* Introduce policy to allow the HPA to consume the metrics.k8s.io and custom.metrics.k8s.io API groups. ([#52572](https://github.com/kubernetes/kubernetes/pull/52572), [@DirectXMan12](https://github.com/DirectXMan12))
* kubelet to master communication when doing node status updates now has a timeout to prevent indefinite hangs ([#52176](https://github.com/kubernetes/kubernetes/pull/52176), [@liggitt](https://github.com/liggitt))
* Introduced Metrics Server in version v0.2.0. For more details see https://github.com/kubernetes-incubator/metrics-server/releases/tag/v0.2.0. ([#52548](https://github.com/kubernetes/kubernetes/pull/52548), [@piosz](https://github.com/piosz))
* Adds ROTATE_CERTIFICATES environment variable to kube-up.sh script for GCE ([#52115](https://github.com/kubernetes/kubernetes/pull/52115), [@jcbsmpsn](https://github.com/jcbsmpsn))
    * clusters. When that var is set to true, the command line flag enabling kubelet
    * client certificate rotation will be added to the kubelet command line.
* Make sure that resources being updated are handled correctly by Quota system ([#52452](https://github.com/kubernetes/kubernetes/pull/52452), [@gnufied](https://github.com/gnufied))
* WATCHLIST calls are now reported as WATCH verbs in prometheus for the apiserver_request_* series.  A new "scope" label is added to all apiserver_request_* values that is either 'cluster', 'resource', or 'namespace' depending on which level the query is performed at. ([#52237](https://github.com/kubernetes/kubernetes/pull/52237), [@smarterclayton](https://github.com/smarterclayton))
* Fixed the webhook admission plugin so that it works even if the apiserver and the nodes are in two networks (e.g., in GKE). ([#50476](https://github.com/kubernetes/kubernetes/pull/50476), [@caesarxuchao](https://github.com/caesarxuchao))
    * Fixed the webhook admission plugin so that webhook author could use the DNS name of the service as the CommonName when generating the server cert for the webhook.
    * Action required:
    * Anyone who generated server cert for admission webhooks need to regenerate the cert. Previously, when generating server cert for the admission webhook, the CN value doesn't matter. Now you must set it to the DNS name of the webhook service, i.e., `<service.Name>.<service.Namespace>.svc`.
* Ignore pods marked for deletion that exceed their grace period in ResourceQuota ([#46542](https://github.com/kubernetes/kubernetes/pull/46542), [@derekwaynecarr](https://github.com/derekwaynecarr))
* custom resources that use unconventional pluralization now work properly with kubectl and garbage collection ([#50012](https://github.com/kubernetes/kubernetes/pull/50012), [@deads2k](https://github.com/deads2k))
* [fluentd-gcp addon] Fluentd will trim lines exceeding 100KB instead of dropping them. ([#52289](https://github.com/kubernetes/kubernetes/pull/52289), [@crassirostris](https://github.com/crassirostris))
* dockershim: check the error when syncing the checkpoint. ([#52125](https://github.com/kubernetes/kubernetes/pull/52125), [@yujuhong](https://github.com/yujuhong))
* By default, clusters on GCE no longer sends RequestReceived audit event, if advanced audit is configured. ([#52343](https://github.com/kubernetes/kubernetes/pull/52343), [@crassirostris](https://github.com/crassirostris))
* [BugFix] Soft Eviction timer works correctly ([#52046](https://github.com/kubernetes/kubernetes/pull/52046), [@dashpole](https://github.com/dashpole))
* Azuredisk mount on windows node ([#51252](https://github.com/kubernetes/kubernetes/pull/51252), [@andyzhangx](https://github.com/andyzhangx))
* [fluentd-gcp addon] Bug with event-exporter leaking memory on metrics in clusters with CA is fixed. ([#52263](https://github.com/kubernetes/kubernetes/pull/52263), [@crassirostris](https://github.com/crassirostris))
* kubeadm: Enable kubelet client certificate rotation ([#52196](https://github.com/kubernetes/kubernetes/pull/52196), [@luxas](https://github.com/luxas))
* Scheduler predicate developer should respect equivalence class cache ([#52146](https://github.com/kubernetes/kubernetes/pull/52146), [@resouer](https://github.com/resouer))
* The `kube-cloud-controller-manager` flag `--service-account-private-key-file` was non-functional and is now deprecated. ([#50289](https://github.com/kubernetes/kubernetes/pull/50289), [@liggitt](https://github.com/liggitt))
    * The `kube-cloud-controller-manager` flag `--use-service-account-credentials` is now honored consistently, regardless of whether `--service-account-private-key-file` was specified.
* Fix credentials providers for docker sandbox image. ([#51870](https://github.com/kubernetes/kubernetes/pull/51870), [@feiskyer](https://github.com/feiskyer))
* Fixed an issue looking up cronjobs when they existed in more than one API version ([#52227](https://github.com/kubernetes/kubernetes/pull/52227), [@liggitt](https://github.com/liggitt))
* Add priority-based preemption to the scheduler. ([#50949](https://github.com/kubernetes/kubernetes/pull/50949), [@bsalamat](https://github.com/bsalamat))
* Add CLUSTER_SIGNING_DURATION environment variable to cluster configuration scripts ([#51844](https://github.com/kubernetes/kubernetes/pull/51844), [@jcbsmpsn](https://github.com/jcbsmpsn))
    * to allow configuration of signing duration of certificates issued via the Certificate
    * Signing Request API.
* Adding German translation for kubectl ([#51867](https://github.com/kubernetes/kubernetes/pull/51867), [@Steffen911](https://github.com/Steffen911))
* The ScaleIO volume plugin can now read the SDC GUID value as node label scaleio.sdcGuid; if binary drv_cfg is not installed, the plugin will still work properly; if node label not found, it defaults to drv_cfg if installed. ([#50780](https://github.com/kubernetes/kubernetes/pull/50780), [@vladimirvivien](https://github.com/vladimirvivien))
* A policy with 0 rules should return an error ([#51782](https://github.com/kubernetes/kubernetes/pull/51782), [@charrywanganthony](https://github.com/charrywanganthony))
* Log a warning when --audit-policy-file not passed to apiserver ([#52071](https://github.com/kubernetes/kubernetes/pull/52071), [@CaoShuFeng](https://github.com/CaoShuFeng))



# v1.8.0-beta.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.8/examples)

## Changelog since v1.8.0-alpha.3

### Action Required

* The OwnerReferencesPermissionEnforcement admission plugin now requires `update` permission on the `finalizers` subresource of the referenced owner in order to set `blockOwnerDeletion` on an owner reference. ([#49133](https://github.com/kubernetes/kubernetes/pull/49133), [@deads2k](https://github.com/deads2k))
* The deprecated alpha and beta initContainer annotations are no longer supported. Init containers must be specified using the initContainers field in the pod spec. ([#51816](https://github.com/kubernetes/kubernetes/pull/51816), [@liggitt](https://github.com/liggitt))
* Action required: validation rule on metadata.initializers.pending[x].name is tightened. The initializer name needs to contain at least three segments separated by dots. If you create objects with pending initializers, (i.e., not relying on apiserver adding pending initializers according to initializerconfiguration), you need to update the initializer name in existing objects and in configuration files to comply to the new validation rule. ([#51283](https://github.com/kubernetes/kubernetes/pull/51283), [@caesarxuchao](https://github.com/caesarxuchao))
* Audit policy supports matching subresources and resource names, but the top level resource no longer matches the subresouce. For example "pods" no longer matches requests to the logs subresource of pods. Use "pods/logs" to match subresources. ([#48836](https://github.com/kubernetes/kubernetes/pull/48836), [@ericchiang](https://github.com/ericchiang))
* Protobuf serialization does not distinguish between `[]` and `null`. ([#45294](https://github.com/kubernetes/kubernetes/pull/45294), [@liggitt](https://github.com/liggitt))
    * API fields previously capable of storing and returning either `[]` and `null` via JSON API requests (for example, the Endpoints `subsets` field) can now store only `null` when created using the protobuf content-type or stored in etcd using protobuf serialization (the default in 1.6+). JSON API clients should tolerate `null` values for such fields, and treat `null` and `[]` as equivalent in meaning unless specifically documented otherwise for a particular field.

### Other notable changes

* Fixes an issue with upgrade requests made via pod/service/node proxy subresources sending a non-absolute HTTP request-uri to backends ([#52065](https://github.com/kubernetes/kubernetes/pull/52065), [@liggitt](https://github.com/liggitt))
* kubeadm: add `kubeadm phase addons` command ([#51171](https://github.com/kubernetes/kubernetes/pull/51171), [@andrewrynhard](https://github.com/andrewrynhard))
* v2 of the autoscaling API group, including improvements to the HorizontalPodAutoscaler, has moved from alpha1 to beta1. ([#50708](https://github.com/kubernetes/kubernetes/pull/50708), [@DirectXMan12](https://github.com/DirectXMan12))
* Fixed a bug where some alpha features were enabled by default. ([#51839](https://github.com/kubernetes/kubernetes/pull/51839), [@jennybuckley](https://github.com/jennybuckley))
* Implement StatsProvider interface using CRI stats ([#51557](https://github.com/kubernetes/kubernetes/pull/51557), [@yguo0905](https://github.com/yguo0905))
* set AdvancedAuditing feature gate to true by default ([#51943](https://github.com/kubernetes/kubernetes/pull/51943), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Migrate the metrics/v1alpha1 API to metrics/v1beta1.  The HorizontalPodAutoscaler ([#51653](https://github.com/kubernetes/kubernetes/pull/51653), [@DirectXMan12](https://github.com/DirectXMan12))
    * controller REST client now uses that version.  For v1beta1, the API is now known as
    * resource-metrics.metrics.k8s.io.
* In GCE with COS, increase TasksMax for Docker service to raise cap on number of threads/processes used by containers. ([#51986](https://github.com/kubernetes/kubernetes/pull/51986), [@yujuhong](https://github.com/yujuhong))
* Fixes an issue with APIService auto-registration affecting rolling HA apiserver restarts that add or remove API groups being served. ([#51921](https://github.com/kubernetes/kubernetes/pull/51921), [@liggitt](https://github.com/liggitt))
* Sharing a PID namespace between containers in a pod is disabled by default in 1.8. To enable for a node, use the --docker-disable-shared-pid=false kubelet flag. Note that PID namespace sharing requires docker >= 1.13.1. ([#51634](https://github.com/kubernetes/kubernetes/pull/51634), [@verb](https://github.com/verb))
* Build test targets for all server platforms ([#51873](https://github.com/kubernetes/kubernetes/pull/51873), [@luxas](https://github.com/luxas))
* Add EgressRule to NetworkPolicy ([#51351](https://github.com/kubernetes/kubernetes/pull/51351), [@cmluciano](https://github.com/cmluciano))
* Allow DNS resolution of service name for COS using containerized mounter.  It fixed the issue with DNS resolution of NFS and Gluster services. ([#51645](https://github.com/kubernetes/kubernetes/pull/51645), [@jingxu97](https://github.com/jingxu97))
* Fix journalctl leak on kubelet restart ([#51751](https://github.com/kubernetes/kubernetes/pull/51751), [@dashpole](https://github.com/dashpole))
    * Fix container memory rss
    * Add hugepages monitoring support
    * Fix incorrect CPU usage metrics with 4.7 kernel
    * Add tmpfs monitoring support
* Support for Huge pages in empty_dir volume plugin ([#50072](https://github.com/kubernetes/kubernetes/pull/50072), [@squall0gd](https://github.com/squall0gd))
    * [Huge pages](https://www.kernel.org/doc/Documentation/vm/hugetlbpage.txt) can now be used with empty dir volume plugin.
* Alpha support for pre-allocated hugepages ([#50859](https://github.com/kubernetes/kubernetes/pull/50859), [@derekwaynecarr](https://github.com/derekwaynecarr))
* add support for client-side spam filtering of events ([#47367](https://github.com/kubernetes/kubernetes/pull/47367), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Provide a way to omit Event stages in audit policy ([#49280](https://github.com/kubernetes/kubernetes/pull/49280), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Introduced Metrics Server ([#51792](https://github.com/kubernetes/kubernetes/pull/51792), [@piosz](https://github.com/piosz))
* Implement Controller for growing persistent volumes ([#49727](https://github.com/kubernetes/kubernetes/pull/49727), [@gnufied](https://github.com/gnufied))
* Kubernetes 1.8 supports docker version 1.11.x, 1.12.x and 1.13.x. And also supports overlay2. ([#51845](https://github.com/kubernetes/kubernetes/pull/51845), [@Random-Liu](https://github.com/Random-Liu))
* The Deployment, DaemonSet, and ReplicaSet kinds in the extensions/v1beta1 group version are now deprecated, as are the Deployment, StatefulSet, and ControllerRevision kinds in apps/v1beta1. As they will not be removed until after a GA version becomes available, you may continue to use these kinds in existing code. However, all new code should be developed against the apps/v1beta2 group version. ([#51828](https://github.com/kubernetes/kubernetes/pull/51828), [@kow3ns](https://github.com/kow3ns))
* kubeadm: Detect kubelet readiness and error out if the kubelet is unhealthy ([#51369](https://github.com/kubernetes/kubernetes/pull/51369), [@luxas](https://github.com/luxas))
* Fix providerID update validation ([#51761](https://github.com/kubernetes/kubernetes/pull/51761), [@karataliu](https://github.com/karataliu))
* Calico has been updated to v2.5, RBAC added, and is now automatically scaled when GCE clusters are resized. ([#51237](https://github.com/kubernetes/kubernetes/pull/51237), [@gunjan5](https://github.com/gunjan5))
* Add backoff policy and failed pod limit for a job ([#51153](https://github.com/kubernetes/kubernetes/pull/51153), [@clamoriniere1A](https://github.com/clamoriniere1A))
* Adds a new alpha EventRateLimit admission control that is used to limit the number of event queries that are accepted by the API Server. ([#50925](https://github.com/kubernetes/kubernetes/pull/50925), [@staebler](https://github.com/staebler))
* The OpenID Connect authenticator can now use a custom prefix, or omit the default prefix, for username and groups claims through the --oidc-username-prefix and --oidc-groups-prefix flags. For example, the authenticator can map a user with the username "jane" to "google:jane" by supplying the "google:" username prefix. ([#50875](https://github.com/kubernetes/kubernetes/pull/50875), [@ericchiang](https://github.com/ericchiang))
* Implemented `kubeadm upgrade plan` for checking whether you can upgrade your cluster to a newer version ([#48899](https://github.com/kubernetes/kubernetes/pull/48899), [@luxas](https://github.com/luxas))
    * Implemented `kubeadm upgrade apply` for upgrading your cluster from one version to an other
* Switch to audit.k8s.io/v1beta1 in audit. ([#51719](https://github.com/kubernetes/kubernetes/pull/51719), [@soltysh](https://github.com/soltysh))
* update QEMU version to v2.9.1 ([#50597](https://github.com/kubernetes/kubernetes/pull/50597), [@dixudx](https://github.com/dixudx))
* controllers backoff better in face of quota denial ([#49142](https://github.com/kubernetes/kubernetes/pull/49142), [@joelsmith](https://github.com/joelsmith))
* The event table output under `kubectl describe` has been simplified to show only the most essential info. ([#51748](https://github.com/kubernetes/kubernetes/pull/51748), [@smarterclayton](https://github.com/smarterclayton))
* Use arm32v7|arm64v8 images instead of the deprecated armhf|aarch64 image organizations ([#50602](https://github.com/kubernetes/kubernetes/pull/50602), [@dixudx](https://github.com/dixudx))
* audit newest impersonated user info in the ResponseStarted, ResponseComplete audit stage ([#48184](https://github.com/kubernetes/kubernetes/pull/48184), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Fixed bug in AWS provider to handle multiple IPs when using more than 1 network interface per ec2 instance. ([#50112](https://github.com/kubernetes/kubernetes/pull/50112), [@jlz27](https://github.com/jlz27))
* Add flag "--include-uninitialized" to kubectl annotate, apply, edit-last-applied, delete, describe, edit, get, label, set. "--include-uninitialized=true" makes kubectl commands apply to uninitialized objects, which by default are ignored if the names of the objects are not provided. "--all" also makes kubectl commands apply to uninitialized objects. Please see the [initializer](https://kubernetes.io/docs/admin/extensible-admission-controllers/) doc for more details. ([#50497](https://github.com/kubernetes/kubernetes/pull/50497), [@dixudx](https://github.com/dixudx))
* GCE: Service object now supports "Network Tiers" as an Alpha feature via annotations. ([#51301](https://github.com/kubernetes/kubernetes/pull/51301), [@yujuhong](https://github.com/yujuhong))
* When using kube-up.sh on GCE, user could set env `ENABLE_POD_PRIORITY=true` to enable pod priority feature gate. ([#51069](https://github.com/kubernetes/kubernetes/pull/51069), [@MrHohn](https://github.com/MrHohn))
* The names generated for ControllerRevision and ReplicaSet are consistent with the GenerateName functionality of the API Server and will not contain "bad words". ([#51538](https://github.com/kubernetes/kubernetes/pull/51538), [@kow3ns](https://github.com/kow3ns))
* PersistentVolumeClaim metrics like "volume_stats_inodes" and "volume_stats_capacity_bytes" are now reported via kubelet prometheus ([#51553](https://github.com/kubernetes/kubernetes/pull/51553), [@wongma7](https://github.com/wongma7))
* When using IP aliases, use a secondary range rather than subnetwork to reserve cluster IPs. ([#51690](https://github.com/kubernetes/kubernetes/pull/51690), [@bowei](https://github.com/bowei))
* IPAM controller unifies handling of node pod CIDR range allocation. ([#51374](https://github.com/kubernetes/kubernetes/pull/51374), [@bowei](https://github.com/bowei))
    * It is intended to supersede the logic that is currently in range_allocator 
    * and cloud_cidr_allocator. (ALPHA FEATURE)
    * Note: for this change, the other allocators still exist and are the default.
    * It supports two modes:
        * CIDR range allocations done within the cluster that are then propagated out to the cloud provider.
        * Cloud provider managed IPAM that is then reflected into the cluster.
* Alpha list paging implementation ([#48921](https://github.com/kubernetes/kubernetes/pull/48921), [@smarterclayton](https://github.com/smarterclayton))
* add reconcile command to kubectl auth ([#51636](https://github.com/kubernetes/kubernetes/pull/51636), [@deads2k](https://github.com/deads2k))
* Advanced audit allows logging failed login attempts ([#51119](https://github.com/kubernetes/kubernetes/pull/51119), [@soltysh](https://github.com/soltysh))
* kubeadm: Add support for using an external CA whose key is never stored in the cluster ([#50832](https://github.com/kubernetes/kubernetes/pull/50832), [@nckturner](https://github.com/nckturner))
* the custom metrics API (custom.metrics.k8s.io) has moved from v1alpha1 to v1beta1 ([#50920](https://github.com/kubernetes/kubernetes/pull/50920), [@DirectXMan12](https://github.com/DirectXMan12))
* Add backoff policy and failed pod limit for a job ([#48075](https://github.com/kubernetes/kubernetes/pull/48075), [@clamoriniere1A](https://github.com/clamoriniere1A))
* Performs validation (when applying for example) against OpenAPI schema rather than Swagger 1.0. ([#51364](https://github.com/kubernetes/kubernetes/pull/51364), [@apelisse](https://github.com/apelisse))
* Make all e2e tests lookup image to use from a centralized place. In that centralized place, add support for multiple platforms. ([#49457](https://github.com/kubernetes/kubernetes/pull/49457), [@mkumatag](https://github.com/mkumatag))
* kubelet has alpha support for mount propagation. It is disabled by default and it is there for testing only. This feature may be redesigned or even removed in a future release. ([#46444](https://github.com/kubernetes/kubernetes/pull/46444), [@jsafrane](https://github.com/jsafrane))
* Add selfsubjectrulesreview API for allowing users to query which permissions they have in a given namespace. ([#48051](https://github.com/kubernetes/kubernetes/pull/48051), [@xilabao](https://github.com/xilabao))
* Kubelet re-binds /var/lib/kubelet directory with rshared mount propagation during startup if it is not shared yet. ([#45724](https://github.com/kubernetes/kubernetes/pull/45724), [@jsafrane](https://github.com/jsafrane))
* Deviceplugin jiayingz ([#51209](https://github.com/kubernetes/kubernetes/pull/51209), [@jiayingz](https://github.com/jiayingz))
* Make logdump support kubemark and support gke with 'use_custom_instance_list' ([#51834](https://github.com/kubernetes/kubernetes/pull/51834), [@shyamjvs](https://github.com/shyamjvs))
* add apps/v1beta2 conversion test ([#49645](https://github.com/kubernetes/kubernetes/pull/49645), [@dixudx](https://github.com/dixudx))
* Fixed an issue ([#47800](https://github.com/kubernetes/kubernetes/pull/47800)) where `kubectl logs -f` failed with `unexpected stream type ""`. ([#50381](https://github.com/kubernetes/kubernetes/pull/50381), [@sczizzo](https://github.com/sczizzo))
* GCE: Internal load balancer IPs are now reserved during service sync to prevent losing the address to another service. ([#51055](https://github.com/kubernetes/kubernetes/pull/51055), [@nicksardo](https://github.com/nicksardo))
* Switch JSON marshal/unmarshal to json-iterator library.  Performance should be close to previous with no generated code. ([#48287](https://github.com/kubernetes/kubernetes/pull/48287), [@thockin](https://github.com/thockin))
* Adds optional group and version information to the discovery interface, so that if an endpoint uses non-default values, the proper value of "kind" can be determined. Scale is a common example. ([#49971](https://github.com/kubernetes/kubernetes/pull/49971), [@deads2k](https://github.com/deads2k))
* [#43077](https://github.com/kubernetes/kubernetes/pull/43077) introduced a condition where DaemonSet controller did not respect the TerminationGracePeriodSeconds of the Pods it created. This is now corrected. ([#51279](https://github.com/kubernetes/kubernetes/pull/51279), [@kow3ns](https://github.com/kow3ns))
* Add a persistent volume label controller to the cloud-controller-manager ([#44680](https://github.com/kubernetes/kubernetes/pull/44680), [@rrati](https://github.com/rrati))
* Tainted nodes by conditions as following: ([#49257](https://github.com/kubernetes/kubernetes/pull/49257), [@k82cn](https://github.com/k82cn))
          * 'node.kubernetes.io/network-unavailable=:NoSchedule' if NetworkUnavailable is true
          * 'node.kubernetes.io/disk-pressure=:NoSchedule' if DiskPressure is true
          * 'node.kubernetes.io/memory-pressure=:NoSchedule' if MemoryPressure is true
          * 'node.kubernetes.io/out-of-disk=:NoSchedule' if OutOfDisk is true
* rbd: default image format to v2 instead of deprecated v1 ([#51574](https://github.com/kubernetes/kubernetes/pull/51574), [@dillaman](https://github.com/dillaman))
* Surface reasonable error when client detects connection closed. ([#51381](https://github.com/kubernetes/kubernetes/pull/51381), [@mengqiy](https://github.com/mengqiy))
* Allow PSP's to specify a whitelist of allowed paths for host volume ([#50212](https://github.com/kubernetes/kubernetes/pull/50212), [@jhorwit2](https://github.com/jhorwit2))
* For Deployment, ReplicaSet, and DaemonSet, selectors are now immutable when updating via the new `apps/v1beta2` API. For backward compatibility, selectors can still be changed when updating via `apps/v1beta1` or `extensions/v1beta1`. ([#50719](https://github.com/kubernetes/kubernetes/pull/50719), [@crimsonfaith91](https://github.com/crimsonfaith91))
* Allows kubectl to use http caching mechanism for the OpenAPI schema. The cache directory can be configured through `--cache-dir` command line flag to kubectl. If set to empty string, caching will be disabled. ([#50404](https://github.com/kubernetes/kubernetes/pull/50404), [@apelisse](https://github.com/apelisse))
* Pod log attempts are now reported in apiserver prometheus metrics with verb `CONNECT` since they can run for very long periods of time. ([#50123](https://github.com/kubernetes/kubernetes/pull/50123), [@WIZARD-CXY](https://github.com/WIZARD-CXY))
* The `emptyDir.sizeLimit` field is now correctly omitted from API requests and responses when unset. ([#50163](https://github.com/kubernetes/kubernetes/pull/50163), [@jingxu97](https://github.com/jingxu97))
* Promote CronJobs to batch/v1beta1. ([#51465](https://github.com/kubernetes/kubernetes/pull/51465), [@soltysh](https://github.com/soltysh))
* Add local ephemeral storage support to LimitRange ([#50757](https://github.com/kubernetes/kubernetes/pull/50757), [@NickrenREN](https://github.com/NickrenREN))
* Add mount options field to StorageClass. The options listed there are automatically added to PVs provisioned using the class. ([#51228](https://github.com/kubernetes/kubernetes/pull/51228), [@wongma7](https://github.com/wongma7))
* Implement IPVS-based in-cluster service load balancing ([#46580](https://github.com/kubernetes/kubernetes/pull/46580), [@dujun1990](https://github.com/dujun1990))
* Release the kubelet client certificate rotation as beta. ([#51045](https://github.com/kubernetes/kubernetes/pull/51045), [@jcbsmpsn](https://github.com/jcbsmpsn))
* Adds --append-hash flag to kubectl create configmap/secret, which will append a short hash of the configmap/secret contents to the name during creation. ([#49961](https://github.com/kubernetes/kubernetes/pull/49961), [@mtaufen](https://github.com/mtaufen))
* Add validation for CustomResources via JSON Schema. ([#47263](https://github.com/kubernetes/kubernetes/pull/47263), [@nikhita](https://github.com/nikhita))
* enqueue a sync task to wake up jobcontroller to check job ActiveDeadlineSeconds in time ([#48454](https://github.com/kubernetes/kubernetes/pull/48454), [@weiwei04](https://github.com/weiwei04))
* Remove previous local ephemeral storage resource names: "ResourceStorageOverlay" and "ResourceStorageScratch" ([#51425](https://github.com/kubernetes/kubernetes/pull/51425), [@NickrenREN](https://github.com/NickrenREN))
* Add `retainKeys` to patchStrategy for v1 Volumes and extensions/v1beta1 DeploymentStrategy. ([#50296](https://github.com/kubernetes/kubernetes/pull/50296), [@mengqiy](https://github.com/mengqiy))
* Add mount options field to PersistentVolume spec ([#50919](https://github.com/kubernetes/kubernetes/pull/50919), [@wongma7](https://github.com/wongma7))
* Use of the alpha initializers feature now requires enabling the `Initializers` feature gate. This feature gate is auto-enabled if the `Initialzers` admission plugin is enabled. ([#51436](https://github.com/kubernetes/kubernetes/pull/51436), [@liggitt](https://github.com/liggitt))
* Fix inconsistent Prometheus cAdvisor metrics ([#51473](https://github.com/kubernetes/kubernetes/pull/51473), [@bboreham](https://github.com/bboreham))
* Add local ephemeral storage to downward API  ([#50435](https://github.com/kubernetes/kubernetes/pull/50435), [@NickrenREN](https://github.com/NickrenREN))
* kubectl zsh autocompletion will work with compinit ([#50561](https://github.com/kubernetes/kubernetes/pull/50561), [@cblecker](https://github.com/cblecker))
* When using kube-up.sh on GCE, user could set env `KUBE_PROXY_DAEMONSET=true` to run kube-proxy as a DaemonSet. kube-proxy is run as static pods by default. ([#50705](https://github.com/kubernetes/kubernetes/pull/50705), [@MrHohn](https://github.com/MrHohn))
* Add --request-timeout to kube-apiserver to make global request timeout configurable. ([#51415](https://github.com/kubernetes/kubernetes/pull/51415), [@jpbetz](https://github.com/jpbetz))
* Deprecate auto detecting cloud providers in kubelet. Auto detecting cloud providers go against the initiative for out-of-tree cloud providers as we'll now depend on cAdvisor integrations with cloud providers instead of the core repo. In the near future, `--cloud-provider` for kubelet will either be an empty string or `external`.  ([#51312](https://github.com/kubernetes/kubernetes/pull/51312), [@andrewsykim](https://github.com/andrewsykim))
* Add local ephemeral storage support to Quota ([#49610](https://github.com/kubernetes/kubernetes/pull/49610), [@NickrenREN](https://github.com/NickrenREN))
* Kubelet updates default labels if those are deprecated ([#47044](https://github.com/kubernetes/kubernetes/pull/47044), [@mrIncompetent](https://github.com/mrIncompetent))
* Add error count and time-taken metrics for storage operations such as mount and attach, per-volume-plugin. ([#50036](https://github.com/kubernetes/kubernetes/pull/50036), [@wongma7](https://github.com/wongma7))
* A new predicates, named 'CheckNodeCondition', was added to replace node condition filter. 'NetworkUnavailable', 'OutOfDisk' and 'NotReady' maybe reported as a reason when failed to schedule pods. ([#51117](https://github.com/kubernetes/kubernetes/pull/51117), [@k82cn](https://github.com/k82cn))
* Add support for configurable groups for bootstrap token authentication. ([#50933](https://github.com/kubernetes/kubernetes/pull/50933), [@mattmoyer](https://github.com/mattmoyer))
* Fix forbidden message format ([#49006](https://github.com/kubernetes/kubernetes/pull/49006), [@CaoShuFeng](https://github.com/CaoShuFeng))
* make volumesInUse sorted in node status updates ([#49849](https://github.com/kubernetes/kubernetes/pull/49849), [@dixudx](https://github.com/dixudx))
* Adds `InstanceExists` and `InstanceExistsByProviderID` to cloud provider interface for the cloud controller manager ([#51087](https://github.com/kubernetes/kubernetes/pull/51087), [@prydie](https://github.com/prydie))
* Dynamic Flexvolume plugin discovery. Flexvolume plugins can now be discovered on the fly rather than only at system initialization time. ([#50031](https://github.com/kubernetes/kubernetes/pull/50031), [@verult](https://github.com/verult))
* add fieldSelector spec.schedulerName ([#50582](https://github.com/kubernetes/kubernetes/pull/50582), [@dixudx](https://github.com/dixudx))
* Change eviction manager to manage one single local ephemeral storage resource ([#50889](https://github.com/kubernetes/kubernetes/pull/50889), [@NickrenREN](https://github.com/NickrenREN))
* Cloud Controller Manager now sets Node.Spec.ProviderID ([#50730](https://github.com/kubernetes/kubernetes/pull/50730), [@andrewsykim](https://github.com/andrewsykim))
* Paramaterize session affinity timeout seconds in service API for Client IP based session affinity. ([#49850](https://github.com/kubernetes/kubernetes/pull/49850), [@m1093782566](https://github.com/m1093782566))
* Changing scheduling part of the alpha feature 'LocalStorageCapacityIsolation' to manage one single local ephemeral storage resource ([#50819](https://github.com/kubernetes/kubernetes/pull/50819), [@NickrenREN](https://github.com/NickrenREN))
* set --audit-log-format default to json ([#50971](https://github.com/kubernetes/kubernetes/pull/50971), [@CaoShuFeng](https://github.com/CaoShuFeng))
* kubeadm: Implement a `--dry-run` mode and flag for `kubeadm` ([#51122](https://github.com/kubernetes/kubernetes/pull/51122), [@luxas](https://github.com/luxas))
* kubectl rollout `history`, `status`, and `undo` subcommands now support StatefulSets. ([#49674](https://github.com/kubernetes/kubernetes/pull/49674), [@crimsonfaith91](https://github.com/crimsonfaith91))
* Add IPBlock to Network Policy ([#50033](https://github.com/kubernetes/kubernetes/pull/50033), [@cmluciano](https://github.com/cmluciano))
* Adding Italian translation for kubectl ([#50155](https://github.com/kubernetes/kubernetes/pull/50155), [@lucab85](https://github.com/lucab85))
* Simplify capabilities handling in FlexVolume. ([#51169](https://github.com/kubernetes/kubernetes/pull/51169), [@MikaelCluseau](https://github.com/MikaelCluseau))
* cloudprovider.Zones should support external cloud providers ([#50858](https://github.com/kubernetes/kubernetes/pull/50858), [@andrewsykim](https://github.com/andrewsykim))
* Finalizers are now honored on custom resources, and on other resources even when garbage collection is disabled via the apiserver flag `--enable-garbage-collector=false` ([#51148](https://github.com/kubernetes/kubernetes/pull/51148), [@ironcladlou](https://github.com/ironcladlou))
* Renamed the API server flag `--experimental-bootstrap-token-auth` to `--enable-bootstrap-token-auth`. The old value is accepted with a warning in 1.8 and will be removed in 1.9. ([#51198](https://github.com/kubernetes/kubernetes/pull/51198), [@mattmoyer](https://github.com/mattmoyer))
* Azure file persistent volumes can use a new `secretNamespace` field to reference a secret in a different namespace than the one containing their bound persistent volume claim. The azure file persistent volume provisioner honors a corresponding `secretNamespace` storage class parameter to determine where to place secrets containing the storage account key. ([#47660](https://github.com/kubernetes/kubernetes/pull/47660), [@rootfs](https://github.com/rootfs))
* Bumped gRPC version to 1.3.0 ([#51154](https://github.com/kubernetes/kubernetes/pull/51154), [@RenaudWasTaken](https://github.com/RenaudWasTaken))
* Delete load balancers if the UIDs for services don't match. ([#50539](https://github.com/kubernetes/kubernetes/pull/50539), [@brendandburns](https://github.com/brendandburns))
* Show events when describing service accounts ([#51035](https://github.com/kubernetes/kubernetes/pull/51035), [@mrogers950](https://github.com/mrogers950))
* implement proposal 34058: hostPath volume type ([#46597](https://github.com/kubernetes/kubernetes/pull/46597), [@dixudx](https://github.com/dixudx))
* HostAlias is now supported for both non-HostNetwork Pods and HostNetwork Pods. ([#50646](https://github.com/kubernetes/kubernetes/pull/50646), [@rickypai](https://github.com/rickypai))
* CRDs support metadata.generation and implement spec/status split ([#50764](https://github.com/kubernetes/kubernetes/pull/50764), [@nikhita](https://github.com/nikhita))
* Allow attach of volumes to multiple nodes for vSphere ([#51066](https://github.com/kubernetes/kubernetes/pull/51066), [@BaluDontu](https://github.com/BaluDontu))



# v1.8.0-alpha.3

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.8.0-alpha.2

### Action Required

* Remove deprecated kubectl command aliases `apiversions, clusterinfo, resize, rollingupdate, run-container, update` ([#49935](https://github.com/kubernetes/kubernetes/pull/49935), [@xiangpengzhao](https://github.com/xiangpengzhao))
* The following deprecated flags have been removed from `kube-controller-manager`: `replication-controller-lookup-cache-size`, `replicaset-lookup-cache-size`, and `daemonset-lookup-cache-size`. Make sure you no longer attempt to set them. ([#50678](https://github.com/kubernetes/kubernetes/pull/50678), [@xiangpengzhao](https://github.com/xiangpengzhao))
* Beta annotations `service.beta.kubernetes.io/external-traffic` and `service.beta.kubernetes.io/healthcheck-nodeport` have been removed. Please use fields `service.spec.externalTrafficPolicy` and `service.spec.healthCheckNodePort` instead. ([#50224](https://github.com/kubernetes/kubernetes/pull/50224), [@xiangpengzhao](https://github.com/xiangpengzhao))
* A cluster using the AWS cloud provider will need to label existing nodes and resources with a ClusterID or the kube-controller-manager will not start.  To run without a ClusterID pass --allow-untagged-cloud=true to the kube-controller-manager on startup. ([#49215](https://github.com/kubernetes/kubernetes/pull/49215), [@rrati](https://github.com/rrati))
* RBAC: the `system:node` role is no longer automatically granted to the `system:nodes` group in new clusters. It is recommended that nodes be authorized using the `Node` authorization mode instead. Installations that wish to continue giving all members of the `system:nodes` group the `system:node` role (which grants broad read access, including all secrets and configmaps) must create an installation-specific `ClusterRoleBinding`. ([#49638](https://github.com/kubernetes/kubernetes/pull/49638), [@liggitt](https://github.com/liggitt))
* StatefulSet: The deprecated `pod.alpha.kubernetes.io/initialized` annotation for interrupting StatefulSet Pod management is now ignored. If you were setting it to `true` or leaving it unset, no action is required. However, if you were setting it to `false`, be aware that previously-dormant StatefulSets may become active after upgrading. ([#49251](https://github.com/kubernetes/kubernetes/pull/49251), [@enisoc](https://github.com/enisoc))
* add some more deprecation warnings to cluster ([#49148](https://github.com/kubernetes/kubernetes/pull/49148), [@mikedanese](https://github.com/mikedanese))
* The --insecure-allow-any-token flag has been removed from kube-apiserver. Users of the flag should use impersonation headers instead for debugging. ([#49045](https://github.com/kubernetes/kubernetes/pull/49045), [@ericchiang](https://github.com/ericchiang))
* Restored cAdvisor prometheus metrics to the main port -- a regression that existed in v1.7.0-v1.7.2 ([#49079](https://github.com/kubernetes/kubernetes/pull/49079), [@smarterclayton](https://github.com/smarterclayton))
    * cAdvisor metrics can now be scraped from `/metrics/cadvisor` on the kubelet ports.
    * Note that you have to update your scraping jobs to get kubelet-only metrics from `/metrics` and `container_*` metrics from `/metrics/cadvisor`
* Change the default kubeadm bootstrap token TTL from infinite to 24 hours. This is a breaking change. If you require the old behavior, use `kubeadm init --token-ttl 0` / `kubeadm token create --ttl 0`. ([#48783](https://github.com/kubernetes/kubernetes/pull/48783), [@mattmoyer](https://github.com/mattmoyer))

### Other notable changes

* Remove duplicate command example from `kubectl port-forward --help` ([#50229](https://github.com/kubernetes/kubernetes/pull/50229), [@tcharding](https://github.com/tcharding))
* Adds a new `kubeadm config` command that lets users tell `kubeadm upgrade` what kubeadm configuration to use and lets users view the current state. ([#50980](https://github.com/kubernetes/kubernetes/pull/50980), [@luxas](https://github.com/luxas))
* Kubectl uses openapi for validation. If OpenAPI is not available on the server, it defaults back to the old Swagger. ([#50546](https://github.com/kubernetes/kubernetes/pull/50546), [@apelisse](https://github.com/apelisse))
* kubectl show node role if defined ([#50438](https://github.com/kubernetes/kubernetes/pull/50438), [@dixudx](https://github.com/dixudx))
* iSCSI volume plugin: iSCSI initiatorname support ([#48789](https://github.com/kubernetes/kubernetes/pull/48789), [@mtanino](https://github.com/mtanino))
* On AttachDetachController node status update, do not retry when node doesn't exist but keep the node entry in cache. ([#50806](https://github.com/kubernetes/kubernetes/pull/50806), [@verult](https://github.com/verult))
* Prevent unneeded endpoint updates ([#50934](https://github.com/kubernetes/kubernetes/pull/50934), [@joelsmith](https://github.com/joelsmith))
* Affinity in annotations alpha feature is no longer supported in 1.8. Anyone upgrading from 1.7 with AffinityInAnnotation feature enabled must ensure pods (specifically with pod anti-affinity PreferredDuringSchedulingIgnoredDuringExecution) with empty TopologyKey fields must be removed before upgrading to 1.8. ([#49976](https://github.com/kubernetes/kubernetes/pull/49976), [@aveshagarwal](https://github.com/aveshagarwal))
* - kubeadm now supports "ci/latest-1.8" or "ci-cross/latest-1.8" and similar labels. ([#49119](https://github.com/kubernetes/kubernetes/pull/49119), [@kad](https://github.com/kad))
* kubeadm: Adds dry-run support for kubeadm using the `--dry-run` option ([#50631](https://github.com/kubernetes/kubernetes/pull/50631), [@luxas](https://github.com/luxas))
* Change GCE installs (kube-up.sh) to use GCI/COS for node OS, by default. ([#46512](https://github.com/kubernetes/kubernetes/pull/46512), [@thockin](https://github.com/thockin))
* Use CollisionCount for collision avoidance when creating ControllerRevisions in StatefulSet controller ([#50490](https://github.com/kubernetes/kubernetes/pull/50490), [@liyinan926](https://github.com/liyinan926))
* AWS: Arbitrarily choose first (lexicographically) subnet in AZ ([#50255](https://github.com/kubernetes/kubernetes/pull/50255), [@mattlandis](https://github.com/mattlandis))
* Change CollisionCount from int64 to int32 across controllers ([#50575](https://github.com/kubernetes/kubernetes/pull/50575), [@dixudx](https://github.com/dixudx))
* fix GPU resource validation that incorrectly allows zero limits ([#50218](https://github.com/kubernetes/kubernetes/pull/50218), [@dixudx](https://github.com/dixudx))
* The `kubernetes.io/created-by` annotation is now deprecated and will be removed in v1.9. Use [ControllerRef](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/api-machinery/controller-ref.md) instead to determine which controller, if any, owns an object. ([#50536](https://github.com/kubernetes/kubernetes/pull/50536), [@crimsonfaith91](https://github.com/crimsonfaith91))
* Disable Docker's health check until we officially support it ([#50796](https://github.com/kubernetes/kubernetes/pull/50796), [@yguo0905](https://github.com/yguo0905))
* Add ControllerRevision to apps/v1beta2 ([#50698](https://github.com/kubernetes/kubernetes/pull/50698), [@liyinan926](https://github.com/liyinan926))
* StorageClass has a new field to configure reclaim policy of dynamically provisioned PVs. ([#47987](https://github.com/kubernetes/kubernetes/pull/47987), [@wongma7](https://github.com/wongma7))
* Rerun init containers when the pod needs to be restarted ([#47599](https://github.com/kubernetes/kubernetes/pull/47599), [@yujuhong](https://github.com/yujuhong))
* Resources outside the `*kubernetes.io` namespace are integers and cannot be over-committed. ([#48922](https://github.com/kubernetes/kubernetes/pull/48922), [@ConnorDoyle](https://github.com/ConnorDoyle))
* apps/v1beta2 is enabled by default. DaemonSet, Deployment, ReplicaSet, and StatefulSet have been moved to this group version. ([#50643](https://github.com/kubernetes/kubernetes/pull/50643), [@kow3ns](https://github.com/kow3ns))
* TLS cert storage for self-hosted clusters is now configurable. You can store them as secrets (alpha) or as usual host mounts. ([#50762](https://github.com/kubernetes/kubernetes/pull/50762), [@jamiehannaford](https://github.com/jamiehannaford))
* Remove deprecated command 'kubectl stop' ([#46927](https://github.com/kubernetes/kubernetes/pull/46927), [@shiywang](https://github.com/shiywang))
* Add new Prometheus metric that monitors the remaining lifetime of certificates used to authenticate requests to the API server. ([#50387](https://github.com/kubernetes/kubernetes/pull/50387), [@jcbsmpsn](https://github.com/jcbsmpsn))
* Upgrade advanced audit to version v1beta1 ([#49115](https://github.com/kubernetes/kubernetes/pull/49115), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Cluster Autoscaler - fixes issues with taints and updates kube-proxy cpu request. ([#50514](https://github.com/kubernetes/kubernetes/pull/50514), [@mwielgus](https://github.com/mwielgus))
* fluentd-elasticsearch addon: change the fluentd base image to fix crashes on systems with non-standard systemd installation ([#50679](https://github.com/kubernetes/kubernetes/pull/50679), [@aknuds1](https://github.com/aknuds1))
* advanced audit: shutdown batching audit webhook gracefully ([#50577](https://github.com/kubernetes/kubernetes/pull/50577), [@crassirostris](https://github.com/crassirostris))
* Add Priority admission controller for monitoring and resolving PriorityClasses. ([#49322](https://github.com/kubernetes/kubernetes/pull/49322), [@bsalamat](https://github.com/bsalamat))
* apiservers: add synchronous shutdown mechanism on SIGTERM+INT ([#50439](https://github.com/kubernetes/kubernetes/pull/50439), [@sttts](https://github.com/sttts))
* Fix kubernetes-worker charm hook failure when applying labels ([#50633](https://github.com/kubernetes/kubernetes/pull/50633), [@Cynerva](https://github.com/Cynerva))
* kubeadm: Implementing the controlplane phase ([#50302](https://github.com/kubernetes/kubernetes/pull/50302), [@fabriziopandini](https://github.com/fabriziopandini))
* Refactor addons into multiple packages ([#50214](https://github.com/kubernetes/kubernetes/pull/50214), [@andrewrynhard](https://github.com/andrewrynhard))
* Kubelet now manages `/etc/hosts` file for both hostNetwork Pods and non-hostNetwork Pods. ([#49140](https://github.com/kubernetes/kubernetes/pull/49140), [@rickypai](https://github.com/rickypai))
* After 1.8, admission controller will add 'MemoryPressure' toleration to Guaranteed and Burstable pods. ([#50180](https://github.com/kubernetes/kubernetes/pull/50180), [@k82cn](https://github.com/k82cn))
* A new predicates, named 'CheckNodeCondition', was added to replace node condition filter. 'NetworkUnavailable', 'OutOfDisk' and 'NotReady' maybe reported as a reason when failed to schedule pods. ([#50362](https://github.com/kubernetes/kubernetes/pull/50362), [@k82cn](https://github.com/k82cn))
* fix apps DeploymentSpec conversion issue ([#49719](https://github.com/kubernetes/kubernetes/pull/49719), [@dixudx](https://github.com/dixudx))
* fluentd-gcp addon: Fix a bug in the event-exporter, when repeated events were not sent to Stackdriver. ([#50511](https://github.com/kubernetes/kubernetes/pull/50511), [@crassirostris](https://github.com/crassirostris))
* not allowing "kubectl edit <resource>" when you got an empty list ([#50205](https://github.com/kubernetes/kubernetes/pull/50205), [@dixudx](https://github.com/dixudx))
* fixes kubefed's ability to create RBAC roles in version-skewed clusters ([#50537](https://github.com/kubernetes/kubernetes/pull/50537), [@liggitt](https://github.com/liggitt))
* API server authentication now caches successful bearer token authentication results for a few seconds. ([#50258](https://github.com/kubernetes/kubernetes/pull/50258), [@liggitt](https://github.com/liggitt))
* Added field CollisionCount to StatefulSetStatus in both apps/v1beta1 and apps/v1beta2 ([#49983](https://github.com/kubernetes/kubernetes/pull/49983), [@liyinan926](https://github.com/liyinan926))
* FC volume plugin: Support WWID for volume identifier ([#48741](https://github.com/kubernetes/kubernetes/pull/48741), [@mtanino](https://github.com/mtanino))
* kubeadm: added enhanced TLS validation for token-based discovery in `kubeadm join` using a new `--discovery-token-ca-cert-hash` flag. ([#49520](https://github.com/kubernetes/kubernetes/pull/49520), [@mattmoyer](https://github.com/mattmoyer))
* federation: Support for leader-election among federation controller-manager instances introduced. ([#46090](https://github.com/kubernetes/kubernetes/pull/46090), [@shashidharatd](https://github.com/shashidharatd))
* New get-kube.sh option: KUBERNETES_SKIP_RELEASE_VALIDATION ([#50391](https://github.com/kubernetes/kubernetes/pull/50391), [@pipejakob](https://github.com/pipejakob))
* Azure: Allow VNet to be in a separate Resource Group. ([#49725](https://github.com/kubernetes/kubernetes/pull/49725), [@sylr](https://github.com/sylr))
* fix bug when azure cloud provider configuration file is not specified ([#49283](https://github.com/kubernetes/kubernetes/pull/49283), [@dixudx](https://github.com/dixudx))
* The `rbac.authorization.k8s.io/v1beta1` API has been promoted to `rbac.authorization.k8s.io/v1` with no changes. ([#49642](https://github.com/kubernetes/kubernetes/pull/49642), [@liggitt](https://github.com/liggitt))
    * The `rbac.authorization.k8s.io/v1alpha1` version is deprecated and will be removed in a future release.
* Fix an issue where if a CSR is not approved initially by the SAR approver is not retried. ([#49788](https://github.com/kubernetes/kubernetes/pull/49788), [@mikedanese](https://github.com/mikedanese))
* The v1.Service.PublishNotReadyAddresses field is added to notify DNS addons to publish the notReadyAddresses of Enpdoints. The "service.alpha.kubernetes.io/tolerate-unready-endpoints" annotation has been deprecated and will be removed when clients have sufficient time to consume the field. ([#49061](https://github.com/kubernetes/kubernetes/pull/49061), [@kow3ns](https://github.com/kow3ns))
* vSphere cloud provider: vSphere cloud provider code refactoring ([#49164](https://github.com/kubernetes/kubernetes/pull/49164), [@BaluDontu](https://github.com/BaluDontu))
* `cluster/gke` has been removed. GKE end-to-end testing should be done using `kubetest --deployment=gke` ([#50338](https://github.com/kubernetes/kubernetes/pull/50338), [@zmerlynn](https://github.com/zmerlynn))
* kubeadm: Upload configuration used at 'kubeadm init' time to ConfigMap for easier upgrades ([#50320](https://github.com/kubernetes/kubernetes/pull/50320), [@luxas](https://github.com/luxas))
* Adds (alpha feature) the ability to dynamically configure Kubelets by enabling the DynamicKubeletConfig feature gate, posting a ConfigMap to the API server, and setting the spec.configSource field on Node objects. See the proposal at https://github.com/kubernetes/community/blob/master/contributors/design-proposals/node/dynamic-kubelet-configuration.md for details. ([#46254](https://github.com/kubernetes/kubernetes/pull/46254), [@mtaufen](https://github.com/mtaufen))
* Remove deprecated ScheduledJobs endpoints, use CronJobs instead. ([#49930](https://github.com/kubernetes/kubernetes/pull/49930), [@soltysh](https://github.com/soltysh))
* [Federation] Make the hpa scale time window configurable ([#49583](https://github.com/kubernetes/kubernetes/pull/49583), [@irfanurrehman](https://github.com/irfanurrehman))
* fuse daemons for GlusterFS and CephFS are now run in their own systemd scope when Kubernetes runs on a system with systemd. ([#49640](https://github.com/kubernetes/kubernetes/pull/49640), [@jsafrane](https://github.com/jsafrane))
* `kubectl proxy` will now correctly handle the `exec`, `attach`, and `portforward` commands.  You must pass `--disable-filter` to the command in order to allow these endpoints. ([#49534](https://github.com/kubernetes/kubernetes/pull/49534), [@smarterclayton](https://github.com/smarterclayton))
* Copy annotations from a StatefulSet's metadata to the ControllerRevisions it owns ([#50263](https://github.com/kubernetes/kubernetes/pull/50263), [@liyinan926](https://github.com/liyinan926))
* Make rolling update the default update strategy for v1beta2.DaemonSet and v1beta2.StatefulSet ([#50175](https://github.com/kubernetes/kubernetes/pull/50175), [@foxish](https://github.com/foxish))
* Deprecate Deployment .spec.rollbackTo field  ([#49340](https://github.com/kubernetes/kubernetes/pull/49340), [@janetkuo](https://github.com/janetkuo))
* Collect metrics from Heapster in Stackdriver mode. ([#50290](https://github.com/kubernetes/kubernetes/pull/50290), [@piosz](https://github.com/piosz))
* [Federation] HPA controller ([#45993](https://github.com/kubernetes/kubernetes/pull/45993), [@irfanurrehman](https://github.com/irfanurrehman))
* Relax restrictions on environment variable names. ([#48986](https://github.com/kubernetes/kubernetes/pull/48986), [@timoreimann](https://github.com/timoreimann))
* The node condition 'NodeInodePressure' was removed, as kubelet did not report it. ([#50124](https://github.com/kubernetes/kubernetes/pull/50124), [@k82cn](https://github.com/k82cn))
* Fix premature return ([#49834](https://github.com/kubernetes/kubernetes/pull/49834), [@guoshimin](https://github.com/guoshimin))
* StatefulSet uses scale subresource when scaling in accord with ReplicationController, ReplicaSet, and Deployment implementations. ([#49168](https://github.com/kubernetes/kubernetes/pull/49168), [@crimsonfaith91](https://github.com/crimsonfaith91))
* Feature gates now determine whether a cluster is self-hosted. For more information, see the FeatureGates configuration flag. ([#50241](https://github.com/kubernetes/kubernetes/pull/50241), [@jamiehannaford](https://github.com/jamiehannaford))
* Updates Cinder AttachDisk operation to be more reliable by delegating Detaches to volume manager. ([#50042](https://github.com/kubernetes/kubernetes/pull/50042), [@jingxu97](https://github.com/jingxu97))
* add fieldSelector podIP ([#50091](https://github.com/kubernetes/kubernetes/pull/50091), [@dixudx](https://github.com/dixudx))
* Return Audit-Id http response header for trouble shooting ([#49377](https://github.com/kubernetes/kubernetes/pull/49377), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Status objects for 404 API errors will have the correct APIVersion ([#49868](https://github.com/kubernetes/kubernetes/pull/49868), [@shiywang](https://github.com/shiywang))
* Fix incorrect retry logic in scheduler ([#50106](https://github.com/kubernetes/kubernetes/pull/50106), [@julia-stripe](https://github.com/julia-stripe))
* Enforce explicit references to API group client interfaces in clientsets to avoid ambiguity. ([#49370](https://github.com/kubernetes/kubernetes/pull/49370), [@sttts](https://github.com/sttts))
* update dashboard image version ([#49855](https://github.com/kubernetes/kubernetes/pull/49855), [@zouyee](https://github.com/zouyee))
* kubeadm: Implementing the kubeconfig phase fully ([#49419](https://github.com/kubernetes/kubernetes/pull/49419), [@fabriziopandini](https://github.com/fabriziopandini))
* fixes a bug around using the Global config ElbSecurityGroup where Kuberentes would modify the passed in Security Group. ([#49805](https://github.com/kubernetes/kubernetes/pull/49805), [@nbutton23](https://github.com/nbutton23))
* Fluentd DaemonSet in the fluentd-elasticsearch addon is configured via ConfigMap and includes journald plugin ([#50082](https://github.com/kubernetes/kubernetes/pull/50082), [@crassirostris](https://github.com/crassirostris))
    * Elasticsearch StatefulSet in the fluentd-elasticsearch addon uses local storage instead of PVC by default
* Add possibility to use multiple floatingip pools in openstack loadbalancer ([#49697](https://github.com/kubernetes/kubernetes/pull/49697), [@zetaab](https://github.com/zetaab))
* The 504 timeout error was returning a JSON error body that indicated it was a 500.  The body contents now correctly report a 500 error. ([#49678](https://github.com/kubernetes/kubernetes/pull/49678), [@smarterclayton](https://github.com/smarterclayton))
* add examples for kubectl run --labels ([#49862](https://github.com/kubernetes/kubernetes/pull/49862), [@dixudx](https://github.com/dixudx))
* Kubelet will by default fail with swap enabled from now on. The experimental flag "--experimental-fail-swap-on" has been deprecated, please set the new "--fail-swap-on" flag to false if you wish to run with /proc/swaps on. ([#47181](https://github.com/kubernetes/kubernetes/pull/47181), [@dims](https://github.com/dims))
* Fix bug in scheduler that caused initially unschedulable pods to stuck in Pending state forever. ([#50028](https://github.com/kubernetes/kubernetes/pull/50028), [@julia-stripe](https://github.com/julia-stripe))
* GCE: Bump GLBC version to 0.9.6 ([#50096](https://github.com/kubernetes/kubernetes/pull/50096), [@nicksardo](https://github.com/nicksardo))
* Remove 0,1,3 from rand.String, to avoid 'bad words' ([#50070](https://github.com/kubernetes/kubernetes/pull/50070), [@dixudx](https://github.com/dixudx))
* Fix data race during addition of new CRD ([#50098](https://github.com/kubernetes/kubernetes/pull/50098), [@nikhita](https://github.com/nikhita))
* Do not try to run preStopHook when the gracePeriod is 0 ([#49449](https://github.com/kubernetes/kubernetes/pull/49449), [@dhilipkumars](https://github.com/dhilipkumars))
* The SubjectAccessReview API in the authorization.k8s.io API group now allows providing the user uid. ([#49677](https://github.com/kubernetes/kubernetes/pull/49677), [@dims](https://github.com/dims))
* Increase default value of apps/v1beta2 DeploymentSpec.RevisionHistoryLimit to 10 ([#49924](https://github.com/kubernetes/kubernetes/pull/49924), [@dixudx](https://github.com/dixudx))
* Upgrade Elasticsearch/Kibana to 5.5.1 in fluentd-elasticsearch addon ([#48722](https://github.com/kubernetes/kubernetes/pull/48722), [@aknuds1](https://github.com/aknuds1))
        * Switch to basing our image of Elasticsearch in fluentd-elasticsearch addon off the official one
        * Switch to the official image of Kibana in fluentd-elasticsearch addon
        * Use StatefulSet for Elasticsearch instead of ReplicationController, with persistent volume claims
        * Require authenticating towards Elasticsearch, as Elasticsearch 5.5 by default requires basic authentication
* Rebase hyperkube image on debian-hyperkube-base, based on debian-base. ([#48365](https://github.com/kubernetes/kubernetes/pull/48365), [@ixdy](https://github.com/ixdy))
* change apps/v1beta2 StatefulSet observedGeneration (optional field) from a pointer to an int for consistency ([#49607](https://github.com/kubernetes/kubernetes/pull/49607), [@dixudx](https://github.com/dixudx))
* After a kubelet rotates its client cert, it now closes its connections to the API server to force a handshake using the new cert. Previously, the kubelet could keep its existing connection open, even if the cert used for that connection was expired and rejected by the API server. ([#49899](https://github.com/kubernetes/kubernetes/pull/49899), [@ericchiang](https://github.com/ericchiang))
* Improve our Instance Metadata coverage in Azure. ([#49237](https://github.com/kubernetes/kubernetes/pull/49237), [@brendandburns](https://github.com/brendandburns))
* Add etcd connectivity endpoint to healthz ([#49412](https://github.com/kubernetes/kubernetes/pull/49412), [@bjhaid](https://github.com/bjhaid))
* kube-proxy will emit "FailedToStartNodeHealthcheck" event when fails to start healthz server. ([#49267](https://github.com/kubernetes/kubernetes/pull/49267), [@MrHohn](https://github.com/MrHohn))
* Fixed a bug in the API server watch cache, which could cause a missing watch event immediately after cache initialization. ([#49992](https://github.com/kubernetes/kubernetes/pull/49992), [@liggitt](https://github.com/liggitt))
* Enforcement of fsGroup; enable ScaleIO multiple-instance volume mapping; default PVC capacity; alignment of PVC, PV, and volume names for dynamic provisioning ([#48999](https://github.com/kubernetes/kubernetes/pull/48999), [@vladimirvivien](https://github.com/vladimirvivien))
* In GCE, add measures to prevent corruption of known_tokens.csv. ([#49897](https://github.com/kubernetes/kubernetes/pull/49897), [@mikedanese](https://github.com/mikedanese))
* kubeadm: Fix join preflight check false negative ([#49825](https://github.com/kubernetes/kubernetes/pull/49825), [@erhudy](https://github.com/erhudy))
* route_controller will emit "FailedToCreateRoute" event when fails to create route. ([#49821](https://github.com/kubernetes/kubernetes/pull/49821), [@MrHohn](https://github.com/MrHohn))
* Fix incorrect parsing of io_priority in Portworx volume StorageClass and add support for new parameters. ([#49526](https://github.com/kubernetes/kubernetes/pull/49526), [@harsh-px](https://github.com/harsh-px))
* The API Server now automatically creates RBAC ClusterRoles for CSR approving.  ([#49284](https://github.com/kubernetes/kubernetes/pull/49284), [@luxas](https://github.com/luxas))
    * Each deployment method should bind users/groups to the ClusterRoles if they are using this feature.
* Adds AllowPrivilegeEscalation to control whether a process can gain more privileges than its parent process ([#47019](https://github.com/kubernetes/kubernetes/pull/47019), [@jessfraz](https://github.com/jessfraz))
* `hack/local-up-cluster.sh` now enables the Node authorizer by default. Authorization modes can be overridden with the `AUTHORIZATION_MODE` environment variable, and the `ENABLE_RBAC` environment variable is no longer used. ([#49812](https://github.com/kubernetes/kubernetes/pull/49812), [@liggitt](https://github.com/liggitt))
* rename stop.go file to delete.go to avoid confusion ([#49533](https://github.com/kubernetes/kubernetes/pull/49533), [@dixudx](https://github.com/dixudx))
* Adding option to set the federation api server port if nodeport is set ([#46283](https://github.com/kubernetes/kubernetes/pull/46283), [@ktsakalozos](https://github.com/ktsakalozos))
* The garbage collector now supports custom APIs added via CustomResourceDefinition or aggregated apiservers. Note that the garbage collector controller refreshes periodically, so there is a latency between when the API is added and when the garbage collector starts to manage it. ([#47665](https://github.com/kubernetes/kubernetes/pull/47665), [@ironcladlou](https://github.com/ironcladlou))
* set the juju master charm state to blocked if the services appear to be failing ([#49717](https://github.com/kubernetes/kubernetes/pull/49717), [@wwwtyro](https://github.com/wwwtyro))
* keep-terminated-pod-volumes flag on kubelet is deprecated. ([#47539](https://github.com/kubernetes/kubernetes/pull/47539), [@gnufied](https://github.com/gnufied))
* kubectl describe podsecuritypolicy describes all fields. ([#45813](https://github.com/kubernetes/kubernetes/pull/45813), [@xilabao](https://github.com/xilabao))
* Added flag support to kubectl plugins ([#47267](https://github.com/kubernetes/kubernetes/pull/47267), [@fabianofranz](https://github.com/fabianofranz))
* Adding metrics support to local volume ([#49598](https://github.com/kubernetes/kubernetes/pull/49598), [@sbezverk](https://github.com/sbezverk))
* Bug fix: Parsing of `--requestheader-group-headers` in requests should be case-insensitive. ([#49219](https://github.com/kubernetes/kubernetes/pull/49219), [@jmillikin-stripe](https://github.com/jmillikin-stripe))
* Fix instance metadata service URL. ([#49081](https://github.com/kubernetes/kubernetes/pull/49081), [@brendandburns](https://github.com/brendandburns))
* Add a new API object apps/v1beta2.ReplicaSet ([#49238](https://github.com/kubernetes/kubernetes/pull/49238), [@janetkuo](https://github.com/janetkuo))
* fix pdb validation bug on PodDisruptionBudgetSpec ([#48706](https://github.com/kubernetes/kubernetes/pull/48706), [@dixudx](https://github.com/dixudx))
* Revert deprecation of vCenter port in vSphere Cloud Provider. ([#49689](https://github.com/kubernetes/kubernetes/pull/49689), [@divyenpatel](https://github.com/divyenpatel))
* Rev version of Calico's Typha daemon used in add-on to v0.2.3 to pull in bug-fixes. ([#48469](https://github.com/kubernetes/kubernetes/pull/48469), [@fasaxc](https://github.com/fasaxc))
* set default adminid for rbd deleter if unset  ([#49271](https://github.com/kubernetes/kubernetes/pull/49271), [@dixudx](https://github.com/dixudx))
* Adding type apps/v1beta2.DaemonSet ([#49071](https://github.com/kubernetes/kubernetes/pull/49071), [@foxish](https://github.com/foxish))
* Fix nil value issue when creating json patch for merge ([#49259](https://github.com/kubernetes/kubernetes/pull/49259), [@dixudx](https://github.com/dixudx))
* Adds metrics for checking reflector health. ([#48224](https://github.com/kubernetes/kubernetes/pull/48224), [@deads2k](https://github.com/deads2k))
* remove deads2k from volume reviewer ([#49566](https://github.com/kubernetes/kubernetes/pull/49566), [@deads2k](https://github.com/deads2k))
* Unify genclient tags and add more fine control on verbs generated ([#49192](https://github.com/kubernetes/kubernetes/pull/49192), [@mfojtik](https://github.com/mfojtik))
* kubeadm: Fixes a small bug where `--config` and `--skip-*` flags couldn't be passed at the same time in validation. ([#49498](https://github.com/kubernetes/kubernetes/pull/49498), [@luxas](https://github.com/luxas))
* Remove depreciated flags: --low-diskspace-threshold-mb and --outofdisk-transition-frequency, which are replaced by --eviction-hard ([#48846](https://github.com/kubernetes/kubernetes/pull/48846), [@dashpole](https://github.com/dashpole))
* Fixed OpenAPI Description and Nickname of API objects with subresources ([#49357](https://github.com/kubernetes/kubernetes/pull/49357), [@mbohlool](https://github.com/mbohlool))
* set RBD default values as constant vars ([#49274](https://github.com/kubernetes/kubernetes/pull/49274), [@dixudx](https://github.com/dixudx))
* Fix a bug with binding mount directories and files using flexVolumes ([#49118](https://github.com/kubernetes/kubernetes/pull/49118), [@adelton](https://github.com/adelton))
* PodPreset is not injected if conflict occurs while applying PodPresets to a Pod. ([#47864](https://github.com/kubernetes/kubernetes/pull/47864), [@droot](https://github.com/droot))
* `kubectl drain` no longer spins trying to delete pods that do not exist ([#49444](https://github.com/kubernetes/kubernetes/pull/49444), [@eparis](https://github.com/eparis))
* Support specifying of FSType in StorageClass ([#45345](https://github.com/kubernetes/kubernetes/pull/45345), [@codablock](https://github.com/codablock))
* The NodeRestriction admission plugin now allows a node to evict pods bound to itself ([#48707](https://github.com/kubernetes/kubernetes/pull/48707), [@danielfm](https://github.com/danielfm))
* more robust stat handling from ceph df output in the kubernetes-master charm create-rbd-pv action ([#49394](https://github.com/kubernetes/kubernetes/pull/49394), [@wwwtyro](https://github.com/wwwtyro))
* added cronjobs.batch to all, so kubectl get all returns them. ([#49326](https://github.com/kubernetes/kubernetes/pull/49326), [@deads2k](https://github.com/deads2k))
* Update status to show failing services. ([#49296](https://github.com/kubernetes/kubernetes/pull/49296), [@ktsakalozos](https://github.com/ktsakalozos))
* Fixes [#49418](https://github.com/kubernetes/kubernetes/pull/49418) where kube-controller-manager can panic on volume.CanSupport methods and enter a crash loop. ([#49420](https://github.com/kubernetes/kubernetes/pull/49420), [@gnufied](https://github.com/gnufied))
* Add a new API version apps/v1beta2 ([#48746](https://github.com/kubernetes/kubernetes/pull/48746), [@janetkuo](https://github.com/janetkuo))
* Websocket requests to aggregated APIs now perform TLS verification using the service DNS name instead of the backend server's IP address, consistent with non-websocket requests. ([#49353](https://github.com/kubernetes/kubernetes/pull/49353), [@liggitt](https://github.com/liggitt))
* kubeadm: Don't set a specific `spc_t` SELinux label on the etcd Static Pod as that is more privs than etcd needs and due to that `spc_t` isn't compatible with some OSes. ([#49328](https://github.com/kubernetes/kubernetes/pull/49328), [@euank](https://github.com/euank))
* GCE Cloud Provider: New created LoadBalancer type Service will have health checks for nodes by default if all nodes have version >= v1.7.2. ([#49330](https://github.com/kubernetes/kubernetes/pull/49330), [@MrHohn](https://github.com/MrHohn))
* hack/local-up-cluster.sh now enables RBAC authorization by default ([#49323](https://github.com/kubernetes/kubernetes/pull/49323), [@mtanino](https://github.com/mtanino))
* Use port 20256 for node-problem-detector in standalone mode. ([#49316](https://github.com/kubernetes/kubernetes/pull/49316), [@ajitak](https://github.com/ajitak))
* Fixed unmounting of vSphere volumes when kubelet runs in a container. ([#49111](https://github.com/kubernetes/kubernetes/pull/49111), [@jsafrane](https://github.com/jsafrane))
* use informers for quota evaluation of core resources where possible ([#49230](https://github.com/kubernetes/kubernetes/pull/49230), [@deads2k](https://github.com/deads2k))
* additional backoff in azure cloudprovider ([#48967](https://github.com/kubernetes/kubernetes/pull/48967), [@jackfrancis](https://github.com/jackfrancis))
* allow impersonate serviceaccount in cli ([#48253](https://github.com/kubernetes/kubernetes/pull/48253), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Add PriorityClass API object under new "scheduling" API group ([#48377](https://github.com/kubernetes/kubernetes/pull/48377), [@bsalamat](https://github.com/bsalamat))
* Added golint check for pkg/kubelet. ([#47316](https://github.com/kubernetes/kubernetes/pull/47316), [@k82cn](https://github.com/k82cn))
* azure: acr: support MSI with preview ACR with AAD auth ([#48981](https://github.com/kubernetes/kubernetes/pull/48981), [@colemickens](https://github.com/colemickens))
* Set default CIDR to /16 for Juju deployments ([#49182](https://github.com/kubernetes/kubernetes/pull/49182), [@ktsakalozos](https://github.com/ktsakalozos))
* Fix pod preset to ignore input pod namespace in favor of request namespace ([#49120](https://github.com/kubernetes/kubernetes/pull/49120), [@jpeeler](https://github.com/jpeeler))
* Previously a deleted bootstrapping token secret would be considered valid until it was reaped.  Now it is invalid as soon as the deletionTimestamp is set. ([#49057](https://github.com/kubernetes/kubernetes/pull/49057), [@ericchiang](https://github.com/ericchiang))
* Set default snap channel on charms to 1.7 stable ([#48874](https://github.com/kubernetes/kubernetes/pull/48874), [@ktsakalozos](https://github.com/ktsakalozos))
* prevent unsetting of nonexistent previous port in kubeapi-load-balancer charm ([#49033](https://github.com/kubernetes/kubernetes/pull/49033), [@wwwtyro](https://github.com/wwwtyro))
* kubeadm: Make kube-proxy tolerate the external cloud provider taint so that an external cloud provider can be easily used on top of kubeadm ([#49017](https://github.com/kubernetes/kubernetes/pull/49017), [@luxas](https://github.com/luxas))
* Fix Pods using Portworx volumes getting stuck in ContainerCreating phase. ([#48898](https://github.com/kubernetes/kubernetes/pull/48898), [@harsh-px](https://github.com/harsh-px))
* hpa: Prevent scaling below MinReplicas if desiredReplicas is zero ([#48997](https://github.com/kubernetes/kubernetes/pull/48997), [@johanneswuerbach](https://github.com/johanneswuerbach))
* Kubelet CRI: move seccomp from annotations to security context. ([#46332](https://github.com/kubernetes/kubernetes/pull/46332), [@feiskyer](https://github.com/feiskyer))
* Never prevent deletion of resources as part of namespace lifecycle ([#48733](https://github.com/kubernetes/kubernetes/pull/48733), [@liggitt](https://github.com/liggitt))
* The generic RESTClient type (`k8s.io/client-go/rest`) no longer exposes `LabelSelectorParam` or `FieldSelectorParam` methods - use `VersionedParams` with `metav1.ListOptions` instead.  The `UintParam` method has been removed.  The `timeout` parameter will no longer cause an error when using `Param()`. ([#48991](https://github.com/kubernetes/kubernetes/pull/48991), [@smarterclayton](https://github.com/smarterclayton))
* Support completion for kubectl config delete-cluster ([#48381](https://github.com/kubernetes/kubernetes/pull/48381), [@superbrothers](https://github.com/superbrothers))
* Could get the patch from kubectl edit command ([#46091](https://github.com/kubernetes/kubernetes/pull/46091), [@xilabao](https://github.com/xilabao))
* Added scheduler integration test owners. ([#46930](https://github.com/kubernetes/kubernetes/pull/46930), [@k82cn](https://github.com/k82cn))
* `kubectl run` learned how to set a service account name in the generated pod spec with the `--serviceaccount` flag. ([#46318](https://github.com/kubernetes/kubernetes/pull/46318), [@liggitt](https://github.com/liggitt))
* Fix share name generation in azure file provisioner. ([#48326](https://github.com/kubernetes/kubernetes/pull/48326), [@karataliu](https://github.com/karataliu))
* Fixed a bug where a jsonpath filter would return an error if one of the items being evaluated did not contain all of the nested elements in the filter query. ([#47846](https://github.com/kubernetes/kubernetes/pull/47846), [@ncdc](https://github.com/ncdc))
* Uses the port config option in the kubeapi-load-balancer charm. ([#48958](https://github.com/kubernetes/kubernetes/pull/48958), [@wwwtyro](https://github.com/wwwtyro))
* azure: support retrieving access tokens via managed identity extension ([#48854](https://github.com/kubernetes/kubernetes/pull/48854), [@colemickens](https://github.com/colemickens))
* Add a runtime warning about the kubeadm default token TTL changes. ([#48838](https://github.com/kubernetes/kubernetes/pull/48838), [@mattmoyer](https://github.com/mattmoyer))
* Azure PD (Managed/Blob) ([#46360](https://github.com/kubernetes/kubernetes/pull/46360), [@khenidak](https://github.com/khenidak))
* Redirect all examples README to the the kubernetes/examples repo ([#46362](https://github.com/kubernetes/kubernetes/pull/46362), [@sebgoa](https://github.com/sebgoa))
* Fix a regression that broke the `--config` flag for `kubeadm init`. ([#48915](https://github.com/kubernetes/kubernetes/pull/48915), [@mattmoyer](https://github.com/mattmoyer))
* Fluentd-gcp DaemonSet exposes different set of metrics. ([#48812](https://github.com/kubernetes/kubernetes/pull/48812), [@crassirostris](https://github.com/crassirostris))
* MountPath should be absolute ([#48815](https://github.com/kubernetes/kubernetes/pull/48815), [@dixudx](https://github.com/dixudx))
* Updated comments of func in testapi. ([#48407](https://github.com/kubernetes/kubernetes/pull/48407), [@k82cn](https://github.com/k82cn))
* Fix service controller crash loop when Service with GCP LoadBalancer uses static IP ([#48848](https://github.com/kubernetes/kubernetes/pull/48848), [@nicksardo](https://github.com/nicksardo)) ([#48849](https://github.com/kubernetes/kubernetes/pull/48849), [@nicksardo](https://github.com/nicksardo))
* Fix pods failing to start when subPath is a dangling symlink from kubelet point of view, which can happen if it is running inside a container ([#48555](https://github.com/kubernetes/kubernetes/pull/48555), [@redbaron](https://github.com/redbaron))
* Add initial support for the Azure instance metadata service. ([#48243](https://github.com/kubernetes/kubernetes/pull/48243), [@brendandburns](https://github.com/brendandburns))
* Added new flag to `kubeadm init`: --node-name, that lets you specify the name of the Node object that will be created ([#48594](https://github.com/kubernetes/kubernetes/pull/48594), [@GheRivero](https://github.com/GheRivero))
* Added pod evictors for new zone. ([#47952](https://github.com/kubernetes/kubernetes/pull/47952), [@k82cn](https://github.com/k82cn))
* kube-up and kubemark will default to using cos (GCI) images for nodes. ([#48279](https://github.com/kubernetes/kubernetes/pull/48279), [@abgworrall](https://github.com/abgworrall))
    * The previous default was container-vm (CVM, "debian"), which is deprecated.
    * If you need to explicitly use container-vm for some reason, you should set
    * KUBE_NODE_OS_DISTRIBUTION=debian
* kubectl: Fix bug that showed terminated/evicted pods even without `--show-all`. ([#48786](https://github.com/kubernetes/kubernetes/pull/48786), [@janetkuo](https://github.com/janetkuo))
* Fixed GlusterFS volumes taking too long to time out ([#48709](https://github.com/kubernetes/kubernetes/pull/48709), [@jsafrane](https://github.com/jsafrane))



# v1.8.0-alpha.2

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.7.0

### Action Required

* The deprecated ThirdPartyResource (TPR) API has been removed. To avoid losing your TPR data, you must [migrate to CustomResourceDefinition](https://kubernetes.io/docs/tasks/access-kubernetes-api/migrate-third-party-resource/) before upgrading. ([#48353](https://github.com/kubernetes/kubernetes/pull/48353), [@deads2k](https://github.com/deads2k))

### Other notable changes

* Removed scheduler dependencies to testapi. ([#48405](https://github.com/kubernetes/kubernetes/pull/48405), [@k82cn](https://github.com/k82cn))
* kubeadm: Fix a bug where `kubeadm join` would wait 5 seconds without doing anything. Now `kubeadm join` executes the tasks immediately. ([#48737](https://github.com/kubernetes/kubernetes/pull/48737), [@mattmoyer](https://github.com/mattmoyer))
* Reduce amount of noise in Stackdriver Logging, generated by the event-exporter component in the fluentd-gcp addon. ([#48712](https://github.com/kubernetes/kubernetes/pull/48712), [@crassirostris](https://github.com/crassirostris))
* To allow the userspace proxy to work correctly on multi-interface hosts when using the non-default-route interface, you may now set the `bindAddress` configuration option to an IP address assigned to a network interface.  The proxy will use that IP address for any required NAT operations instead of the IP address of the interface which has the default route. ([#48613](https://github.com/kubernetes/kubernetes/pull/48613), [@dcbw](https://github.com/dcbw))
* Move Mesos Cloud Provider out of Kubernetes Repo ([#47232](https://github.com/kubernetes/kubernetes/pull/47232), [@gyliu513](https://github.com/gyliu513))
* - kubeadm now can accept versions like "1.6.4" where previously it strictly required "v1.6.4" ([#48507](https://github.com/kubernetes/kubernetes/pull/48507), [@kad](https://github.com/kad))
* kubeadm: Implementing the certificates phase fully ([#48196](https://github.com/kubernetes/kubernetes/pull/48196), [@fabriziopandini](https://github.com/fabriziopandini))
* Added case on 'terminated-but-not-yet-deleted' for Admit. ([#48322](https://github.com/kubernetes/kubernetes/pull/48322), [@k82cn](https://github.com/k82cn))
* `kubectl run --env` no longer supports CSV parsing. To provide multiple env vars, use the `--env` flag multiple times instead of having env vars separated by commas. E.g. `--env ONE=1 --env TWO=2` instead of `--env ONE=1,TWO=2`. ([#47460](https://github.com/kubernetes/kubernetes/pull/47460), [@mengqiy](https://github.com/mengqiy))
* Local storage teardown fix ([#48402](https://github.com/kubernetes/kubernetes/pull/48402), [@ianchakeres](https://github.com/ianchakeres))
* support json output for log backend of advanced audit ([#48605](https://github.com/kubernetes/kubernetes/pull/48605), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Requests with the query parameter `?watch=` are treated by the API server as a request to watch, but authorization and metrics were not correctly identifying those as watch requests, instead grouping them as list calls. ([#48583](https://github.com/kubernetes/kubernetes/pull/48583), [@smarterclayton](https://github.com/smarterclayton))
* As part of the NetworkPolicy "v1" changes, it is also now ([#47123](https://github.com/kubernetes/kubernetes/pull/47123), [@danwinship](https://github.com/danwinship))
    * possible to update the spec field of an existing
    * NetworkPolicy. (Previously you had to delete and recreate a
    * NetworkPolicy if you wanted to change it.)
* Fix udp service blackhole problem when number of backends changes from 0 to non-0 ([#48524](https://github.com/kubernetes/kubernetes/pull/48524), [@freehan](https://github.com/freehan))
* kubeadm: Make self-hosting work by using DaemonSets and split it out to a phase that can be invoked via the CLI ([#47435](https://github.com/kubernetes/kubernetes/pull/47435), [@luxas](https://github.com/luxas))
* Added new flag to `kubeadm join`: --node-name, that lets you specify the name of the Node object that's gonna be created ([#48538](https://github.com/kubernetes/kubernetes/pull/48538), [@GheRivero](https://github.com/GheRivero))
* Fix Audit-ID header key ([#48492](https://github.com/kubernetes/kubernetes/pull/48492), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Checked container spec when killing container. ([#48194](https://github.com/kubernetes/kubernetes/pull/48194), [@k82cn](https://github.com/k82cn))
* Fix kubectl describe for pods with controllerRef  ([#45467](https://github.com/kubernetes/kubernetes/pull/45467), [@ddysher](https://github.com/ddysher))
* Skip errors when unregistering juju kubernetes-workers ([#48144](https://github.com/kubernetes/kubernetes/pull/48144), [@ktsakalozos](https://github.com/ktsakalozos))
* Configures the Juju Charm code to run kube-proxy with conntrack-max-per-core set to 0 when in an lxc as a workaround for issues when mounting /sys/module/nf_conntrack/parameters/hashsize ([#48450](https://github.com/kubernetes/kubernetes/pull/48450), [@wwwtyro](https://github.com/wwwtyro))
* Group and order imported packages. ([#48399](https://github.com/kubernetes/kubernetes/pull/48399), [@k82cn](https://github.com/k82cn))
* RBAC role and role-binding reconciliation now ensures namespaces exist when reconciling on startup. ([#48480](https://github.com/kubernetes/kubernetes/pull/48480), [@liggitt](https://github.com/liggitt))
* Fix charms leaving services running after remove-unit ([#48446](https://github.com/kubernetes/kubernetes/pull/48446), [@Cynerva](https://github.com/Cynerva))
* Added helper funcs to schedulercache.Resource. ([#46926](https://github.com/kubernetes/kubernetes/pull/46926), [@k82cn](https://github.com/k82cn))
* When performing a GET then PUT, the kube-apiserver must write the canonical representation of the object to etcd if the current value does not match. That allows external agents to migrate content in etcd from one API version to another, across different storage types, or across varying encryption levels. This fixes a bug introduced in 1.5 where we unintentionally stopped writing the newest data. ([#48394](https://github.com/kubernetes/kubernetes/pull/48394), [@smarterclayton](https://github.com/smarterclayton))
* Fixed kubernetes charms not restarting services after snap upgrades ([#48440](https://github.com/kubernetes/kubernetes/pull/48440), [@Cynerva](https://github.com/Cynerva))
* Fix: namespace-create have kubectl in path ([#48439](https://github.com/kubernetes/kubernetes/pull/48439), [@ktsakalozos](https://github.com/ktsakalozos))
* add validate for advanced audit policy ([#47784](https://github.com/kubernetes/kubernetes/pull/47784), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Support NoSchedule taints correctly in DaemonSet controller. ([#48189](https://github.com/kubernetes/kubernetes/pull/48189), [@mikedanese](https://github.com/mikedanese))
* Adds configuration option for Swift object store container name to OpenStack Heat provider. ([#48281](https://github.com/kubernetes/kubernetes/pull/48281), [@hogepodge](https://github.com/hogepodge))
* Allow the system:heapster ClusterRole read access to deployments ([#48357](https://github.com/kubernetes/kubernetes/pull/48357), [@faraazkhan](https://github.com/faraazkhan))
* Ensure get_password is accessing a file that exists. ([#48351](https://github.com/kubernetes/kubernetes/pull/48351), [@ktsakalozos](https://github.com/ktsakalozos))
* GZip openapi schema if accepted by client ([#48151](https://github.com/kubernetes/kubernetes/pull/48151), [@apelisse](https://github.com/apelisse))
* Fixes issue where you could not mount NFS or glusterFS volumes using hostnames on GCI/GKE with COS images. ([#42376](https://github.com/kubernetes/kubernetes/pull/42376), [@jingxu97](https://github.com/jingxu97))
* Previously a deleted service account token secret would be considered valid until it was reaped.  Now it is invalid as soon as the deletionTimestamp is set. ([#48343](https://github.com/kubernetes/kubernetes/pull/48343), [@deads2k](https://github.com/deads2k))
* Securing the cluster created by Juju ([#47835](https://github.com/kubernetes/kubernetes/pull/47835), [@ktsakalozos](https://github.com/ktsakalozos))
* addon-resizer flapping behavior was removed. ([#46850](https://github.com/kubernetes/kubernetes/pull/46850), [@x13n](https://github.com/x13n))
* Change default `httpGet` probe `User-Agent` to `kube-probe/<version major.minor>` if none specified, overriding the default Go `User-Agent`. ([#47729](https://github.com/kubernetes/kubernetes/pull/47729), [@paultyng](https://github.com/paultyng))
* Registries backed by the generic Store's `Update` implementation support delete-on-update, which allows resources to be automatically deleted during an update provided: ([#48065](https://github.com/kubernetes/kubernetes/pull/48065), [@ironcladlou](https://github.com/ironcladlou))
        * Garbage collection is enabled for the Store
        * The resource being updated has no finalizers
        * The resource being updated has a non-nil DeletionGracePeriodSeconds equal to 0
    * With this fix, Custom Resource instances now also support delete-on-update behavior under the same circumstances.
* Fixes an edge case where "kubectl apply view-last-applied" would emit garbage if the data contained Go format codes. ([#45611](https://github.com/kubernetes/kubernetes/pull/45611), [@atombender](https://github.com/atombender))
* Bumped Heapster to v1.4.0. ([#48205](https://github.com/kubernetes/kubernetes/pull/48205), [@piosz](https://github.com/piosz))
    * More details about the release https://github.com/kubernetes/heapster/releases/tag/v1.4.0
* In GCE and in a "private master" setup, do not set the network-plugin provider to CNI by default if a network policy provider is given. ([#48004](https://github.com/kubernetes/kubernetes/pull/48004), [@dnardo](https://github.com/dnardo))
* Add generic NoSchedule toleration to fluentd in gcp config. ([#48182](https://github.com/kubernetes/kubernetes/pull/48182), [@gmarek](https://github.com/gmarek))
* kubeadm: Expose only the cluster-info ConfigMap in the kube-public ns ([#48050](https://github.com/kubernetes/kubernetes/pull/48050), [@luxas](https://github.com/luxas))
* Fixes kubelet race condition in container manager. ([#48123](https://github.com/kubernetes/kubernetes/pull/48123), [@msau42](https://github.com/msau42))
* Bump GCE ContainerVM to container-vm-v20170627 ([#48159](https://github.com/kubernetes/kubernetes/pull/48159), [@zmerlynn](https://github.com/zmerlynn))
* Add PriorityClassName and Priority fields to PodSpec. ([#45610](https://github.com/kubernetes/kubernetes/pull/45610), [@bsalamat](https://github.com/bsalamat))
* Add a failsafe for etcd not returning a connection string ([#48054](https://github.com/kubernetes/kubernetes/pull/48054), [@ktsakalozos](https://github.com/ktsakalozos))
* Fix fluentd-gcp configuration to facilitate JSON parsing ([#48139](https://github.com/kubernetes/kubernetes/pull/48139), [@crassirostris](https://github.com/crassirostris))
* Setting env var ENABLE_BIG_CLUSTER_SUBNETS=true will allow kube-up.sh to start clusters bigger that 4095 Nodes on GCE. ([#47513](https://github.com/kubernetes/kubernetes/pull/47513), [@gmarek](https://github.com/gmarek))
* When determining the default external host of the kube apiserver, any configured cloud provider is now consulted ([#47038](https://github.com/kubernetes/kubernetes/pull/47038), [@yastij](https://github.com/yastij))
* Updated comments for functions. ([#47242](https://github.com/kubernetes/kubernetes/pull/47242), [@k82cn](https://github.com/k82cn))
* Fix setting juju worker labels during deployment ([#47178](https://github.com/kubernetes/kubernetes/pull/47178), [@ktsakalozos](https://github.com/ktsakalozos))
* `kubefed init` correctly checks for RBAC API enablement. ([#48077](https://github.com/kubernetes/kubernetes/pull/48077), [@liggitt](https://github.com/liggitt))
* The garbage collector now cascades deletion properly when deleting an object with propagationPolicy="background". This resolves issue [#44046](https://github.com/kubernetes/kubernetes/issues/44046), so that when a deployment is deleted with propagationPolicy="background", the garbage collector ensures dependent pods are deleted as well. ([#44058](https://github.com/kubernetes/kubernetes/pull/44058), [@caesarxuchao](https://github.com/caesarxuchao))
* Fix restart action on juju kubernetes-master ([#47170](https://github.com/kubernetes/kubernetes/pull/47170), [@ktsakalozos](https://github.com/ktsakalozos))
* e2e: bump kubelet's resurce usage limit ([#47971](https://github.com/kubernetes/kubernetes/pull/47971), [@yujuhong](https://github.com/yujuhong))
* Cluster Autoscaler 0.6 ([#48074](https://github.com/kubernetes/kubernetes/pull/48074), [@mwielgus](https://github.com/mwielgus))
* Checked whether balanced Pods were created. ([#47488](https://github.com/kubernetes/kubernetes/pull/47488), [@k82cn](https://github.com/k82cn))
* Update protobuf time serialization for a one second granularity ([#47975](https://github.com/kubernetes/kubernetes/pull/47975), [@deads2k](https://github.com/deads2k))
* Bumped Heapster to v1.4.0-beta.0 ([#47961](https://github.com/kubernetes/kubernetes/pull/47961), [@piosz](https://github.com/piosz))
* `kubectl api-versions` now always fetches information about enabled API groups and versions instead of using the local cache. ([#48016](https://github.com/kubernetes/kubernetes/pull/48016), [@liggitt](https://github.com/liggitt))
* Removes alpha feature gate for affinity annotations.   ([#47869](https://github.com/kubernetes/kubernetes/pull/47869), [@timothysc](https://github.com/timothysc))
* Websocket requests may now authenticate to the API server by passing a bearer token in a websocket subprotocol of the form `base64url.bearer.authorization.k8s.io.<base64url-encoded-bearer-token>` ([#47740](https://github.com/kubernetes/kubernetes/pull/47740), [@liggitt](https://github.com/liggitt))
* Update cadvisor to v0.26.1 ([#47940](https://github.com/kubernetes/kubernetes/pull/47940), [@Random-Liu](https://github.com/Random-Liu))
* Bump up npd version to v0.4.1 ([#47892](https://github.com/kubernetes/kubernetes/pull/47892), [@ajitak](https://github.com/ajitak))
* Allow StorageClass Ceph RBD to specify image format and image features. ([#45805](https://github.com/kubernetes/kubernetes/pull/45805), [@weiwei04](https://github.com/weiwei04))
* Removed mesos related labels. ([#46824](https://github.com/kubernetes/kubernetes/pull/46824), [@k82cn](https://github.com/k82cn))
* Add RBAC support to fluentd-elasticsearch cluster addon ([#46203](https://github.com/kubernetes/kubernetes/pull/46203), [@simt2](https://github.com/simt2))
* Avoid redundant copying of tars during kube-up for gce if the same file already exists ([#46792](https://github.com/kubernetes/kubernetes/pull/46792), [@ianchakeres](https://github.com/ianchakeres))
* container runtime version has been added to the output of `kubectl get nodes -o=wide` as `CONTAINER-RUNTIME` ([#46646](https://github.com/kubernetes/kubernetes/pull/46646), [@rickypai](https://github.com/rickypai))
* cAdvisor binds only to the interface that kubelet is running on instead of all interfaces. ([#47195](https://github.com/kubernetes/kubernetes/pull/47195), [@dims](https://github.com/dims))
* The schema of the API that are served by the kube-apiserver, together with a small amount of generated code, are moved to k8s.io/api (https://github.com/kubernetes/api). ([#44784](https://github.com/kubernetes/kubernetes/pull/44784), [@caesarxuchao](https://github.com/caesarxuchao))



# v1.8.0-alpha.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.7.0-alpha.4

### Action Required

* The following alpha API groups were unintentionally enabled by default in previous releases, and will no longer be enabled by default in v1.8: ([#47690](https://github.com/kubernetes/kubernetes/pull/47690), [@caesarxuchao](https://github.com/caesarxuchao))
    * rbac.authorization.k8s.io/v1alpha1
    * settings.k8s.io/v1alpha1
    * If you wish to continue using them in v1.8, please enable them explicitly using the `--runtime-config` flag of the apiserver (for example, `--runtime-config="rbac.authorization.k8s.io/v1alpha1,settings.k8s.io/v1alpha1"`)
* Paths containing backsteps (for example, "../bar") are no longer allowed in hostPath volume paths, or in volumeMount subpaths ([#47290](https://github.com/kubernetes/kubernetes/pull/47290), [@jhorwit2](https://github.com/jhorwit2))
* Azure: Change container permissions to private for provisioned volumes. If you have existing Azure volumes that were created by Kubernetes v1.6.0-v1.6.5, you should change the permissions on them manually. ([#47605](https://github.com/kubernetes/kubernetes/pull/47605), [@brendandburns](https://github.com/brendandburns))
* New and upgraded 1.7 GCE/GKE clusters no longer have an RBAC ClusterRoleBinding that grants the `cluster-admin` ClusterRole to the `default` service account in the `kube-system` namespace. ([#46750](https://github.com/kubernetes/kubernetes/pull/46750), [@cjcullen](https://github.com/cjcullen))
    * If this permission is still desired, run the following command to explicitly grant it, either before or after upgrading to 1.7:
    *     kubectl create clusterrolebinding kube-system-default --serviceaccount=kube-system:default --clusterrole=cluster-admin
* kube-apiserver: a new authorization mode (`--authorization-mode=Node`) authorizes nodes to access secrets, configmaps, persistent volume claims and persistent volumes related to their pods. ([#46076](https://github.com/kubernetes/kubernetes/pull/46076), [@liggitt](https://github.com/liggitt))
        * Nodes must use client credentials that place them in the `system:nodes` group with a username of `system:node:<nodeName>` in order to be authorized by the node authorizer (the credentials obtained by the kubelet via TLS bootstrapping satisfy these requirements)
        * When used in combination with the `RBAC` authorization mode (`--authorization-mode=Node,RBAC`), the `system:node` role is no longer automatically granted to the `system:nodes` group.
* kube-controller-manager has dropped support for the `--insecure-experimental-approve-all-kubelet-csrs-for-group` flag. Instead, the `csrapproving` controller uses authorization checks to determine whether to approve certificate signing requests: ([#45619](https://github.com/kubernetes/kubernetes/pull/45619), [@mikedanese](https://github.com/mikedanese))
        * requests for a TLS client certificate for any node are approved if the CSR creator has `create` permission on the `certificatesigningrequests` resource and `nodeclient` subresource in the `certificates.k8s.io` API group
        * requests from a node for a TLS client certificate for itself are approved if the CSR creator has `create` permission on the `certificatesigningrequests` resource and the `selfnodeclient` subresource in the `certificates.k8s.io` API group
        * requests from a node for a TLS serving certificate for itself are approved if the CSR creator has `create` permission on the `certificatesigningrequests` resource and the `selfnodeserver` subresource in the `certificates.k8s.io` API group
* Support updating storageclasses in etcd to storage.k8s.io/v1. You must do this prior to upgrading to 1.8. ([#46116](https://github.com/kubernetes/kubernetes/pull/46116), [@ncdc](https://github.com/ncdc))
* The namespace API object no longer supports the deletecollection operation. ([#46407](https://github.com/kubernetes/kubernetes/pull/46407), [@liggitt](https://github.com/liggitt))
* NetworkPolicy has been moved from `extensions/v1beta1` to the new ([#39164](https://github.com/kubernetes/kubernetes/pull/39164), [@danwinship](https://github.com/danwinship))
	`networking.k8s.io/v1` API group. The structure remains unchanged from
	the beta1 API.
	The `net.beta.kubernetes.io/network-policy` annotation on Namespaces
	to opt in to isolation has been removed. Instead, isolation is now
	determined at a per-pod level, with pods being isolated if there is
	any NetworkPolicy whose spec.podSelector targets them. Pods that are
	targeted by NetworkPolicies accept traffic that is accepted by any of
	the NetworkPolicies (and nothing else), and pods that are not targeted
	by any NetworkPolicy accept all traffic by default.
	Action Required:
	When upgrading to Kubernetes 1.7 (and a network plugin that supports
	the new NetworkPolicy v1 semantics), to ensure full behavioral
	compatibility with v1beta1:
	1. In Namespaces that previously had the "DefaultDeny" annotation,
	   you can create equivalent v1 semantics by creating a
	   NetworkPolicy that matches all pods but does not allow any
	   traffic:

	   ```yaml
           kind: NetworkPolicy
           apiVersion: networking.k8s.io/v1
           metadata:
             name: default-deny
           spec:
             podSelector:
	   ```

	   This will ensure that pods that aren't matched by any other
	   NetworkPolicy will continue to be fully-isolated, as they were
	   before.
	2. In Namespaces that previously did not have the "DefaultDeny"
	   annotation, you should delete any existing NetworkPolicy
	   objects. These would have had no effect before, but with v1
	   semantics they might cause some traffic to be blocked that you
	   didn't intend to be blocked.

### Other notable changes

* kubectl logs with label selector supports specifying a container name ([#44282](https://github.com/kubernetes/kubernetes/pull/44282), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Adds an approval work flow to the the certificate approver that will approve certificate signing requests from kubelets that meet all the criteria of kubelet server certificates. ([#46884](https://github.com/kubernetes/kubernetes/pull/46884), [@jcbsmpsn](https://github.com/jcbsmpsn))
* AWS: Maintain a cache of all instances, to fix problem with > 200 nodes with ELBs ([#47410](https://github.com/kubernetes/kubernetes/pull/47410), [@justinsb](https://github.com/justinsb))
* Bump GLBC version to 0.9.5 - fixes [loss of manually modified GCLB health check settings](https://github.com/kubernetes/kubernetes/issues/47559) upon upgrade from pre-1.6.4 to either 1.6.4 or 1.6.5. ([#47567](https://github.com/kubernetes/kubernetes/pull/47567), [@nicksardo](https://github.com/nicksardo))
* Update cluster-proportional-autoscaler, metadata-proxy, and fluentd-gcp addons with fixes for CVE-2016-4448, CVE-2016-8859, CVE-2016-9841, CVE-2016-9843, and CVE-2017-9526. ([#47545](https://github.com/kubernetes/kubernetes/pull/47545), [@ixdy](https://github.com/ixdy))
* AWS: Batch DescribeInstance calls with nodeNames to 150 limit, to stay within AWS filter limits. ([#47516](https://github.com/kubernetes/kubernetes/pull/47516), [@gnufied](https://github.com/gnufied))
* AWS: Process disk attachments even with duplicate NodeNames ([#47406](https://github.com/kubernetes/kubernetes/pull/47406), [@justinsb](https://github.com/justinsb))
* kubefed will now configure NodeInternalIP as the federation API server endpoint when NodeExternalIP is unavailable for federation API servers exposed as NodePort services ([#46960](https://github.com/kubernetes/kubernetes/pull/46960), [@lukaszo](https://github.com/lukaszo))
* PodSecurityPolicy now recognizes pods that specify `runAsNonRoot: false` in their security context and does not overwrite the specified value ([#47073](https://github.com/kubernetes/kubernetes/pull/47073), [@Q-Lee](https://github.com/Q-Lee))
* Bump GLBC version to 0.9.4 ([#47468](https://github.com/kubernetes/kubernetes/pull/47468), [@nicksardo](https://github.com/nicksardo))
* Stackdriver Logging deployment exposes metrics on node port 31337 when enabled. ([#47402](https://github.com/kubernetes/kubernetes/pull/47402), [@crassirostris](https://github.com/crassirostris))
* Update to kube-addon-manager:v6.4-beta.2: kubectl v1.6.4 and refreshed base images ([#47389](https://github.com/kubernetes/kubernetes/pull/47389), [@ixdy](https://github.com/ixdy))
* Enable iptables -w in kubeadm selfhosted ([#46372](https://github.com/kubernetes/kubernetes/pull/46372), [@cmluciano](https://github.com/cmluciano))
* Azure plugin for client auth ([#43987](https://github.com/kubernetes/kubernetes/pull/43987), [@cosmincojocar](https://github.com/cosmincojocar))
* Fix dynamic provisioning of PVs with inaccurate AccessModes by refusing to provision when PVCs ask for AccessModes that can't be satisfied by the PVs' underlying volume plugin ([#47274](https://github.com/kubernetes/kubernetes/pull/47274), [@wongma7](https://github.com/wongma7))
* AWS: Avoid spurious ELB listener recreation - ignore case when matching protocol ([#47391](https://github.com/kubernetes/kubernetes/pull/47391), [@justinsb](https://github.com/justinsb))
* gce kube-up: The `Node` authorization mode and `NodeRestriction` admission controller are now enabled ([#46796](https://github.com/kubernetes/kubernetes/pull/46796), [@mikedanese](https://github.com/mikedanese))
* update gophercloud/gophercloud dependency for reauthentication fixes ([#45545](https://github.com/kubernetes/kubernetes/pull/45545), [@stuart-warren](https://github.com/stuart-warren))
* fix sync loop health check with separating runtime errors ([#47124](https://github.com/kubernetes/kubernetes/pull/47124), [@andyxning](https://github.com/andyxning))
* servicecontroller: Fix node selection logic on initial LB creation ([#45773](https://github.com/kubernetes/kubernetes/pull/45773), [@justinsb](https://github.com/justinsb))
* Fix iSCSI iSER mounting. ([#47281](https://github.com/kubernetes/kubernetes/pull/47281), [@mtanino](https://github.com/mtanino))
* StorageOS Volume Driver ([#42156](https://github.com/kubernetes/kubernetes/pull/42156), [@croomes](https://github.com/croomes))
    * [StorageOS](http://www.storageos.com) can be used as a storage provider for Kubernetes.  With StorageOS, capacity from local or attached storage is pooled across the cluster, providing converged infrastructure for cloud-native applications. 
* CRI has been moved to package `pkg/kubelet/apis/cri/v1alpha1/runtime`. ([#47113](https://github.com/kubernetes/kubernetes/pull/47113), [@feiskyer](https://github.com/feiskyer))
* Make gcp auth provider not to override the Auth header if it's already exits ([#45575](https://github.com/kubernetes/kubernetes/pull/45575), [@wanghaoran1988](https://github.com/wanghaoran1988))
* Allow pods to opt out of PodPreset mutation via an annotation on the pod. ([#44965](https://github.com/kubernetes/kubernetes/pull/44965), [@jpeeler](https://github.com/jpeeler))
* Add Traditional Chinese translation for kubectl ([#46559](https://github.com/kubernetes/kubernetes/pull/46559), [@warmchang](https://github.com/warmchang))
* Remove Initializers from admission-control in kubernetes-master charm for pre-1.7 ([#46987](https://github.com/kubernetes/kubernetes/pull/46987), [@Cynerva](https://github.com/Cynerva))
* Added state guards to the idle_status messaging in the kubernetes-master charm to make deployment faster on initial deployment. ([#47183](https://github.com/kubernetes/kubernetes/pull/47183), [@chuckbutler](https://github.com/chuckbutler))
* Bump up Node Problem Detector version to v0.4.0, which added support of parsing log from /dev/kmsg and ABRT. ([#46743](https://github.com/kubernetes/kubernetes/pull/46743), [@Random-Liu](https://github.com/Random-Liu))
* kubeadm: Enable the Node Authorizer/Admission plugin in v1.7  ([#46879](https://github.com/kubernetes/kubernetes/pull/46879), [@luxas](https://github.com/luxas))
* Deprecated Binding objects in 1.7. ([#47041](https://github.com/kubernetes/kubernetes/pull/47041), [@k82cn](https://github.com/k82cn))
* Add secretbox and AES-CBC encryption modes to at rest encryption.  AES-CBC is considered superior to AES-GCM because it is resistant to nonce-reuse attacks, and secretbox uses Poly1305 and XSalsa20. ([#46916](https://github.com/kubernetes/kubernetes/pull/46916), [@smarterclayton](https://github.com/smarterclayton))
* The HorizontalPodAutoscaler controller will now only send updates when it has new status information, reducing the number of writes caused by the controller. ([#47078](https://github.com/kubernetes/kubernetes/pull/47078), [@DirectXMan12](https://github.com/DirectXMan12))
* gpusInUse info error when kubelet restarts ([#46087](https://github.com/kubernetes/kubernetes/pull/46087), [@tianshapjq](https://github.com/tianshapjq))
* kubeadm: Modifications to cluster-internal resources installed by kubeadm will be overwritten when upgrading from v1.6 to v1.7. ([#47081](https://github.com/kubernetes/kubernetes/pull/47081), [@luxas](https://github.com/luxas))
* Added exponential backoff to Azure cloudprovider ([#46660](https://github.com/kubernetes/kubernetes/pull/46660), [@jackfrancis](https://github.com/jackfrancis))
* fixed HostAlias in PodSpec to allow `foo.bar` hostnames instead of just `foo` DNS labels. ([#46809](https://github.com/kubernetes/kubernetes/pull/46809), [@rickypai](https://github.com/rickypai))
* Implements rolling update for StatefulSets. Updates can be performed using the RollingUpdate, Paritioned, or OnDelete strategies. OnDelete implements the manual behavior from 1.6. status now tracks  ([#46669](https://github.com/kubernetes/kubernetes/pull/46669), [@kow3ns](https://github.com/kow3ns))
    * replicas, readyReplicas, currentReplicas, and updatedReplicas. The semantics of replicas is now consistent with DaemonSet and ReplicaSet, and readyReplicas has the semantics that replicas did prior to this release.
* Add Japanese translation for kubectl ([#46756](https://github.com/kubernetes/kubernetes/pull/46756), [@girikuncoro](https://github.com/girikuncoro))
* federation: Add admission controller for policy-based placement ([#44786](https://github.com/kubernetes/kubernetes/pull/44786), [@tsandall](https://github.com/tsandall))
* Get command uses OpenAPI schema to enhance display for a resource if run with flag 'use-openapi-print-columns'.  ([#46235](https://github.com/kubernetes/kubernetes/pull/46235), [@droot](https://github.com/droot))
    * An example command:
    * kubectl get pods --use-openapi-print-columns 
* add gzip compression to GET and LIST requests ([#45666](https://github.com/kubernetes/kubernetes/pull/45666), [@ilackarms](https://github.com/ilackarms))
* Fix the bug where container cannot run as root when SecurityContext.RunAsNonRoot is false. ([#47009](https://github.com/kubernetes/kubernetes/pull/47009), [@yujuhong](https://github.com/yujuhong))
* Fixes a bug with cAdvisorPort in the KubeletConfiguration that prevented setting it to 0, which is in fact a valid option, as noted in issue [#11710](https://github.com/kubernetes/kubernetes/pull/11710). ([#46876](https://github.com/kubernetes/kubernetes/pull/46876), [@mtaufen](https://github.com/mtaufen))
* Stackdriver cluster logging now deploys a new component to export Kubernetes events. ([#46700](https://github.com/kubernetes/kubernetes/pull/46700), [@crassirostris](https://github.com/crassirostris))
* Alpha feature: allows users to set storage limit to isolate EmptyDir volumes. It enforces the limit by evicting pods that exceed their storage limits   ([#45686](https://github.com/kubernetes/kubernetes/pull/45686), [@jingxu97](https://github.com/jingxu97))
* Adds the `Categories []string` field to API resources, which represents the list of group aliases (e.g. "all") that every resource belongs to.  ([#43338](https://github.com/kubernetes/kubernetes/pull/43338), [@fabianofranz](https://github.com/fabianofranz))
* Promote kubelet tls bootstrap to beta. Add a non-experimental flag to use it and deprecate the old flag. ([#46799](https://github.com/kubernetes/kubernetes/pull/46799), [@mikedanese](https://github.com/mikedanese))
* Fix disk partition discovery for brtfs ([#46816](https://github.com/kubernetes/kubernetes/pull/46816), [@dashpole](https://github.com/dashpole))
    * Add ZFS support
    * Add overlay2 storage driver support
* Support creation of GCP Internal Load Balancers from Service objects ([#46663](https://github.com/kubernetes/kubernetes/pull/46663), [@nicksardo](https://github.com/nicksardo))
* Introduces status conditions to the HorizontalPodAutoscaler in autoscaling/v2alpha1, indicating the current status of a given HorizontalPodAutoscaler, and why it is or is not scaling. ([#46550](https://github.com/kubernetes/kubernetes/pull/46550), [@DirectXMan12](https://github.com/DirectXMan12))
* Support OpenAPI spec aggregation for kube-aggregator ([#46734](https://github.com/kubernetes/kubernetes/pull/46734), [@mbohlool](https://github.com/mbohlool))
* Implement kubectl rollout undo and history for DaemonSet ([#46144](https://github.com/kubernetes/kubernetes/pull/46144), [@janetkuo](https://github.com/janetkuo))
* Respect PDBs during node upgrades and add test coverage to the ServiceTest upgrade test. ([#45748](https://github.com/kubernetes/kubernetes/pull/45748), [@mml](https://github.com/mml))
* Disk Pressure triggers the deletion of terminated containers on the node. ([#45896](https://github.com/kubernetes/kubernetes/pull/45896), [@dashpole](https://github.com/dashpole))
* Add the `alpha.image-policy.k8s.io/failed-open=true` annotation when the image policy webhook encounters an error and fails open. ([#46264](https://github.com/kubernetes/kubernetes/pull/46264), [@Q-Lee](https://github.com/Q-Lee))
* Enable kubelet csr bootstrap in GCE/GKE ([#40760](https://github.com/kubernetes/kubernetes/pull/40760), [@mikedanese](https://github.com/mikedanese))
* Implement Daemonset history ([#45924](https://github.com/kubernetes/kubernetes/pull/45924), [@janetkuo](https://github.com/janetkuo))
* When switching from the `service.beta.kubernetes.io/external-traffic` annotation to the new ([#46716](https://github.com/kubernetes/kubernetes/pull/46716), [@thockin](https://github.com/thockin))
    * `externalTrafficPolicy` field, the values chnag as follows:
          * "OnlyLocal" becomes "Local"
          * "Global" becomes "Cluster".
* Fix kubelet reset liveness probe failure count across pod restart boundaries ([#46371](https://github.com/kubernetes/kubernetes/pull/46371), [@sjenning](https://github.com/sjenning))
* The gce metadata server can be hidden behind a proxy, hiding the kubelet's token. ([#45565](https://github.com/kubernetes/kubernetes/pull/45565), [@Q-Lee](https://github.com/Q-Lee))
* AWS: Allow configuration of a single security group for ELBs ([#45500](https://github.com/kubernetes/kubernetes/pull/45500), [@nbutton23](https://github.com/nbutton23))
* Allow remote admission controllers to be dynamically added and removed by administrators.  External admission controllers make an HTTP POST containing details of the requested action which the service can approve or reject. ([#46388](https://github.com/kubernetes/kubernetes/pull/46388), [@lavalamp](https://github.com/lavalamp))
* iscsi storage plugin: Fix dangling session when using multiple target portal addresses. ([#46239](https://github.com/kubernetes/kubernetes/pull/46239), [@mtanino](https://github.com/mtanino))
* Duplicate recurring Events now include the latest event's Message string ([#46034](https://github.com/kubernetes/kubernetes/pull/46034), [@kensimon](https://github.com/kensimon))
* With --feature-gates=RotateKubeletClientCertificate=true set, the kubelet will ([#41912](https://github.com/kubernetes/kubernetes/pull/41912), [@jcbsmpsn](https://github.com/jcbsmpsn))
    * request a client certificate from the API server during the boot cycle and pause
    * waiting for the request to be satisfied. It will continually refresh the certificate
    * as the certificates expiration approaches.
* The Kubernetes API supports retrieving tabular output for API resources via a new mime-type `application/json;as=Table;v=v1alpha1;g=meta.k8s.io`.  The returned object (if the server supports it) will be of type `meta.k8s.io/v1alpha1` with `Table`, and contain column and row information related to the resource.  Each row will contain information about the resource - by default it will be the object metadata, but callers can add the `?includeObject=Object` query parameter and receive the full object.  In the future kubectl will use this to retrieve the results of `kubectl get`. ([#40848](https://github.com/kubernetes/kubernetes/pull/40848), [@smarterclayton](https://github.com/smarterclayton))
* This change add nonResourceURL to kubectl auth cani ([#46432](https://github.com/kubernetes/kubernetes/pull/46432), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Webhook added to the API server which omits structured audit log events. ([#45919](https://github.com/kubernetes/kubernetes/pull/45919), [@ericchiang](https://github.com/ericchiang))
* By default, --low-diskspace-threshold-mb is not set, and --eviction-hard includes "nodefs.available<10%,nodefs.inodesFree<5%" ([#46448](https://github.com/kubernetes/kubernetes/pull/46448), [@dashpole](https://github.com/dashpole))
* kubectl edit and kubectl apply will keep the ordering of elements in merged lists ([#45980](https://github.com/kubernetes/kubernetes/pull/45980), [@mengqiy](https://github.com/mengqiy))
* [Federation][kubefed]: Use StorageClassName for etcd pvc ([#46323](https://github.com/kubernetes/kubernetes/pull/46323), [@marun](https://github.com/marun))
* Restrict active deadline seconds max allowed value to be maximum uint32 ([#46640](https://github.com/kubernetes/kubernetes/pull/46640), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Implement kubectl get controllerrevisions ([#46655](https://github.com/kubernetes/kubernetes/pull/46655), [@janetkuo](https://github.com/janetkuo))
* Local storage plugin ([#44897](https://github.com/kubernetes/kubernetes/pull/44897), [@msau42](https://github.com/msau42))
* With `--feature-gates=RotateKubeletServerCertificate=true` set, the kubelet will ([#45059](https://github.com/kubernetes/kubernetes/pull/45059), [@jcbsmpsn](https://github.com/jcbsmpsn))
    * request a server certificate from the API server during the boot cycle and pause
    * waiting for the request to be satisfied. It will continually refresh the certificate as
    * the certificates expiration approaches.
* Allow PSP's to specify a whitelist of allowed paths for host volume based on path prefixes ([#43946](https://github.com/kubernetes/kubernetes/pull/43946), [@jhorwit2](https://github.com/jhorwit2))
* Add `kubectl config rename-context` ([#46114](https://github.com/kubernetes/kubernetes/pull/46114), [@arthur0](https://github.com/arthur0))
* Fix AWS EBS volumes not getting detached from node if routine to verify volumes are attached runs while the node is down ([#46463](https://github.com/kubernetes/kubernetes/pull/46463), [@wongma7](https://github.com/wongma7))
* Move hardPodAffinitySymmetricWeight to scheduler policy config ([#44159](https://github.com/kubernetes/kubernetes/pull/44159), [@wanghaoran1988](https://github.com/wanghaoran1988))
* AWS: support node port health check ([#43585](https://github.com/kubernetes/kubernetes/pull/43585), [@foolusion](https://github.com/foolusion))
* Add generic Toleration for NoExecute Taints to NodeProblemDetector ([#45883](https://github.com/kubernetes/kubernetes/pull/45883), [@gmarek](https://github.com/gmarek))
* support replaceKeys patch strategy and directive for strategic merge patch ([#44597](https://github.com/kubernetes/kubernetes/pull/44597), [@mengqiy](https://github.com/mengqiy))
* Augment CRI to support retrieving container stats from the runtime. ([#45614](https://github.com/kubernetes/kubernetes/pull/45614), [@yujuhong](https://github.com/yujuhong))
* Prevent kubelet from setting allocatable < 0 for a resource upon initial creation. ([#46516](https://github.com/kubernetes/kubernetes/pull/46516), [@derekwaynecarr](https://github.com/derekwaynecarr))
* add --non-resource-url to kubectl create clusterrole ([#45809](https://github.com/kubernetes/kubernetes/pull/45809), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Add `kubectl apply edit-last-applied` subcommand ([#42256](https://github.com/kubernetes/kubernetes/pull/42256), [@shiywang](https://github.com/shiywang))
* Adding admissionregistration API group which enables dynamic registration of initializers and external admission webhooks. It is an alpha feature. ([#46294](https://github.com/kubernetes/kubernetes/pull/46294), [@caesarxuchao](https://github.com/caesarxuchao))
* Fix log spam due to unnecessary status update when node is deleted. ([#45923](https://github.com/kubernetes/kubernetes/pull/45923), [@verult](https://github.com/verult))
* GCE installs will now avoid IP masquerade for all RFC-1918 IP blocks, rather than just 10.0.0.0/8.  This means that clusters can ([#46473](https://github.com/kubernetes/kubernetes/pull/46473), [@thockin](https://github.com/thockin))
    * be created in 192.168.0.0./16 and 172.16.0.0/12 while preserving the container IPs (which would be lost before).
* `set selector` and `set subject` no longer print "running in local/dry-run mode..." at the top, so their output can be piped as valid yaml or json ([#46507](https://github.com/kubernetes/kubernetes/pull/46507), [@bboreham](https://github.com/bboreham))
* ControllerRevision type added for StatefulSet and DaemonSet history. ([#45867](https://github.com/kubernetes/kubernetes/pull/45867), [@kow3ns](https://github.com/kow3ns))
* Bump Go version to 1.8.3 ([#46429](https://github.com/kubernetes/kubernetes/pull/46429), [@wojtek-t](https://github.com/wojtek-t))
* Upgrade Elasticsearch Addon to v5.4.0 ([#45589](https://github.com/kubernetes/kubernetes/pull/45589), [@it-svit](https://github.com/it-svit))
* PodDisruptionBudget now uses ControllerRef to decide which controller owns a given Pod, so it doesn't get confused by controllers with overlapping selectors. ([#45003](https://github.com/kubernetes/kubernetes/pull/45003), [@krmayankk](https://github.com/krmayankk))
* aws: Support for ELB tagging by users ([#45932](https://github.com/kubernetes/kubernetes/pull/45932), [@lpabon](https://github.com/lpabon))
* Portworx volume driver no longer has to run on the master. ([#45518](https://github.com/kubernetes/kubernetes/pull/45518), [@harsh-px](https://github.com/harsh-px))
* kube-proxy: ratelimit runs of iptables by sync-period flags ([#46266](https://github.com/kubernetes/kubernetes/pull/46266), [@thockin](https://github.com/thockin))
* Deployments are updated to use (1) a more stable hashing algorithm (fnv) than the previous one (adler) and (2) a hashing collision avoidance mechanism that will ensure new rollouts will not block on hashing collisions anymore. ([#44774](https://github.com/kubernetes/kubernetes/pull/44774), [@kargakis](https://github.com/kargakis))
* The Prometheus metrics for the kube-apiserver for tracking incoming API requests and latencies now return the `subresource` label for correctly attributing the type of API call. ([#46354](https://github.com/kubernetes/kubernetes/pull/46354), [@smarterclayton](https://github.com/smarterclayton))
* Add Simplified Chinese translation for kubectl ([#45573](https://github.com/kubernetes/kubernetes/pull/45573), [@shiywang](https://github.com/shiywang))
* The --namespace flag is now honored for in-cluster clients that have an empty configuration. ([#46299](https://github.com/kubernetes/kubernetes/pull/46299), [@ncdc](https://github.com/ncdc))
* Fix init container status reporting when active deadline is exceeded. ([#46305](https://github.com/kubernetes/kubernetes/pull/46305), [@sjenning](https://github.com/sjenning))
* Improves performance of Cinder volume attach/detach operations ([#41785](https://github.com/kubernetes/kubernetes/pull/41785), [@jamiehannaford](https://github.com/jamiehannaford))
* GCE and AWS dynamic provisioners extension: admins can configure zone(s) in which a persistent volume shall be created. ([#38505](https://github.com/kubernetes/kubernetes/pull/38505), [@pospispa](https://github.com/pospispa))
* Break the 'certificatesigningrequests' controller into a 'csrapprover' controller and 'csrsigner' controller. ([#45514](https://github.com/kubernetes/kubernetes/pull/45514), [@mikedanese](https://github.com/mikedanese))
* Modifies kubefed to create and the federation controller manager to use credentials associated with a service account rather than the user's credentials. ([#42042](https://github.com/kubernetes/kubernetes/pull/42042), [@perotinus](https://github.com/perotinus))
* Adds a MaxUnavailable field to PodDisruptionBudget ([#45587](https://github.com/kubernetes/kubernetes/pull/45587), [@foxish](https://github.com/foxish))
* The behavior of some watch calls to the server when filtering on fields was incorrect.  If watching objects with a filter, when an update was made that no longer matched the filter a DELETE event was correctly sent.  However, the object that was returned by that delete was not the (correct) version before the update, but instead, the newer version.  That meant the new object was not matched by the filter.  This was a regression from behavior between cached watches on the server side and uncached watches, and thus broke downstream API clients. ([#46223](https://github.com/kubernetes/kubernetes/pull/46223), [@smarterclayton](https://github.com/smarterclayton))
* vSphere cloud provider: vSphere Storage policy Support for dynamic volume provisioning ([#46176](https://github.com/kubernetes/kubernetes/pull/46176), [@BaluDontu](https://github.com/BaluDontu))
* Add support for emitting metrics from openstack cloudprovider about storage operations. ([#46008](https://github.com/kubernetes/kubernetes/pull/46008), [@NickrenREN](https://github.com/NickrenREN))
* 'kubefed init' now supports overriding the default etcd image name with the --etcd-image parameter. ([#46247](https://github.com/kubernetes/kubernetes/pull/46247), [@marun](https://github.com/marun))
* remove the elasticsearch template ([#45952](https://github.com/kubernetes/kubernetes/pull/45952), [@harryge00](https://github.com/harryge00))
* Adds the `CustomResourceDefinition` (crd) types to the `kube-apiserver`.  These are the successors to `ThirdPartyResource`.  See https://github.com/kubernetes/community/blob/master/contributors/design-proposals/api-machinery/thirdpartyresources.md for more details. ([#46055](https://github.com/kubernetes/kubernetes/pull/46055), [@deads2k](https://github.com/deads2k))
* StatefulSets now include an alpha scaling feature accessible by setting the `spec.podManagementPolicy` field to `Parallel`.  The controller will not wait for pods to be ready before adding the other pods, and will replace deleted pods as needed.  Since parallel scaling creates pods out of order, you cannot depend on predictable membership changes within your set. ([#44899](https://github.com/kubernetes/kubernetes/pull/44899), [@smarterclayton](https://github.com/smarterclayton))
* fix kubelet event recording for selected events. ([#46246](https://github.com/kubernetes/kubernetes/pull/46246), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Moved qos to api.helpers. ([#44906](https://github.com/kubernetes/kubernetes/pull/44906), [@k82cn](https://github.com/k82cn))
* Kubelet PLEG updates the relist timestamp only after successfully relisting. ([#45496](https://github.com/kubernetes/kubernetes/pull/45496), [@andyxning](https://github.com/andyxning))
* OpenAPI spec is now available in protobuf binary and gzip format (with ETag support) ([#45836](https://github.com/kubernetes/kubernetes/pull/45836), [@mbohlool](https://github.com/mbohlool))
* Added support to a hierarchy of kubectl plugins (a tree of plugins as children of other plugins). ([#45981](https://github.com/kubernetes/kubernetes/pull/45981), [@fabianofranz](https://github.com/fabianofranz))
    * Added exported env vars to kubectl plugins so that plugin developers have access to global flags, namespace, the plugin descriptor and the full path to the caller binary.
* Ignored mirror pods in PodPreset admission plugin. ([#45958](https://github.com/kubernetes/kubernetes/pull/45958), [@k82cn](https://github.com/k82cn))
* Don't try to attach volume to new node if it is already attached to another node and the volume does not support multi-attach. ([#45346](https://github.com/kubernetes/kubernetes/pull/45346), [@codablock](https://github.com/codablock))
* The Calico version included in kube-up for GCE has been updated to v2.2. ([#38169](https://github.com/kubernetes/kubernetes/pull/38169), [@caseydavenport](https://github.com/caseydavenport))
* Kubelet: Fix image garbage collector attempting to remove in-use images. ([#46121](https://github.com/kubernetes/kubernetes/pull/46121), [@Random-Liu](https://github.com/Random-Liu))
* Add ip-masq-agent addon to the addons folder which is used in GCE if  --non-masquerade-cidr is set to 0/0 ([#46038](https://github.com/kubernetes/kubernetes/pull/46038), [@dnardo](https://github.com/dnardo))
* Fix serialization of EnforceNodeAllocatable ([#44606](https://github.com/kubernetes/kubernetes/pull/44606), [@ivan4th](https://github.com/ivan4th))
* Add --write-config-to flag to kube-proxy to allow users to write the default configuration settings to a file. ([#45908](https://github.com/kubernetes/kubernetes/pull/45908), [@ncdc](https://github.com/ncdc))
* The `NodeRestriction` admission plugin limits the `Node` and `Pod` objects a kubelet can modify. In order to be limited by this admission plugin, kubelets must use credentials in the `system:nodes` group, with a username in the form `system:node:<nodeName>`. Such kubelets will only be allowed to modify their own `Node` API object, and only modify `Pod` API objects that are bound to their node. ([#45929](https://github.com/kubernetes/kubernetes/pull/45929), [@liggitt](https://github.com/liggitt))
* vSphere cloud provider: Report same Node IP as both internal and external. ([#45201](https://github.com/kubernetes/kubernetes/pull/45201), [@abrarshivani](https://github.com/abrarshivani))
* The options passed to a flexvolume plugin's mount command now contains the pod name (`kubernetes.io/pod.name`), namespace (`kubernetes.io/pod.namespace`), uid (`kubernetes.io/pod.uid`), and service account name (`kubernetes.io/serviceAccount.name`). ([#39488](https://github.com/kubernetes/kubernetes/pull/39488), [@liggitt](https://github.com/liggitt))
