<!-- BEGIN MUNGE: GENERATED_TOC -->
- [v1.7.12](#v1712)
  - [Changelog since v1.7.11](#changelog-since-v1711)
    - [Other notable changes](#other-notable-changes)
- [v1.7.11](#v1711)
  - [Changelog since v1.7.10](#changelog-since-v1710)
    - [Other notable changes](#other-notable-changes-1)
- [v1.7.10](#v1710)
  - [Changelog since v1.7.9](#changelog-since-v179)
    - [Other notable changes](#other-notable-changes-2)
- [v1.7.9](#v179)
  - [Changelog since v1.7.8](#changelog-since-v178)
    - [Other notable changes](#other-notable-changes-3)
- [v1.7.8](#v178)
  - [Changelog since v1.7.7](#changelog-since-v177)
    - [Other notable changes](#other-notable-changes-4)
- [v1.7.7](#v177)
  - [Changelog since v1.7.6](#changelog-since-v176)
    - [Other notable changes](#other-notable-changes-5)
- [v1.7.6](#v176)
  - [Changelog since v1.7.5](#changelog-since-v175)
    - [Other notable changes](#other-notable-changes-6)
- [v1.7.5](#v175)
  - [Changelog since v1.7.4](#changelog-since-v174)
    - [Other notable changes](#other-notable-changes-7)
- [v1.7.4](#v174)
  - [Changelog since v1.7.3](#changelog-since-v173)
    - [Other notable changes](#other-notable-changes-8)
- [v1.7.3](#v173)
  - [Changelog since v1.7.2](#changelog-since-v172)
    - [Other notable changes](#other-notable-changes-9)
- [v1.7.2](#v172)
  - [Changelog since v1.7.1](#changelog-since-v171)
    - [Other notable changes](#other-notable-changes-10)
- [v1.7.1](#v171)
  - [Changelog since v1.7.0](#changelog-since-v170)
    - [Other notable changes](#other-notable-changes-11)
- [v1.7.0](#v170)
  - [**Major Themes**](#major-themes)
  - [**Action Required Before Upgrading**](#action-required-before-upgrading)
    - [Network](#network)
    - [Storage](#storage)
    - [API Machinery](#api-machinery)
    - [Controller Manager](#controller-manager)
    - [kubectl (CLI)](#kubectl-cli)
    - [kubeadm](#kubeadm)
    - [Cloud Providers](#cloud-providers)
  - [**Known Issues**](#known-issues)
  - [**Deprecations**](#deprecations)
    - [Cluster provisioning scripts](#cluster-provisioning-scripts)
    - [Client libraries](#client-libraries)
    - [DaemonSet](#daemonset)
    - [kube-proxy](#kube-proxy)
    - [Namespace](#namespace)
    - [Scheduling](#scheduling)
  - [**Notable Features**](#notable-features)
  - [Kubefed](#kubefed)
    - [**Kubernetes API**](#kubernetes-api)
      - [User Provided Extensions](#user-provided-extensions)
    - [**Application Deployment**](#application-deployment)
      - [StatefulSet](#statefulset)
      - [DaemonSet](#daemonset-1)
      - [Deployments](#deployments)
      - [PodDisruptionBudget](#poddisruptionbudget)
    - [**Security**](#security)
      - [Admission Control](#admission-control)
      - [TLS Bootstrapping](#tls-bootstrapping)
      - [Audit Logging](#audit-logging)
      - [Encryption at Rest](#encryption-at-rest)
      - [Node Authorization](#node-authorization)
    - [**Application Autoscaling**](#application-autoscaling)
      - [Horizontal Pod Autoscaler](#horizontal-pod-autoscaler)
    - [**Cluster Lifecycle**](#cluster-lifecycle)
      - [kubeadm](#kubeadm-1)
      - [Cloud Provider Support](#cloud-provider-support)
    - [**Cluster Federation**](#cluster-federation)
      - [Placement Policy](#placement-policy)
      - [Cluster Selection](#cluster-selection)
    - [**Instrumentation**](#instrumentation)
      - [Core Metrics API](#core-metrics-api)
    - [**Internationalization**](#internationalization)
    - [**kubectl (CLI)**](#kubectl-cli-1)
    - [**Networking**](#networking)
      - [Network Policy](#network-policy)
      - [Load Balancing](#load-balancing)
    - [**Node Components**](#node-components)
      - [Container Runtime Interface](#container-runtime-interface)
    - [**Scheduling**](#scheduling-1)
      - [Scheduler Extender](#scheduler-extender)
    - [**Storage**](#storage-1)
      - [Local Storage](#local-storage)
      - [Volume Plugins](#volume-plugins)
      - [Metrics](#metrics)
    - [**Other notable changes**](#other-notable-changes-12)
      - [Admission plugin](#admission-plugin)
      - [API Machinery](#api-machinery-1)
      - [Application autoscaling](#application-autoscaling-1)
      - [Application Deployment](#application-deployment-1)
      - [Cluster Autoscaling](#cluster-autoscaling)
      - [Cloud Provider Enhancement](#cloud-provider-enhancement)
      - [Cluster Provisioning](#cluster-provisioning)
      - [Cluster federation](#cluster-federation-1)
      - [Credential provider](#credential-provider)
      - [Information for Kubernetes clients (openapi, swagger, client-go)](#information-for-kubernetes-clients-openapi-swagger-client-go)
      - [Instrumentation](#instrumentation-1)
      - [Internal storage layer](#internal-storage-layer)
      - [Kubernetes Dashboard](#kubernetes-dashboard)
      - [kube-dns](#kube-dns)
      - [kube-proxy](#kube-proxy-1)
      - [kube-scheduler](#kube-scheduler)
      - [Storage](#storage-2)
      - [Networking](#networking-1)
      - [Node controller](#node-controller)
      - [Node Components](#node-components-1)
      - [Scheduling](#scheduling-2)
      - [Security](#security-1)
      - [Scalability](#scalability)
  - [**External Dependency Version Information**](#external-dependency-version-information)
    - [Previous Releases Included in v1.7.0](#previous-releases-included-in-v170)
- [v1.7.0-rc.1](#v170-rc1)
  - [Changelog since v1.7.0-beta.2](#changelog-since-v170-beta2)
    - [Action Required](#action-required)
    - [Other notable changes](#other-notable-changes-13)
- [v1.7.0-beta.2](#v170-beta2)
  - [Changelog since v1.7.0-beta.1](#changelog-since-v170-beta1)
    - [Action Required](#action-required-1)
    - [Other notable changes](#other-notable-changes-14)
- [v1.7.0-beta.1](#v170-beta1)
  - [Changelog since v1.7.0-alpha.4](#changelog-since-v170-alpha4)
    - [Action Required](#action-required-2)
    - [Other notable changes](#other-notable-changes-15)
- [v1.7.0-alpha.4](#v170-alpha4)
  - [Changelog since v1.7.0-alpha.3](#changelog-since-v170-alpha3)
    - [Action Required](#action-required-3)
    - [Other notable changes](#other-notable-changes-16)
- [v1.7.0-alpha.3](#v170-alpha3)
  - [Changelog since v1.7.0-alpha.2](#changelog-since-v170-alpha2)
    - [Action Required](#action-required-4)
    - [Other notable changes](#other-notable-changes-17)
- [v1.7.0-alpha.2](#v170-alpha2)
  - [Changelog since v1.7.0-alpha.1](#changelog-since-v170-alpha1)
    - [Action Required](#action-required-5)
    - [Other notable changes](#other-notable-changes-18)
- [v1.7.0-alpha.1](#v170-alpha1)
  - [Changelog since v1.6.0](#changelog-since-v160)
    - [Other notable changes](#other-notable-changes-19)
<!-- END MUNGE: GENERATED_TOC -->

<!-- NEW RELEASE NOTES ENTRY -->


# v1.7.12

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.11

### Other notable changes

* fix azure disk storage account init issue ([#55927](https://github.com/kubernetes/kubernetes/pull/55927), [@andyzhangx](https://github.com/andyzhangx))
* Fixes a bug where if an error was returned that was not an `autorest.DetailedError` we would return `"not found", nil` which caused nodes to go to `NotReady` state. ([#57484](https://github.com/kubernetes/kubernetes/pull/57484), [@brendandburns](https://github.com/brendandburns))
* Retry 'connection refused' errors when setting up clusters on GCE. ([#57394](https://github.com/kubernetes/kubernetes/pull/57394), [@mborsz](https://github.com/mborsz))
* Retry 'connection refused' errors when setting up clusters on GCE. ([#57394](https://github.com/kubernetes/kubernetes/pull/57394), [@mborsz](https://github.com/mborsz))
* Retry 'connection refused' errors when setting up clusters on GCE. ([#57394](https://github.com/kubernetes/kubernetes/pull/57394), [@mborsz](https://github.com/mborsz))
* Fix a problem of not respecting TerminationGracePeriodSeconds of the Pods created by DaemonSet controller. ([#51279](https://github.com/kubernetes/kubernetes/pull/51279), [@kow3ns](https://github.com/kow3ns))
* BUG FIX: Check both name and ports for azure health probes ([#56918](https://github.com/kubernetes/kubernetes/pull/56918), [@feiskyer](https://github.com/feiskyer))
* Provides compatibility of fields SizeLimit in types.EmptyDirVolumeSource since v1.7.8 ([#56505](https://github.com/kubernetes/kubernetes/pull/56505), [@yue9944882](https://github.com/yue9944882))
* Fixes issue where masquerade rules are flushed in GCE k8s clusters. ([#56728](https://github.com/kubernetes/kubernetes/pull/56728), [@dnardo](https://github.com/dnardo))
* kubelet: fix bug where `runAsUser: MustRunAsNonRoot` strategy didn't reject a pod with a non-numeric `USER`. ([#56711](https://github.com/kubernetes/kubernetes/pull/56711), [@php-coder](https://github.com/php-coder))
* Fix a bug in GCE multizonal clusters where PersistentVolumes were sometimes created in zones without nodes. ([#52322](https://github.com/kubernetes/kubernetes/pull/52322), [@davidz627](https://github.com/davidz627))
* Fix validation of NetworkPolicy ([#56223](https://github.com/kubernetes/kubernetes/pull/56223), [@deads2k](https://github.com/deads2k))
* add GRS, RAGRS storage account type support for azure disk ([#55931](https://github.com/kubernetes/kubernetes/pull/55931), [@andyzhangx](https://github.com/andyzhangx))
* Fixes server name verification of aggregated API servers and webhook admission endpoints ([#56415](https://github.com/kubernetes/kubernetes/pull/56415), [@liggitt](https://github.com/liggitt))
* Fix a typo in prometheus-to-sd configuration, that drops some stackdriver metrics. ([#56473](https://github.com/kubernetes/kubernetes/pull/56473), [@loburm](https://github.com/loburm))
* Update jquery and bootstrap dependencies ([#56447](https://github.com/kubernetes/kubernetes/pull/56447), [@dashpole](https://github.com/dashpole))



# v1.7.11

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.10

### Other notable changes

* Bugfix: master startup script on GCP no longer fails randomly due to concurrent iptables invocations. ([#55945](https://github.com/kubernetes/kubernetes/pull/55945), [@x13n](https://github.com/x13n))
* Fix bug in mounting volumes with GlusterFS plugin ([#53292](https://github.com/kubernetes/kubernetes/pull/53292), [@humblec](https://github.com/humblec))
* Add /bin/tee symlink to bazel build for busybox, so that CI builds have /bin/tee ([#55417](https://github.com/kubernetes/kubernetes/pull/55417), [@justinsb](https://github.com/justinsb))
* Reduce log noise produced by prometheus-to-sd, by bumping it to version 0.2.2. ([#54635](https://github.com/kubernetes/kubernetes/pull/54635), [@loburm](https://github.com/loburm))
* Fix session affinity issue with external load balancer traffic when ExternalTrafficPolicy=Local. ([#55519](https://github.com/kubernetes/kubernetes/pull/55519), [@MrHohn](https://github.com/MrHohn))
* Add masquerading rules by default to GCE/GKE ([#55178](https://github.com/kubernetes/kubernetes/pull/55178), [@dnardo](https://github.com/dnardo))
* Azure cloudprovider: Fix controller manager crash issue on a manually created k8s cluster. ([#53694](https://github.com/kubernetes/kubernetes/pull/53694), [@andyzhangx](https://github.com/andyzhangx))
* Fix a bug where soft eviction would not trigger when the threshold was crossed ([#52046](https://github.com/kubernetes/kubernetes/pull/52046), [@dashpole](https://github.com/dashpole))
* Addon manager supports HA masters. ([#55782](https://github.com/kubernetes/kubernetes/pull/55782), [@x13n](https://github.com/x13n))
* Fixed 'Schedulercache is corrupted' error in kube-scheduler ([#55262](https://github.com/kubernetes/kubernetes/pull/55262), [@liggitt](https://github.com/liggitt))
* Fix hyperkube kubelet --experimental-dockershim ([#55335](https://github.com/kubernetes/kubernetes/pull/55335), [@ivan4th](https://github.com/ivan4th))
* fix azure pv crash due to volumeSource.ReadOnly value nil ([#54607](https://github.com/kubernetes/kubernetes/pull/54607), [@andyzhangx](https://github.com/andyzhangx))
* GCE: provide an option to disable docker's live-restore on COS/ubuntu ([#55260](https://github.com/kubernetes/kubernetes/pull/55260), [@yujuhong](https://github.com/yujuhong))
* Fix overlay2 container disk metrics for Docker ([#54958](https://github.com/kubernetes/kubernetes/pull/54958), [@dashpole](https://github.com/dashpole))



# v1.7.10

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.9

### Other notable changes

* Fix for service controller so that it won't retry on doNotRetry service update failure. ([#54184](https://github.com/kubernetes/kubernetes/pull/54184), [@MrHohn](https://github.com/MrHohn))
* [fluentd-gcp addon] Fluentd now runs in its own network, not in the host one. ([#54395](https://github.com/kubernetes/kubernetes/pull/54395), [@crassirostris](https://github.com/crassirostris))
* fix azure disk mount failure on coreos and some other distros ([#54334](https://github.com/kubernetes/kubernetes/pull/54334), [@andyzhangx](https://github.com/andyzhangx))
* Update busybox image link to gcr.io for kube-proxy. ([#53818](https://github.com/kubernetes/kubernetes/pull/53818), [@MrHohn](https://github.com/MrHohn))
* Restores the ability to apply network policy objects against the networking.k8s.io/v1 API ([#54106](https://github.com/kubernetes/kubernetes/pull/54106), [@liggitt](https://github.com/liggitt))
* Allow for configuring etcd hostname in the manifest ([#54403](https://github.com/kubernetes/kubernetes/pull/54403), [@wojtek-t](https://github.com/wojtek-t))
* fix a bug where disk pressure could trigger prematurely when using overlay2 ([#53684](https://github.com/kubernetes/kubernetes/pull/53684), [@dashpole](https://github.com/dashpole))



# v1.7.9

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.8

### Other notable changes

* Support German cloud for azure disk mount feature ([#50673](https://github.com/kubernetes/kubernetes/pull/50673), [@clement-buchart](https://github.com/clement-buchart))
* BugFix: Exited containers are not Garbage Collected by the kubelet while the pod is running ([#53167](https://github.com/kubernetes/kubernetes/pull/53167), [@dashpole](https://github.com/dashpole))
* Address a bug which allowed the horizontal pod autoscaler to allocate `desiredReplicas` > `maxReplicas` in certain instances. ([#53690](https://github.com/kubernetes/kubernetes/pull/53690), [@mattjmcnaughton](https://github.com/mattjmcnaughton))
* Use separate client for leader election in scheduler to avoid starving leader election by regular scheduler operations. ([#53793](https://github.com/kubernetes/kubernetes/pull/53793), [@wojtek-t](https://github.com/wojtek-t))
* fix azure disk mounter issue ([#52260](https://github.com/kubernetes/kubernetes/pull/52260), [@andyzhangx](https://github.com/andyzhangx))
* GCE: Fix issue deleting internal load balancers when the firewall resource may not exist. ([#53450](https://github.com/kubernetes/kubernetes/pull/53450), [@nicksardo](https://github.com/nicksardo))
* Fix compilation of k8s.io/apiextensions-apiserver ([#48036](https://github.com/kubernetes/kubernetes/pull/48036), [@hongchaodeng](https://github.com/hongchaodeng))


# v1.7.8

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.7

### Other notable changes

* Ignore pods marked for deletion that exceed their grace period in ResourceQuota ([#46542](https://github.com/kubernetes/kubernetes/pull/46542), [@derekwaynecarr](https://github.com/derekwaynecarr))
* kubelet to master communication when doing node status updates now has a timeout to prevent indefinite hangs ([#52176](https://github.com/kubernetes/kubernetes/pull/52176), [@liggitt](https://github.com/liggitt))
* Bumped Heapster version to 1.4.3 - more details https://github.com/kubernetes/heapster/releases/tag/v1.4.3 ([#53376](https://github.com/kubernetes/kubernetes/pull/53376), [@loburm](https://github.com/loburm))
* Delete the federation namespace from control plane instead of individual objects ([#51768](https://github.com/kubernetes/kubernetes/pull/51768), [@shashidharatd](https://github.com/shashidharatd))
* Bugfix: OpenAPI models may not get group-version-kind extension if kubernetes is vendored in another project (e.g. minikube). Kubectl 1.8 needs this extension to work with those projects. ([#53152](https://github.com/kubernetes/kubernetes/pull/53152), [@mbohlool](https://github.com/mbohlool))
* Fix for Nodes in vSphere lacking an InternalIP. ([#48760](https://github.com/kubernetes/kubernetes/pull/48760)) ([#49202](https://github.com/kubernetes/kubernetes/pull/49202), [@cbonte](https://github.com/cbonte))
* [fluentd-gcp addon] Update Stackdriver plugin to version 0.6.7 ([#52565](https://github.com/kubernetes/kubernetes/pull/52565), [@crassirostris](https://github.com/crassirostris))
* Fixes an issue with RBAC reconciliation that could cause duplicated subjects in some bootstrapped rolebindings on each restart of the API server. ([#53239](https://github.com/kubernetes/kubernetes/pull/53239), [@enj](https://github.com/enj))
* Restores redirect behavior for proxy subresources ([#52933](https://github.com/kubernetes/kubernetes/pull/52933), [@liggitt](https://github.com/liggitt))
* Fix panic in ControllerManager on GCE when it has a problem with creating external loadbalancer healthcheck ([#52646](https://github.com/kubernetes/kubernetes/pull/52646), [@gmarek](https://github.com/gmarek))
* custom resources that use unconventional pluralization now work properly with kubectl and garbage collection ([#50012](https://github.com/kubernetes/kubernetes/pull/50012), [@deads2k](https://github.com/deads2k))
* When performing a GET then PUT, the kube-apiserver must write the canonical representation of the object to etcd if the current value does not match. That allows external agents to migrate content in etcd from one API version to another, across different storage types, or across varying encryption levels. This fixes a bug introduced in 1.5 where we unintentionally stopped writing the newest data. ([#48394](https://github.com/kubernetes/kubernetes/pull/48394), [@smarterclayton](https://github.com/smarterclayton))



# v1.7.7

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.6

### Other notable changes

* Update kube-dns to 1.14.5 ([#53114](https://github.com/kubernetes/kubernetes/pull/53114), [@bowei](https://github.com/bowei))
* StatefulSet will now fill the `hostname` and `subdomain` fields if they're empty on existing Pods it owns. This allows it to self-correct the issue where StatefulSet Pod DNS entries disappear after upgrading to v1.7.x ([#48327](https://github.com/kubernetes/kubernetes/pull/48327)). ([#51199](https://github.com/kubernetes/kubernetes/pull/51199), [@kow3ns](https://github.com/kow3ns))
* Third Party Resource tests in the e2e suite were incorrectly marked as part of the conformance bucket.  They are alpha and are not required for conformance. ([#52823](https://github.com/kubernetes/kubernetes/pull/52823), [@smarterclayton](https://github.com/smarterclayton))
* fixes upgrade test to work with tightened validation of initializer names in 1.8 ([#52592](https://github.com/kubernetes/kubernetes/pull/52592), [@liggitt](https://github.com/liggitt))
* Fix inconsistent Prometheus cAdvisor metrics ([#51473](https://github.com/kubernetes/kubernetes/pull/51473), [@bboreham](https://github.com/bboreham))
* Fixed an issue reporting lack of progress for a deployment prematurely ([#52178](https://github.com/kubernetes/kubernetes/pull/52178), [@kargakis](https://github.com/kargakis))
* [fluentd-gcp addon] Bug with event-exporter leaking memory on metrics in clusters with CA is fixed. ([#52263](https://github.com/kubernetes/kubernetes/pull/52263), [@crassirostris](https://github.com/crassirostris))



# v1.7.6

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.5

### Other notable changes

* [fluentd-gcp addon] Fluentd will trim lines exceeding 100KB instead of dropping them. ([#52289](https://github.com/kubernetes/kubernetes/pull/52289), [@crassirostris](https://github.com/crassirostris))
* Cluster Autoscaler 0.6.2 ([#52359](https://github.com/kubernetes/kubernetes/pull/52359), [@mwielgus](https://github.com/mwielgus))
* Add --request-timeout to kube-apiserver to make global request timeout configurable. ([#51415](https://github.com/kubernetes/kubernetes/pull/51415), [@jpbetz](https://github.com/jpbetz))
* Fix credentials providers for docker sandbox image. ([#51870](https://github.com/kubernetes/kubernetes/pull/51870), [@feiskyer](https://github.com/feiskyer))
* Fix security holes in GCE metadata proxy. ([#51302](https://github.com/kubernetes/kubernetes/pull/51302), [@ihmccreery](https://github.com/ihmccreery))
* Fixed an issue looking up cronjobs when they existed in more than one API version ([#52227](https://github.com/kubernetes/kubernetes/pull/52227), [@liggitt](https://github.com/liggitt))
* Fixes an issue with upgrade requests made via pod/service/node proxy subresources sending a non-absolute HTTP request-uri to backends ([#52065](https://github.com/kubernetes/kubernetes/pull/52065), [@liggitt](https://github.com/liggitt))
* Fix a kube-controller-manager crash which can result when `--concurrent-resource-quota-syncs` is >1 and pods exist in the system containing certain alpha/beta annotation keys. ([#52092](https://github.com/kubernetes/kubernetes/pull/52092), [@ironcladlou](https://github.com/ironcladlou))
* Make logdump support kubemark and support gke with 'use_custom_instance_list' ([#51834](https://github.com/kubernetes/kubernetes/pull/51834), [@shyamjvs](https://github.com/shyamjvs))
* Fixes an issue with APIService auto-registration affecting rolling HA apiserver restarts that add or remove API groups being served. ([#51921](https://github.com/kubernetes/kubernetes/pull/51921), [@liggitt](https://github.com/liggitt))
* In GCE with COS, increase TasksMax for Docker service to raise cap on number of threads/processes used by containers. ([#51986](https://github.com/kubernetes/kubernetes/pull/51986), [@yujuhong](https://github.com/yujuhong))
* Fix providerID update validation ([#51761](https://github.com/kubernetes/kubernetes/pull/51761), [@karataliu](https://github.com/karataliu))
* Automated cherry pick of [#50381](https://github.com/kubernetes/kubernetes/pull/50381) to release-1.7 ([#51871](https://github.com/kubernetes/kubernetes/pull/51871), [@feiskyer](https://github.com/feiskyer))
* The `emptyDir.sizeLimit` field is now correctly omitted from API requests and responses when unset. ([#50163](https://github.com/kubernetes/kubernetes/pull/50163), [@jingxu97](https://github.com/jingxu97))
* Calico has been updated to v2.5, RBAC added, and is now automatically scaled when GCE clusters are resized. ([#51237](https://github.com/kubernetes/kubernetes/pull/51237), [@gunjan5](https://github.com/gunjan5))



# v1.7.5

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.4

### Other notable changes

* Bumped Heapster version to 1.4.2 - more details https://github.com/kubernetes/heapster/releases/tag/v1.4.2. ([#51620](https://github.com/kubernetes/kubernetes/pull/51620), [@piosz](https://github.com/piosz))
* Fix for Pod stuck in ContainerCreating with error "Volume is not yet attached according to node". ([#50806](https://github.com/kubernetes/kubernetes/pull/50806), [@verult](https://github.com/verult))
* Fixed controller manager crash by making it tolerant to discovery errors.([#49767](https://github.com/kubernetes/kubernetes/pull/49767), [@deads2k](https://github.com/deads2k))
* Finalizers are now honored on custom resources, and on other resources even when garbage collection is disabled via the apiserver flag `--enable-garbage-collector=false` ([#51469](https://github.com/kubernetes/kubernetes/pull/51469), [@ironcladlou](https://github.com/ironcladlou))
* Allow attach of volumes to multiple nodes for vSphere ([#51066](https://github.com/kubernetes/kubernetes/pull/51066), [@BaluDontu](https://github.com/BaluDontu))
* vSphere: Fix attach volume failing on the first try. ([#51217](https://github.com/kubernetes/kubernetes/pull/51217), [@BaluDontu](https://github.com/BaluDontu))
* azure: support retrieving access tokens via managed identity extension ([#48854](https://github.com/kubernetes/kubernetes/pull/48854), [@colemickens](https://github.com/colemickens))
* Fixed a bug in strategic merge patch that caused kubectl apply to error out under some conditions ([#50862](https://github.com/kubernetes/kubernetes/pull/50862), [@guoshimin](https://github.com/guoshimin))
* It is now posible to use flexVolumes to bind mount directories and files. ([#50596](https://github.com/kubernetes/kubernetes/pull/50596), [@adelton](https://github.com/adelton))
* StatefulSet: Fix "forbidden pod updates" error on Pods created prior to upgrading to 1.7. ([#48327](https://github.com/kubernetes/kubernetes/pull/48327)) ([#51149](https://github.com/kubernetes/kubernetes/pull/51149), [@kow3ns](https://github.com/kow3ns))
* Fixed regression in initial kubectl exec terminal dimensions ([#51127](https://github.com/kubernetes/kubernetes/pull/51127), [@chen-anders](https://github.com/chen-anders))
* Enforcement of fsGroup; enable ScaleIO multiple-instance volume mapping; default PVC capacity; alignment of PVC, PV, and volume names for dynamic provisioning ([#48999](https://github.com/kubernetes/kubernetes/pull/48999), [@vladimirvivien](https://github.com/vladimirvivien))



# v1.7.4

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.3

### Other notable changes

* Azure: Allow VNet to be in a separate Resource Group. ([#49725](https://github.com/kubernetes/kubernetes/pull/49725), [@sylr](https://github.com/sylr))
* Fix an issue where if a CSR is not approved initially by the SAR approver is not retried. ([#49788](https://github.com/kubernetes/kubernetes/pull/49788), [@mikedanese](https://github.com/mikedanese))
* Cluster Autoscaler - fixes issues with taints and updates kube-proxy cpu request. ([#50514](https://github.com/kubernetes/kubernetes/pull/50514), [@mwielgus](https://github.com/mwielgus))
* Bumped Heapster version to 1.4.1: ([#50642](https://github.com/kubernetes/kubernetes/pull/50642), [@piosz](https://github.com/piosz))
    * handle gracefully problem when kubelet reports duplicated stats for the same container (see [#47853](https://github.com/kubernetes/kubernetes/pull/47853)) on Heapster side
    * fixed bugs and improved performance in Stackdriver Sink
* fluentd-gcp addon: Fix a bug in the event-exporter, when repeated events were not sent to Stackdriver. ([#50511](https://github.com/kubernetes/kubernetes/pull/50511), [@crassirostris](https://github.com/crassirostris))
* Collect metrics from Heapster in Stackdriver mode. ([#50517](https://github.com/kubernetes/kubernetes/pull/50517), [@piosz](https://github.com/piosz))
* fixes a bug around using the Global config ElbSecurityGroup where Kuberentes would modify the passed in Security Group. ([#49805](https://github.com/kubernetes/kubernetes/pull/49805), [@nbutton23](https://github.com/nbutton23))
* Updates Cinder AttachDisk operation to be more reliable by delegating Detaches to volume manager. ([#50042](https://github.com/kubernetes/kubernetes/pull/50042), [@jingxu97](https://github.com/jingxu97))
* fixes kubefed's ability to create RBAC roles in version-skewed clusters ([#50537](https://github.com/kubernetes/kubernetes/pull/50537), [@liggitt](https://github.com/liggitt))
* Fix data race during addition of new CRD ([#50098](https://github.com/kubernetes/kubernetes/pull/50098), [@nikhita](https://github.com/nikhita))
* Fix bug in scheduler that caused initially unschedulable pods to stuck in Pending state forever. ([#50028](https://github.com/kubernetes/kubernetes/pull/50028), [@julia-stripe](https://github.com/julia-stripe))
* Fix incorrect retry logic in scheduler ([#50106](https://github.com/kubernetes/kubernetes/pull/50106), [@julia-stripe](https://github.com/julia-stripe))
* GCE: Bump GLBC version to 0.9.6 ([#50096](https://github.com/kubernetes/kubernetes/pull/50096), [@nicksardo](https://github.com/nicksardo))
* The NodeRestriction admission plugin now allows a node to evict pods bound to itself ([#48707](https://github.com/kubernetes/kubernetes/pull/48707), [@danielfm](https://github.com/danielfm))
* Fixed a bug in the API server watch cache, which could cause a missing watch event immediately after cache initialization. ([#49992](https://github.com/kubernetes/kubernetes/pull/49992), [@liggitt](https://github.com/liggitt))



# v1.7.3

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.2

### Other notable changes

* fix pdb validation bug on PodDisruptionBudgetSpec ([#48706](https://github.com/kubernetes/kubernetes/pull/48706), [@dixudx](https://github.com/dixudx))
* kubeadm: Fix join preflight check false negative ([#49825](https://github.com/kubernetes/kubernetes/pull/49825), [@erhudy](https://github.com/erhudy))
* Revert deprecation of vCenter port in vSphere Cloud Provider. ([#49689](https://github.com/kubernetes/kubernetes/pull/49689), [@divyenpatel](https://github.com/divyenpatel))
* Fluentd-gcp DaemonSet exposes different set of metrics. ([#48812](https://github.com/kubernetes/kubernetes/pull/48812), [@crassirostris](https://github.com/crassirostris))
* Fixed OpenAPI Description and Nickname of API objects with subresources ([#49357](https://github.com/kubernetes/kubernetes/pull/49357), [@mbohlool](https://github.com/mbohlool))
* Websocket requests to aggregated APIs now perform TLS verification using the service DNS name instead of the backend server's IP address, consistent with non-websocket requests. ([#49353](https://github.com/kubernetes/kubernetes/pull/49353), [@liggitt](https://github.com/liggitt))
* kubeadm: Fixes a small bug where `--config` and `--skip-*` flags couldn't be passed at the same time in validation. ([#49498](https://github.com/kubernetes/kubernetes/pull/49498), [@luxas](https://github.com/luxas))
* kubeadm: Don't set a specific `spc_t` SELinux label on the etcd Static Pod as that is more privs than etcd needs and due to that `spc_t` isn't compatible with some OSes. ([#49328](https://github.com/kubernetes/kubernetes/pull/49328), [@euank](https://github.com/euank))
* Websocket requests to aggregated APIs now perform TLS verification using the service DNS name instead of the backend server's IP address, consistent with non-websocket requests. ([#49353](https://github.com/kubernetes/kubernetes/pull/49353), [@liggitt](https://github.com/liggitt))
* `kubectl drain` no longer spins trying to delete pods that do not exist ([#49444](https://github.com/kubernetes/kubernetes/pull/49444), [@eparis](https://github.com/eparis))
* Fixes [#49418](https://github.com/kubernetes/kubernetes/pull/49418) where kube-controller-manager can panic on volume.CanSupport methods and enter a crash loop. ([#49420](https://github.com/kubernetes/kubernetes/pull/49420), [@gnufied](https://github.com/gnufied))
* Fix Cinder to support http status 300 in pagination ([#47602](https://github.com/kubernetes/kubernetes/pull/47602), [@rootfs](https://github.com/rootfs))
* Automated cherry pick of [#49079](https://github.com/kubernetes/kubernetes/pull/49079) upstream release 1.7 ([#49254](https://github.com/kubernetes/kubernetes/pull/49254), [@feiskyer](https://github.com/feiskyer))
* Fixed GlusterFS volumes taking too long to time out ([#48709](https://github.com/kubernetes/kubernetes/pull/48709), [@jsafrane](https://github.com/jsafrane))
* The IP address and port for kube-proxy metrics server is now configurable via flag `--metrics-bind-address` ([#48625](https://github.com/kubernetes/kubernetes/pull/48625), [@mrhohn](https://github.com/mrhohn))
  * Special notice for kube-proxy in 1.7+ (including 1.7.0):
    * Healthz server (/healthz) will be served on 0.0.0.0:10256 by default.
    * Metrics server (/metrics and /proxyMode) will be served on 127.0.0.1:10249 by default.
    * Metrics server will continue serving /healthz.


# v1.7.2

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.1

### Other notable changes

* Use port 20256 for node-problem-detector in standalone mode. ([#49316](https://github.com/kubernetes/kubernetes/pull/49316), [@ajitak](https://github.com/ajitak))
* GCE Cloud Provider: New created LoadBalancer type Service will have health checks for nodes by default if all nodes have version >= v1.7.2. ([#49330](https://github.com/kubernetes/kubernetes/pull/49330), [@MrHohn](https://github.com/MrHohn))
* Azure PD (Managed/Blob) ([#46360](https://github.com/kubernetes/kubernetes/pull/46360), [@khenidak](https://github.com/khenidak))
* Fix Pods using Portworx volumes getting stuck in ContainerCreating phase. ([#48898](https://github.com/kubernetes/kubernetes/pull/48898), [@harsh-px](https://github.com/harsh-px))
* kubeadm: Make kube-proxy tolerate the external cloud provider taint so that an external cloud provider can be easily used on top of kubeadm ([#49017](https://github.com/kubernetes/kubernetes/pull/49017), [@luxas](https://github.com/luxas))
* Fix pods failing to start when subPath is a dangling symlink from kubelet point of view, which can happen if it is running inside a container ([#48555](https://github.com/kubernetes/kubernetes/pull/48555), [@redbaron](https://github.com/redbaron))
* Never prevent deletion of resources as part of namespace lifecycle ([#48733](https://github.com/kubernetes/kubernetes/pull/48733), [@liggitt](https://github.com/liggitt))
* kubectl: Fix bug that showed terminated/evicted pods even without `--show-all`. ([#48786](https://github.com/kubernetes/kubernetes/pull/48786), [@janetkuo](https://github.com/janetkuo))
* Add a runtime warning about the kubeadm default token TTL changes. ([#48838](https://github.com/kubernetes/kubernetes/pull/48838), [@mattmoyer](https://github.com/mattmoyer))
* Local storage teardown fix ([#48402](https://github.com/kubernetes/kubernetes/pull/48402), [@ianchakeres](https://github.com/ianchakeres))
* Fix udp service blackhole problem when number of backends changes from 0 to non-0 ([#48524](https://github.com/kubernetes/kubernetes/pull/48524), [@freehan](https://github.com/freehan))
* hpa: Prevent scaling below MinReplicas if desiredReplicas is zero ([#48997](https://github.com/kubernetes/kubernetes/pull/48997), [@johanneswuerbach](https://github.com/johanneswuerbach))
* kubeadm: Fix a bug where `kubeadm join` would wait 5 seconds without doing anything. Now `kubeadm join` executes the tasks immediately. ([#48737](https://github.com/kubernetes/kubernetes/pull/48737), [@mattmoyer](https://github.com/mattmoyer))
* Fix a regression that broke the `--config` flag for `kubeadm init`. ([#48915](https://github.com/kubernetes/kubernetes/pull/48915), [@mattmoyer](https://github.com/mattmoyer))
* Fix service controller crash loop when Service with GCP LoadBalancer uses static IP ([#48848](https://github.com/kubernetes/kubernetes/pull/48848), [@nicksardo](https://github.com/nicksardo)) ([#48849](https://github.com/kubernetes/kubernetes/pull/48849), [@nicksardo](https://github.com/nicksardo))



# v1.7.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.0

### Other notable changes

* Added new flag to `kubeadm init`: --node-name, that lets you specify the name of the Node object that will be created ([#48594](https://github.com/kubernetes/kubernetes/pull/48594), [@GheRivero](https://github.com/GheRivero))
* Added new flag to `kubeadm join`: --node-name, that lets you specify the name of the Node object that's gonna be created ([#48538](https://github.com/kubernetes/kubernetes/pull/48538), [@GheRivero](https://github.com/GheRivero))
* Fixes issue where you could not mount NFS or glusterFS volumes using hostnames on GCI/GKE with COS images. ([#42376](https://github.com/kubernetes/kubernetes/pull/42376), [@jingxu97](https://github.com/jingxu97))
* Reduce amount of noise in Stackdriver Logging, generated by the event-exporter component in the fluentd-gcp addon. ([#48712](https://github.com/kubernetes/kubernetes/pull/48712), [@crassirostris](https://github.com/crassirostris))
* Add generic NoSchedule toleration to fluentd in gcp config. ([#48182](https://github.com/kubernetes/kubernetes/pull/48182), [@gmarek](https://github.com/gmarek))
* RBAC role and role-binding reconciliation now ensures namespaces exist when reconciling on startup. ([#48480](https://github.com/kubernetes/kubernetes/pull/48480), [@liggitt](https://github.com/liggitt))
* Support NoSchedule taints correctly in DaemonSet controller. ([#48189](https://github.com/kubernetes/kubernetes/pull/48189), [@mikedanese](https://github.com/mikedanese))
* kubeadm: Expose only the cluster-info ConfigMap in the kube-public ns ([#48050](https://github.com/kubernetes/kubernetes/pull/48050), [@luxas](https://github.com/luxas))



# v1.7.0

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## **Major Themes**

Kubernetes 1.7 is a milestone release that adds security, stateful application, and extensibility features motivated by widespread production use of Kubernetes.

Security enhancements in this release include encrypted secrets (alpha), network policy for pod-to-pod communication, the node authorizer to limit Kubelet access to API resources, and Kubelet client / server TLS certificate rotation (alpha).  

Major features for stateful applications include automated updates to StatefulSets, enhanced updates for DaemonSets, a burst mode for faster StatefulSets scaling, and (alpha) support for local storage.

Extensibility features include API aggregation (beta), CustomResourceDefinitions (beta) in favor of ThirdPartyResources, support for extensible admission controllers (alpha), pluggable cloud providers (alpha), and container runtime interface (CRI) enhancements.

## **Action Required Before Upgrading**

### Network

* NetworkPolicy has been promoted from extensions/v1beta1 to the new networking.k8s.io/v1 API group. The structure remains unchanged from the v1beta1 API. The net.beta.kubernetes.io/network-policy annotation on Namespaces (used to opt in to isolation) has been removed. Instead, isolation is now determined on a per-pod basis. A NetworkPolicy may target a pod for isolation by including the pod in its spec.podSelector. Targeted Pods accept the traffic specified in the respective NetworkPolicy (and nothing else). Pods not targeted by any NetworkPolicy accept all traffic by default. ([#39164](https://github.com/kubernetes/kubernetes/pull/39164), [@danwinship](https://github.com/danwinship))

	**Action Required:** When upgrading to Kubernetes 1.7 (and a [network plugin](https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/) that supports the new NetworkPolicy v1 semantics), you should consider the following.

	The v1beta1 API used an annotation on Namespaces to activate the DefaultDeny policy for an entire Namespace. To activate default deny in the v1 API, you can create a NetworkPolicy that matches all Pods but does not allow any traffic:

    ```yaml
    kind: NetworkPolicy
    apiVersion: networking.k8s.io/v1
    metadata:
      name: default-deny
    spec:
      podSelector:
    ```

	This will ensure that Pods that aren't matched by any other NetworkPolicy will continue to be fully-isolated, as they were in v1beta1.

	In Namespaces that previously did not have the "DefaultDeny" annotation, you should delete any existing NetworkPolicy objects. These had no effect in the v1beta1 API, but with v1 semantics they might cause some traffic to be unintentionally blocked.


### Storage

* Alpha volume provisioning is removed and default storage class should be used instead. ([#44090](https://github.com/kubernetes/kubernetes/pull/44090), [@NickrenREN](https://github.com/NickrenREN))

* Portworx volume driver no longer has to run on the master. ([#45518](https://github.com/kubernetes/kubernetes/pull/45518), [@harsh-px](https://github.com/harsh-px))

* Default behavior in Cinder storageclass is changed. If availability is not specified, the zone is chosen by algorithm. It makes possible to spread stateful pods across many zones. ([#44798](https://github.com/kubernetes/kubernetes/pull/44798), [@zetaab](https://github.com/zetaab))

* PodSpecs containing parent directory references such as `..` (for example, `../bar`) in hostPath volume path or in volumeMount subpaths must be changed to the simple absolute path. Backsteps `..` are no longer allowed.([#47290](https://github.com/kubernetes/kubernetes/pull/47290), [@jhorwit2](https://github.com/jhorwit2)).


### API Machinery

* The Namespace API object no longer supports the deletecollection operation. ([#46407](https://github.com/kubernetes/kubernetes/pull/46407), [@liggitt](https://github.com/liggitt))

* The following alpha API groups were unintentionally enabled by default in previous releases, and will no longer be enabled by default in v1.8: ([#47690](https://github.com/kubernetes/kubernetes/pull/47690), [@caesarxuchao](https://github.com/caesarxuchao))

    * rbac.authorization.k8s.io/v1alpha1

    * settings.k8s.io/v1alpha1

    * If you wish to continue using them in v1.8, please enable them explicitly using the `--runtime-config` flag on the apiserver (for example, `--runtime-config="rbac.authorization.k8s.io/v1alpha1,settings.k8s.io/v1alpha1"`)

* `cluster/update-storage-objects.sh` now supports updating StorageClasses in etcd to storage.k8s.io/v1. You must do this prior to upgrading to 1.8. ([#46116](https://github.com/kubernetes/kubernetes/pull/46116), [@ncdc](https://github.com/ncdc))


### Controller Manager

* kube-controller-manager has dropped support for the `--insecure-experimental-approve-all-kubelet-csrs-for-group` flag. It is accepted in 1.7, but ignored. Instead, the csrapproving controller uses authorization checks to determine whether to approve certificate signing requests: ([#45619](https://github.com/kubernetes/kubernetes/pull/45619), [@mikedanese](https://github.com/mikedanese))

    * Before upgrading, users must ensure their controller manager will enable the csrapproving controller, create an RBAC ClusterRole and ClusterRoleBinding to approve CSRs for the same group, then upgrade. Example roles to enable the equivalent behavior can be found in the [TLS bootstrapping](https://kubernetes.io/docs/admin/kubelet-tls-bootstrapping/) documentation.


### kubectl (CLI)
* `kubectl create role` and  `kubectl create clusterrole`  invocations must be updated to specify multiple resource names as repeated  `--resource-name` arguments instead of comma-separated arguments to a single `--resource-name` argument. E.g. `--resource-name=x,y` must become `--resource-name x --resource-name y` ([#44950](https://github.com/kubernetes/kubernetes/pull/44950), [@xilabao](https://github.com/xilabao))

* `kubectl create rolebinding` and `kubectl create clusterrolebinding` invocations must be updated to  specify multiple subjects as repeated  `--user`, `--group`, or `--serviceaccount` arguments instead of comma-separated arguments to a single `--user`, `--group`, or `--serviceaccount`.  E.g. `--user=x,y` must become `--user x --user y`  ([#43903](https://github.com/kubernetes/kubernetes/pull/43903), [@xilabao](https://github.com/xilabao))


### kubeadm

* kubeadm: Modifications to cluster-internal resources installed by kubeadm will be overwritten when upgrading from v1.6 to v1.7. ([#47081](https://github.com/kubernetes/kubernetes/pull/47081), [@luxas](https://github.com/luxas))

* kubeadm deb/rpm packages: cAdvisor doesn't listen on `0.0.0.0:4194` without authentication/authorization because of the possible information leakage. The cAdvisor API can still be accessed via `https://{node-ip}:10250/stats/`, though. ([kubernetes/release#356](https://github.com/kubernetes/release/pull/356), [@luxas](https://github.com/luxas))


### Cloud Providers

* Azure: Container permissions for provisioned volumes have changed to private. If you have existing Azure volumes that were created by Kubernetes v1.6.0-v1.6.5, you should change the permissions on them manually. ([#47605](https://github.com/kubernetes/kubernetes/pull/47605), [@brendandburns](https://github.com/brendandburns))

* GKE/GCE: New and upgraded 1.7 GCE/GKE clusters no longer have an RBAC ClusterRoleBinding that grants the cluster-admin ClusterRole to the default service account in the kube-system Namespace. ([#46750](https://github.com/kubernetes/kubernetes/pull/46750), [@cjcullen](https://github.com/cjcullen)). If this permission is still desired, run the following command to explicitly grant it, either before or after upgrading to 1.7:
    ```
    kubectl create clusterrolebinding kube-system-default --serviceaccount=kube-system:default --clusterrole=cluster-admin
    ```

## **Known Issues**

Populated via [v1.7.x known issues / FAQ accumulator](https://github.com/kubernetes/kubernetes/issues/46733)

* The kube-apiserver discovery APIs (for example, `/apis`) return information about the API groups being served, and can change dynamically.
During server startup, prior to the server reporting healthy (via `/healthz`), not all API groups may be reported.
Wait for the server to report healthy (via `/healthz`) before depending on the information provided by the discovery APIs.
Additionally, since the information returned from the discovery APIs may change dynamically, a cache of the results should not be considered authoritative.
ETag support is planned in a future version to facilitate client caching.
([#47977](https://github.com/kubernetes/kubernetes/pull/47977), [#44957](https://github.com/kubernetes/kubernetes/pull/44957))

* The DaemonSet controller will evict running Pods that do not tolerate the NoSchedule taint if the taint is added to a Node.  There is an open PR ([#48189](https://github.com/kubernetes/kubernetes/pull/48189)) to resolve this issue, but as this issue also exists in 1.6, and as we do not wish to risk release stability by merging it directly prior to a release without sufficient testing, we have decided to defer merging the PR until the next point release for each minor version ([#48190](https://github.com/kubernetes/kubernetes/pull/48190)).

* Protobuf serialization does not distinguish between `[]` and `null`.
API fields previously capable of storing and returning either `[]` and `null` via JSON API requests (for example, the Endpoints `subsets` field)
can now store only `null` when created using the protobuf content-type or stored in etcd using protobuf serialization (the default in 1.6).
JSON API clients should tolerate `null` values for such fields, and treat `null` and `[]` as equivalent in meaning unless specifically documented otherwise for a particular field. ([#44593](https://github.com/kubernetes/kubernetes/pull/44593))

* Local volume source paths that are directories and not mount points fail to unmount.  A fix is in process ([#48331](https://github.com/kubernetes/kubernetes/issues/48331)).

* Services of type LoadBalancer (on GCE/GKE) that have static IP addresses will cause the Service Controller to panic and thereby causing the kube-controller-manager to crash loop.
([#48848](https://github.com/kubernetes/kubernetes/issues/48848))

## **Deprecations**

### Cluster provisioning scripts
* cluster/ubuntu: Removed due to [deprecation](https://github.com/kubernetes/kubernetes/tree/master/cluster#cluster-configuration) and lack of maintenance. ([#44344](https://github.com/kubernetes/kubernetes/pull/44344), [@mikedanese](https://github.com/mikedanese))

* cluster/aws: Removed due to [deprecation](https://github.com/kubernetes/kubernetes/pull/38772) and lack of maintenance. ([#42196](https://github.com/kubernetes/kubernetes/pull/42196), [@zmerlynn](https://github.com/zmerlynn))


### Client libraries
* Swagger 1.2 spec (`/swaggerapi/*`) is deprecated. Please use OpenAPI instead.

### DaemonSet
* DaemonSet’s spec.templateGeneration has been deprecated.  ([#45924](https://github.com/kubernetes/kubernetes/pull/45924), [@janetkuo](https://github.com/janetkuo))

### kube-proxy
* In 1.7, the kube-proxy component has been converted to use a configuration file. The old flags still work in 1.7, but they are being deprecated and will be removed in a future release. Cluster administrators are advised to switch to using the configuration file, but no action is strictly necessary in 1.7. ([#34727](https://github.com/kubernetes/kubernetes/pull/34727), [@ncdc](https://github.com/ncdc))

### Namespace
* The Namespace API object no longer supports the deletecollection operation. ([#46407](https://github.com/kubernetes/kubernetes/pull/46407), [@liggitt](https://github.com/liggitt))


### Scheduling
* If you are using `AffinityInAnnotations=true` in `--feature-gates`, then the 1.7 release is your last opportunity to convert from specifying affinity/anti-affinity using the scheduler.alpha.kubernetes.io/affinity annotation on Pods, to using the Affinity field of PodSpec. Support for the alpha version of node and pod affinity (which uses the scheduler.alpha.kubernetes.io/affinity annotations on Pods) is going away **in Kubernetes 1.8** (not this release, but the next release). If you have not enabled AffinityInAnnotations=true in `--feature-gates`, then this change does not affect you.

## **Notable Features**

Features for this release were tracked via the use of the [kubernetes/features](https://github.com/kubernetes/features) issues repo. Each Feature issue is owned by a Special Interest Group from [kubernetes/community](https://github.com/kubernetes/community)

## Kubefed

* Deprecate the `--secret-name` flag from `kubefed join`, instead generating the secret name arbitrarily. ([#42513](https://github.com/kubernetes/kubernetes/pull/42513), [@perotinus](https://github.com/perotinus))


### **Kubernetes API**
#### User Provided Extensions
* [beta] ThirdPartyResource is deprecated. Please migrate to the successor, CustomResourceDefinition. For more information, see [Custom Resources](https://kubernetes.io/docs/concepts/api-extension/custom-resources/) and [Migrate a ThirdPartyResource to CustomResourceDefinition](https://kubernetes.io/docs/tasks/access-kubernetes-api/migrate-third-party-resource/).

* [beta] User-provided apiservers can be aggregated (served along with) the rest of the Kubernetes API. See [Extending the Kubernetes API with the aggregation layer](https://kubernetes.io/docs/concepts/api-extension/apiserver-aggregation/), [Configure the aggregation layer](https://kubernetes.io/docs/tasks/access-kubernetes-api/configure-aggregation-layer/), and [Setup an extension API server](https://kubernetes.io/docs/tasks/access-kubernetes-api/setup-extension-api-server/).

* [alpha] Adding admissionregistration API group which enables dynamic registration of initializers and external admission webhooks. ([#46294](https://github.com/kubernetes/kubernetes/pull/46294), [@caesarxuchao](https://github.com/caesarxuchao))


### **Application Deployment**
#### StatefulSet
* [beta] StatefulSet supports [RollingUpdate](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#rolling-updates) and [OnDelete](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#on-delete) update strategies.

* [alpha] StatefulSet authors should be able to relax the [ordering](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#orderedready-pod-management) and [parallelism](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#parallel-pod-management) policies for software that can safely support rapid, out-of-order changes.

#### DaemonSet
* [beta] DaemonSet supports history and rollback. See [Performing a Rollback on a DaemonSet](https://kubernetes.io/docs/tasks/manage-daemon/rollback-daemon-set/).

#### Deployments
* [beta] Deployments uses a hashing collision avoidance mechanism that ensures new rollouts will not block on hashing collisions anymore. ([kubernetes/features#287](https://github.com/kubernetes/features/issues/287))

#### PodDisruptionBudget
* [beta] PodDisruptionBudget has a new field MaxUnavailable, which allows users to specify the maximum number of disruptions that can be tolerated during eviction. For more information, see [Pod Disruptions](https://kubernetes.io/docs/concepts/workloads/pods/disruptions/) and [Specifying a Disruption Budget for your Application](https://kubernetes.io/docs/tasks/run-application/configure-pdb/).
* PodDisruptionBudget now uses [ControllerRef](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/api-machinery/controller-ref.md) to make the right decisions about Pod eviction even if the built in application controllers have overlapping selectors.

### **Security**
#### Admission Control
* [alpha] Add [extensible external admission control](https://kubernetes.io/docs/admin/extensible-admission-controllers/).

#### TLS Bootstrapping
* [alpha] Rotation of the server TLS certificate on the kubelet. See [TLS bootstrapping - approval controller](https://kubernetes.io/docs/admin/kubelet-tls-bootstrapping/#approval-controller).

* [alpha] Rotation of the client TLS certificate on the kubelet. See [TLS bootstrapping - kubelet configuration](https://kubernetes.io/docs/admin/kubelet-tls-bootstrapping/#kubelet-configuration).

* [beta] [Kubelet TLS Bootstrap](https://kubernetes.io/docs/admin/kubelet-tls-bootstrapping/#kubelet-configuration)

#### Audit Logging
* [alpha] Advanced Auditing enhances the Kubernetes API [audit logging](https://kubernetes.io/docs/tasks/debug-application-cluster/audit/#audit-logs) capabilities through a customizable policy, pluggable audit backends, and richer audit data.

#### Encryption at Rest
* [alpha] Encrypt secrets stored in etcd. For more information, see [Securing a Cluster](https://kubernetes.io/docs/tasks/administer-cluster/securing-a-cluster/) and [Encrypting data at rest](https://kubernetes.io/docs/tasks/administer-cluster/encrypt-data/).

#### Node Authorization
* [beta] A new Node authorization mode and NodeRestriction admission plugin, when used in combination, limit nodes' access to specific APIs, so that they may only modify their own Node API object, only modify Pod objects bound to themselves, and only retrieve secrets and configmaps referenced by pods bound to themselves. See [Using Node Authorization](https://kubernetes.io/docs/admin/authorization/node/) for more information.


### **Application Autoscaling**
#### Horizontal Pod Autoscaler
* [alpha] [HPA Status Conditions](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/#appendix-horizontal-pod-autoscaler-status-conditions).


### **Cluster Lifecycle**
#### kubeadm
* [alpha] Manual [upgrades for kubeadm from v1.6 to v1.7](https://kubernetes.io/docs/tasks/administer-cluster/kubeadm-upgrade-1-7/). Automated upgrades ([kubernetes/features#296](https://github.com/kubernetes/features/issues/296)) are targeted for v1.8.

#### Cloud Provider Support
* [alpha] Improved support for out-of-tree and out-of-process cloud providers, a.k.a pluggable cloud providers. See [Build and Run cloud-controller-manager](https://kubernetes.io/docs/tasks/administer-cluster/running-cloud-controller) documentation.


### **Cluster Federation**
#### Placement Policy
* [alpha] The federation-apiserver now supports a SchedulingPolicy admission controller that enables policy-based control over placement of federated resources. For more information, see [Set up placement policies in Federation](https://kubernetes.io/docs/tasks/federation/set-up-placement-policies-federation/).

#### Cluster Selection
* [alpha] Federation [ClusterSelector annotation](https://kubernetes.io/docs/tasks/administer-federation/cluster/#clusterselector-annotation) to direct objects to federated clusters with matching labels.


### **Instrumentation**
#### Core Metrics API
* [alpha] Introduces a lightweight monitoring component for serving the core resource metrics API used by the Horizontal Pod Autoscaler and other components ([kubernetes/features#271](https://github.com/kubernetes/features/issues/271))


### **Internationalization**

* Add Traditional Chinese translation for kubectl ([#46559](https://github.com/kubernetes/kubernetes/pull/46559), [@warmchang](https://github.com/warmchang))

* Add Japanese translation for kubectl ([#46756](https://github.com/kubernetes/kubernetes/pull/46756), [@girikuncoro](https://github.com/girikuncoro))

* Add Simplified Chinese translation for kubectl ([#45573](https://github.com/kubernetes/kubernetes/pull/45573), [@shiywang](https://github.com/shiywang))

### **kubectl (CLI)**
* Features

  * `kubectl logs` supports specifying a container name when using label selectors ([#44282](https://github.com/kubernetes/kubernetes/pull/44282), [@derekwaynecarr](https://github.com/derekwaynecarr))

  * `kubectl rollout` supports undo and history for DaemonSet ([#46144](https://github.com/kubernetes/kubernetes/pull/46144), [@janetkuo](https://github.com/janetkuo))

  * `kubectl rollout` supports status and history for StatefulSet  ([#46669](https://github.com/kubernetes/kubernetes/pull/46669), [@kow3ns](https://github.com/kow3ns)).

  * Implement `kubectl get controllerrevisions` ([#46655](https://github.com/kubernetes/kubernetes/pull/46655), [@janetkuo](https://github.com/janetkuo))

  * `kubectl create clusterrole` supports `--non-resource-url` ([#45809](https://github.com/kubernetes/kubernetes/pull/45809), [@CaoShuFeng](https://github.com/CaoShuFeng))

  * `kubectl logs` and `kubectl attach` support specifying a wait timeout with `--pod-running-timeout` ([#41813](https://github.com/kubernetes/kubernetes/pull/41813), [@shiywang](https://github.com/shiywang))

  * New commands

    * Add `kubectl config rename-context` ([#46114](https://github.com/kubernetes/kubernetes/pull/46114), [@arthur0](https://github.com/arthur0))

    * Add `kubectl apply edit-last-applied` subcommand ([#42256](https://github.com/kubernetes/kubernetes/pull/42256), [@shiywang](https://github.com/shiywang))

  * Strategic Merge Patch

    * Reference docs now display the patch type and patch merge key used by `kubectl apply` to merge and identify unique elements in arrays.

      * `kubectl edit` and `kubectl apply` will keep the ordering of elements in merged lists ([#45980](https://github.com/kubernetes/kubernetes/pull/45980), [@mengqiy](https://github.com/mengqiy))

      * New patch directive (retainKeys) to specifying clearing fields missing from the request ([#44597](https://github.com/kubernetes/kubernetes/pull/44597), [@mengqiy](https://github.com/mengqiy))

      * Open API now includes strategic merge patch tags (previously only in go struct tags) ([#44121](https://github.com/kubernetes/kubernetes/pull/44121), [@mbohlool](https://github.com/mbohlool))

  * Plugins

      * Introduces the ability to extend kubectl by adding third-party plugins. Developer preview, please refer to the documentation for instructions about how to use it. ([#37499](https://github.com/kubernetes/kubernetes/pull/37499), [@fabianofranz](https://github.com/fabianofranz))

      * Added support for a hierarchy of kubectl plugins (a tree of plugins as children of other plugins). ([#45981](https://github.com/kubernetes/kubernetes/pull/45981), [@fabianofranz](https://github.com/fabianofranz))

      * Added exported env vars to kubectl plugins so that plugin developers have access to global flags, namespace, the plugin descriptor and the full path to the caller binary.

  * Enhancement

    * `kubectl auth can-i` now supports non-resource URLs ([#46432](https://github.com/kubernetes/kubernetes/pull/46432), [@CaoShuFeng](https://github.com/CaoShuFeng))

    * `kubectl set selector` and `kubectl set subject` no longer print "running in local/dry-run mode..." at the top.  The output can now be piped and interpretted as yaml or json ([#46507](https://github.com/kubernetes/kubernetes/pull/46507), [@bboreham](https://github.com/bboreham))

    * When using an in-cluster client with an empty configuration, the `--namespace` flag is now honored ([#46299](https://github.com/kubernetes/kubernetes/pull/46299), [@ncdc](https://github.com/ncdc))

    * The help message for missingResourceError is now generic ([#45582](https://github.com/kubernetes/kubernetes/pull/45582), [@CaoShuFeng](https://github.com/CaoShuFeng))

    * `kubectl taint node` now supports label selectors ([#44740](https://github.com/kubernetes/kubernetes/pull/44740), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))

    * `kubectl proxy --www` now logs a warning when the dir is invalid  ([#44952](https://github.com/kubernetes/kubernetes/pull/44952), [@CaoShuFeng](https://github.com/CaoShuFeng))

    * `kubectl taint` output has been enhanced with the operation ([#43171](https://github.com/kubernetes/kubernetes/pull/43171), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))

    * kubectl `--user` and `--cluster` now support completion ([#44251](https://github.com/kubernetes/kubernetes/pull/44251), [@superbrothers](https://github.com/superbrothers))

    * `kubectl config use-context` now supports completion ([#42336](https://github.com/kubernetes/kubernetes/pull/42336), [@superbrothers](https://github.com/superbrothers))

    * `kubectl version` now supports `--output` ([#39858](https://github.com/kubernetes/kubernetes/pull/39858), [@alejandroEsc](https://github.com/alejandroEsc))

    * `kubectl create configmap` has a new option `--from-env-file` that populates a configmap from file which follows a key=val format for each line. ([#38882](https://github.com/kubernetes/kubernetes/pull/38882), [@fraenkel](https://github.com/fraenkel))

    * `kubectl create secret` has a new option `--from-env-file` that populates a secret from file which follows a key=val format for each line.

  * Printing/describe

    * Print conditions of RC/RS in `kubectl describe` command. ([#44710](https://github.com/kubernetes/kubernetes/pull/44710), [@xiangpengzhao](https://github.com/xiangpengzhao))

    * Improved output on `kubectl get` and `kubectl describe` for generic objects. ([#44222](https://github.com/kubernetes/kubernetes/pull/44222), [@fabianofranz](https://github.com/fabianofranz))

    * In `kubectl describe`, find controllers with ControllerRef, instead of showing the original creator. ([#42849](https://github.com/kubernetes/kubernetes/pull/42849), [@janetkuo](https://github.com/janetkuo))

		* `kubectl version` has new flag --output (=json or yaml) allowing result of the command to be parsed in either json format or yaml. ([#39858](https://github.com/kubernetes/kubernetes/pull/39858), [@alejandroEsc](https://github.com/alejandroEsc))


  * Bug fixes

    * Fix some false negatives in detection of meaningful conflicts during strategic merge patch with maps and lists. ([#43469](https://github.com/kubernetes/kubernetes/pull/43469), [@enisoc](https://github.com/enisoc))

		* Fix false positive "meaningful conflict" detection for strategic merge patch with integer values. ([#44788](https://github.com/kubernetes/kubernetes/pull/44788), [@enisoc](https://github.com/enisoc))

		* Restored the ability of kubectl running inside a pod to consume resource files specifying a different namespace than the one the pod is running in. ([#44862](https://github.com/kubernetes/kubernetes/pull/44862), [@liggitt](https://github.com/liggitt))

    * Kubectl commands run inside a pod using a kubeconfig file now use the namespace specified in the kubeconfig file, instead of using the pod namespace. If no kubeconfig file is used, or the kubeconfig does not specify a namespace, the pod namespace is still used as a fallback. ([#44570](https://github.com/kubernetes/kubernetes/pull/44570), [@liggitt](https://github.com/liggitt))

    * Fixed `kubectl cluster-info` dump to support multi-container pod. ([#44088](https://github.com/kubernetes/kubernetes/pull/44088), [@xingzhou](https://github.com/xingzhou))

    * Kubectl will print a warning when deleting the current context ([#42538](https://github.com/kubernetes/kubernetes/pull/42538), [@adohe](https://github.com/adohe))

    * Fix VolumeClaims/capacity in `kubectl describe statefulsets` output. ([#47573](https://github.com/kubernetes/kubernetes/pull/47573), [@k82cn](https://github.com/k82cn))

		* Fixed the output of kubectl taint node command with minor improvements. ([#43171](https://github.com/kubernetes/kubernetes/pull/43171), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))


### **Networking**
#### Network Policy
* [stable] [NetworkPolicy](https://kubernetes.io/docs/concepts/services-networking/network-policies/) promoted to GA.
  * Additionally adds short name "netpol" for networkpolicies ([#42241](https://github.com/kubernetes/kubernetes/pull/42241), [@xiangpengzhao](https://github.com/xiangpengzhao))


#### Load Balancing
* [stable] Source IP Preservation - change Cloud load-balancer strategy to health-checks and respond to health check only on nodes that host pods for the service. See [Create an External Load Balancer - Preserving the client source IP](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/#preserving-the-client-source-ip).
  Two annotations have been promoted to API fields:

  * Service.Spec.ExternalTrafficPolicy was 'service.beta.kubernetes.io/external-traffic' annotation.

  * Service.Spec.HealthCheckNodePort was 'service.beta.kubernetes.io/healthcheck-nodeport' annotation.

### **Node Components**
#### Container Runtime Interface
* [alpha] CRI validation testing, which provides a test framework and a suite of tests to validate that the CRI server implementation meets all the requirements. This allows the CRI runtime developers to verify that their runtime conforms to CRI, without needing to set up Kubernetes components or run Kubernetes end-to-end tests. ([docs](https://github.com/kubernetes/community/blob/master/contributors/devel/cri-validation.md) and [release notes](https://github.com/kubernetes-incubator/cri-tools/releases/tag/v0.1)) ([kubernetes/features#292](https://github.com/kubernetes/features/issues/292))

* [alpha] Adds support of container metrics in CRI ([docs PR](https://github.com/kubernetes/community/pull/742)) ([kubernetes/features#290](https://github.com/kubernetes/features/issues/290))

* [alpha] Integration with [containerd] (https://github.com/containerd/containerd) , which supports basic pod lifecycle and image management. ([docs](https://github.com/kubernetes-incubator/cri-containerd/blob/master/README.md) and [release notes](https://github.com/kubernetes-incubator/cri-containerd/releases/tag/v0.1.0)) ([kubernetes/features#286](https://github.com/kubernetes/features/issues/286))

* [GA] The Docker-CRI implementation is GA. The legacy, non-CRI Docker integration has been completely removed.

* [beta] [CRI-O](https://github.com/kubernetes-incubator/cri-o) v1.0.0-alpha.0. It has passed all e2e tests. ([release notes](https://github.com/kubernetes-incubator/cri-o/releases/tag/v1.0.0-alpha.0))

* [beta] [Frakti](https://github.com/kubernetes/frakti) v1.0. It has passed all node conformance tests. ([release notes](https://github.com/kubernetes/frakti/releases/tag/v1.0))



### **Scheduling**
#### Scheduler Extender
* [alpha] Support for delegating pod binding to a scheduler extender ([kubernetes/features#270](https://github.com/kubernetes/features/issues/270))

### **Storage**
#### Local Storage
* [alpha] This feature adds capacity isolation support for local storage at node, container, and volume levels. See updated [Reserve Compute Resources for System Daemons](https://kubernetes.io/docs/tasks/administer-cluster/reserve-compute-resources/) documentation.

* [alpha] Make locally attached (non-network attached) storage available as a persistent volume source. For more information, see [Storage Volumes - local](https://kubernetes.io/docs/concepts/storage/volumes/#local).

#### Volume Plugins
* [stable] Volume plugin for StorageOS provides highly-available cluster-wide persistent volumes from local or attached node storage. See [Persistent Volumes - StorageOS](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#storageos) and [Storage Volumes - StorageOS](https://kubernetes.io/docs/concepts/storage/volumes/#storageos).

#### Metrics
* [stable] Add support for cloudprovider metrics for storage API calls. See [Controller manager metrics](https://kubernetes.io/docs/concepts/cluster-administration/controller-metrics/) for more information.

### **Other notable changes**

#### Admission plugin
* OwnerReferencesPermissionEnforcement admission plugin ignores pods/status. ([#45747](https://github.com/kubernetes/kubernetes/pull/45747), [@derekwaynecarr](https://github.com/derekwaynecarr))


* Ignored mirror pods in PodPreset admission plugin. ([#45958](https://github.com/kubernetes/kubernetes/pull/45958), [@k82cn](https://github.com/k82cn))

#### API Machinery
* The protobuf serialization of API objects has been updated to store maps in a predictable order to ensure that the representation of that object does not change when saved into etcd. This prevents the same object from being seen as being modified, even when no values have changed. ([#47701](https://github.com/kubernetes/kubernetes/pull/47701), [@smarterclayton](https://github.com/smarterclayton))

* API resource discovery now includes the singularName used to refer to the resource. ([#43312](https://github.com/kubernetes/kubernetes/pull/43312), [@deads2k](https://github.com/deads2k))

* Enhance the garbage collection admission plugin so that a user who doesn't have delete permission of the owning object cannot modify the blockOwnerDeletion field of existing ownerReferences, or add new ownerReferences with blockOwnerDeletion=true ([#43876](https://github.com/kubernetes/kubernetes/pull/43876), [@caesarxuchao](https://github.com/caesarxuchao))

* Exec and portforward actions over SPDY now properly handle redirects sent by the Kubelet ([#44451](https://github.com/kubernetes/kubernetes/pull/44451), [@ncdc](https://github.com/ncdc))

* The proxy subresource APIs for nodes, services, and pods now support the HTTP PATCH method. ([#44929](https://github.com/kubernetes/kubernetes/pull/44929), [@liggitt](https://github.com/liggitt))

* The Categories []string field on discovered API resources represents the list of group aliases (e.g. "all") that each resource belongs to. ([#43338](https://github.com/kubernetes/kubernetes/pull/43338), [@fabianofranz](https://github.com/fabianofranz))

* [alpha] The Kubernetes API supports retrieving tabular output for API resources via a new mime-type application/json;as=Table;v=v1alpha1;g=meta.k8s.io. The returned object (if the server supports it) will be of type meta.k8s.io/v1alpha1 with Table, and contain column and row information related to the resource. Each row will contain information about the resource - by default it will be the object metadata, but callers can add the ?includeObject=Object query parameter and receive the full object. In the future kubectl will use this to retrieve the results of `kubectl get`. ([#40848](https://github.com/kubernetes/kubernetes/pull/40848), [@smarterclayton](https://github.com/smarterclayton))

* The behavior of some watch calls to the server when filtering on fields was incorrect. If watching objects with a filter, when an update was made that no longer matched the filter a DELETE event was correctly sent. However, the object that was returned by that delete was not the (correct) version before the update, but instead, the newer version. That meant the new object was not matched by the filter. This was a regression from behavior between cached watches on the server side and uncached watches, and thus broke downstream API clients. ([#46223](https://github.com/kubernetes/kubernetes/pull/46223), [@smarterclayton](https://github.com/smarterclayton))

* OpenAPI spec is now available in protobuf binary and gzip format (with ETag support) ([#45836](https://github.com/kubernetes/kubernetes/pull/45836), [@mbohlool](https://github.com/mbohlool))

* Updating apiserver to return UID of the deleted resource. Clients can use this UID to verify that the resource was deleted or waiting for finalizers. ([#45600](https://github.com/kubernetes/kubernetes/pull/45600), [@nikhiljindal](https://github.com/nikhiljindal))

* Fix incorrect conflict errors applying strategic merge patches to resources. ([#43871](https://github.com/kubernetes/kubernetes/pull/43871), [@liggitt](https://github.com/liggitt))

* Fix init container status reporting when active deadline is exceeded. ([#46305](https://github.com/kubernetes/kubernetes/pull/46305), [@sjenning](https://github.com/sjenning))

* Moved qos to api.helpers. ([#44906](https://github.com/kubernetes/kubernetes/pull/44906), [@k82cn](https://github.com/k82cn))

* Fix issue with the resource quota controller causing add quota to be resynced at the wrong ([#45685](https://github.com/kubernetes/kubernetes/pull/45685), [@derekwaynecarr](https://github.com/derekwaynecarr))

* Added Group/Version/Kind and Action extension to OpenAPI Operations ([#44787](https://github.com/kubernetes/kubernetes/pull/44787), [@mbohlool](https://github.com/mbohlool))

* Make clear that meta.KindToResource is only a guess ([#45272](https://github.com/kubernetes/kubernetes/pull/45272), [@sttts](https://github.com/sttts))

* Add APIService conditions ([#43301](https://github.com/kubernetes/kubernetes/pull/43301), [@deads2k](https://github.com/deads2k))

* Create and push a docker image for the cloud-controller-manager ([#45154](https://github.com/kubernetes/kubernetes/pull/45154), [@luxas](https://github.com/luxas))

* Deprecated Binding objects in 1.7. ([#47041](https://github.com/kubernetes/kubernetes/pull/47041), [@k82cn](https://github.com/k82cn))

* Adds the Categories []string field to API resources, which represents the list of group aliases (e.g. "all") that every resource belongs to. ([#43338](https://github.com/kubernetes/kubernetes/pull/43338), [@fabianofranz](https://github.com/fabianofranz))

* `--service-account-lookup` now defaults to true, requiring the Secret API object containing the token to exist in order for a service account token to be valid. This enables service account tokens to be revoked by deleting the Secret object containing the token. ([#44071](https://github.com/kubernetes/kubernetes/pull/44071), [@liggitt](https://github.com/liggitt))

* API Registration is now in beta. ([#45247](https://github.com/kubernetes/kubernetes/pull/45247), [@mbohlool](https://github.com/mbohlool))

* The Kubernetes API server now exits if it encounters a networking failure (e.g. the networking interface hosting its address goes away) to allow a process manager (systemd/kubelet/etc) to react to the problem. Previously the server would log the failure and try again to bind to its configured address:port. ([#42272](https://github.com/kubernetes/kubernetes/pull/42272), [@marun](https://github.com/marun))

* The Prometheus metrics for the kube-apiserver for tracking incoming API requests and latencies now return the subresource label for correctly attributing the type of API call. ([#46354](https://github.com/kubernetes/kubernetes/pull/46354), [@smarterclayton](https://github.com/smarterclayton))

* kube-apiserver now drops unneeded path information if an older version of Windows kubectl sends it. ([#44421](https://github.com/kubernetes/kubernetes/pull/44421), [@mml](https://github.com/mml))


#### Application autoscaling
* Make "upscale forbidden window" and "downscale forbidden window"  duration configurable in arguments of kube-controller-manager. ([#42101](https://github.com/kubernetes/kubernetes/pull/42101), [@Dmitry1987](https://github.com/Dmitry1987))

#### Application Deployment
* StatefulSetStatus now tracks replicas, readyReplicas, currentReplicas, and updatedReplicas. The semantics of replicas is now consistent with DaemonSet and ReplicaSet, and readyReplicas has the semantics that replicas did prior to 1.7 ([#46669](https://github.com/kubernetes/kubernetes/pull/46669), [@kow3ns](https://github.com/kow3ns)).

* ControllerRevision type has been added for StatefulSet and DaemonSet history. Clients should not depend on the stability of this type as it may change, as necessary, in future releases to support StatefulSet and DaemonSet update and rollback. We enable this type as we do with beta features, because StatefulSet update and DaemonSet update are enabled. ([#45867](https://github.com/kubernetes/kubernetes/pull/45867), [@kow3ns](https://github.com/kow3ns))

* PodDisruptionBudget now uses ControllerRef to decide which controller owns a given Pod, so it doesn't get confused by controllers with overlapping selectors. ([#45003](https://github.com/kubernetes/kubernetes/pull/45003), [@krmayankk](https://github.com/krmayankk))

* Deployments are updated to use (1) a more stable hashing algorithm (fnv) than the previous one (adler) and (2) a hashing collision avoidance mechanism that will ensure new rollouts will not block on hashing collisions anymore. ([#44774](https://github.com/kubernetes/kubernetes/pull/44774), [@kargakis](https://github.com/kargakis))([kubernetes/features#287](https://github.com/kubernetes/features/issues/287))

* Deployments and DaemonSets rollouts are considered complete when all of the desired replicas are updated and available. This change affects `kubectl rollout status` and Deployment condition. ([#44672](https://github.com/kubernetes/kubernetes/pull/44672), [@kargakis](https://github.com/kargakis))

* Job controller now respects ControllerRef to avoid fighting over Pods. ([#42176](https://github.com/kubernetes/kubernetes/pull/42176), [@enisoc](https://github.com/enisoc))

* CronJob controller now respects ControllerRef to avoid fighting with other controllers. ([#42177](https://github.com/kubernetes/kubernetes/pull/42177), [@enisoc](https://github.com/enisoc))

#### Cluster Autoscaling
* Cluster Autoscaler 0.6. More information available [here](https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/README.md).

* cluster-autoscaler: Fix duplicate writing of logs. ([#45017](https://github.com/kubernetes/kubernetes/pull/45017), [@MaciekPytel](https://github.com/MaciekPytel))


#### Cloud Provider Enhancement

* AWS:

  * New 'service.beta.kubernetes.io/aws-load-balancer-extra-security-groups' Service annotation to specify extra Security Groups to be added to ELB created by AWS cloudprovider ([#45268](https://github.com/kubernetes/kubernetes/pull/45268), [@redbaron](https://github.com/redbaron))

  * Clean up blackhole routes when using kubenet ([#47572](https://github.com/kubernetes/kubernetes/pull/47572), [@justinsb](https://github.com/justinsb))

  * Maintain a cache of all instances, to fix problem with > 200 nodes with ELBs ([#47410](https://github.com/kubernetes/kubernetes/pull/47410), [@justinsb](https://github.com/justinsb))

  * Avoid spurious ELB listener recreation - ignore case when matching protocol ([#47391](https://github.com/kubernetes/kubernetes/pull/47391), [@justinsb](https://github.com/justinsb))

  * Allow configuration of a single security group for ELBs ([#45500](https://github.com/kubernetes/kubernetes/pull/45500), [@nbutton23](https://github.com/nbutton23))

  * Remove check that forces loadBalancerSourceRanges to be 0.0.0.0/0. ([#38636](https://github.com/kubernetes/kubernetes/pull/38636), [@dhawal55](https://github.com/dhawal55))

	* Allow setting KubernetesClusterID or KubernetesClusterTag in combination with VPC. ([#42512](https://github.com/kubernetes/kubernetes/pull/42512), [@scheeles](https://github.com/scheeles))

	* Start recording cloud provider metrics for AWS ([#43477](https://github.com/kubernetes/kubernetes/pull/43477), [@gnufied](https://github.com/gnufied))

	* AWS: Batch DescribeInstance calls with nodeNames to 150 limit, to stay within AWS filter limits. ([#47516](https://github.com/kubernetes/kubernetes/pull/47516), [@gnufied](https://github.com/gnufied))

	* AWS: Process disk attachments even with duplicate NodeNames ([#47406](https://github.com/kubernetes/kubernetes/pull/47406), [@justinsb](https://github.com/justinsb))

  * Allow configuration of a single security group for ELBs ([#45500](https://github.com/kubernetes/kubernetes/pull/45500), [@nbutton23](https://github.com/nbutton23))

  * Fix support running the master with a different AWS account or even on a different cloud provider than the nodes. ([#44235](https://github.com/kubernetes/kubernetes/pull/44235), [@mrIncompetent](https://github.com/mrIncompetent))

  * Support node port health check ([#43585](https://github.com/kubernetes/kubernetes/pull/43585), [@foolusion](https://github.com/foolusion))

  * Support for ELB tagging by users ([#45932](https://github.com/kubernetes/kubernetes/pull/45932), [@lpabon](https://github.com/lpabon))

* Azure:

  * Add support for UDP ports ([#45523](https://github.com/kubernetes/kubernetes/pull/45523), [@colemickens](https://github.com/colemickens))

  * Fix support for multiple loadBalancerSourceRanges ([#45523](https://github.com/kubernetes/kubernetes/pull/45523), [@colemickens](https://github.com/colemickens))

  * Support the Service spec's sessionAffinity ([#45523](https://github.com/kubernetes/kubernetes/pull/45523), [@colemickens](https://github.com/colemickens))

	* Added exponential backoff to Azure cloudprovider ([#46660](https://github.com/kubernetes/kubernetes/pull/46660), [@jackfrancis](https://github.com/jackfrancis))

  * Add support for bring-your-own ip address for Services on Azure ([#42034](https://github.com/kubernetes/kubernetes/pull/42034), [@brendandburns](https://github.com/brendandburns))

  * Add support for Azure internal load balancer ([#43510](https://github.com/kubernetes/kubernetes/pull/43510), [@karataliu](https://github.com/karataliu))

	* Client poll duration is now 5 seconds ([#43699](https://github.com/kubernetes/kubernetes/pull/43699), [@colemickens](https://github.com/colemickens))

	* Azure plugin for client auth ([#43987](https://github.com/kubernetes/kubernetes/pull/43987), [@cosmincojocar](https://github.com/cosmincojocar))


* GCP:

  * Bump GLBC version to 0.9.5 - fixes [loss of manually modified GCLB health check settings](https://github.com/kubernetes/kubernetes/issues/47559) upon upgrade from pre-1.6.4 to either 1.6.4 or 1.6.5. ([#47567](https://github.com/kubernetes/kubernetes/pull/47567), [@nicksardo](https://github.com/nicksardo))

  * [beta] Support creation of GCP Internal Load Balancers from Service objects ([#46663](https://github.com/kubernetes/kubernetes/pull/46663), [@nicksardo](https://github.com/nicksardo))

  * GCE installs will now avoid IP masquerade for all RFC-1918 IP blocks, rather than just 10.0.0.0/8. This means that clusters can be created in 192.168.0.0./16 and 172.16.0.0/12 while preserving the container IPs (which would be lost before). ([#46473](https://github.com/kubernetes/kubernetes/pull/46473), [@thockin](https://github.com/thockin))

  * The Calico version included in kube-up for GCE has been updated to v2.2. ([#38169](https://github.com/kubernetes/kubernetes/pull/38169), [@caseydavenport](https://github.com/caseydavenport))

	* ip-masq-agent is now on by default for GCE ([#47794](https://github.com/kubernetes/kubernetes/pull/47794), [@dnardo](https://github.com/dnardo))

  * Add ip-masq-agent addon to the addons folder which is used in GCE if `--non-masquerade-cidr` is set to 0/0 ([#46038](https://github.com/kubernetes/kubernetes/pull/46038), [@dnardo](https://github.com/dnardo))

  * Enable kubelet csr bootstrap in GCE/GKE ([#40760](https://github.com/kubernetes/kubernetes/pull/40760), [@mikedanese](https://github.com/mikedanese))

  * Adds support for allocation of pod IPs via IP aliases. ([#42147](https://github.com/kubernetes/kubernetes/pull/42147), [@bowei](https://github.com/bowei))

	* gce kube-up: The Node authorization mode and NodeRestriction admission controller are now enabled ([#46796](https://github.com/kubernetes/kubernetes/pull/46796), [@mikedanese](https://github.com/mikedanese))

	* Tokens retrieved from Google Cloud with application default credentials will not be cached if the client fails authorization ([#46694](https://github.com/kubernetes/kubernetes/pull/46694), [@matt-tyler](https://github.com/matt-tyler))

	* Add metrics to all major gce operations {latency, errors} ([#44510](https://github.com/kubernetes/kubernetes/pull/44510), [@bowei](https://github.com/bowei))

	    * The new metrics are:

	    * cloudprovider_gce_api_request_duration_seconds{request, region, zone}

	    * cloudprovider_gce_api_request_errors{request, region, zone}

	    * request is the specific function that is used.

	    * region is the target region (Will be "<n/a>" if not applicable)

	    * zone is the target zone (Will be "<n/a>" if not applicable)

	    * Note: this fixes some issues with the previous implementation of metrics for disks:

	      * Time duration tracked was of the initial API call, not the entire operation.

	      * Metrics label tuple would have resulted in many independent histograms stored, one for each disk. (Did not aggregate well).

  * Fluentd now tolerates all NoExecute Taints when run in gcp configuration. ([#45715](https://github.com/kubernetes/kubernetes/pull/45715), [@gmarek](https://github.com/gmarek))

	* Taints support in gce/salt startup scripts. ([#47632](https://github.com/kubernetes/kubernetes/pull/47632), [@mwielgus](https://github.com/mwielgus))

	* GCE installs will now avoid IP masquerade for all RFC-1918 IP blocks, rather than just 10.0.0.0/8. This means that clusters can ([#46473](https://github.com/kubernetes/kubernetes/pull/46473), [@thockin](https://github.com/thockin)) be created in 192.168.0.0./16 and 172.16.0.0/12 while preserving the container IPs (which would be lost before).

	* Support running Ubuntu image on GCE node ([#44744](https://github.com/kubernetes/kubernetes/pull/44744), [@yguo0905](https://github.com/yguo0905))

  * The gce metadata server can now be hidden behind a proxy, hiding the kubelet's token. ([#45565](https://github.com/kubernetes/kubernetes/pull/45565), [@Q-Lee](https://github.com/Q-Lee))

* OpenStack:

    * Fix issue during LB creation where ports were incorrectly assigned to a floating IP ([#44387](https://github.com/kubernetes/kubernetes/pull/44387), [@jamiehannaford](https://github.com/jamiehannaford))

    * Openstack cinder v1/v2/auto API support ([#40423](https://github.com/kubernetes/kubernetes/pull/40423), [@mkutsevol](https://github.com/mkutsevol))

    * OpenStack clusters can now specify whether worker nodes are assigned a floating IP ([#42638](https://github.com/kubernetes/kubernetes/pull/42638), [@jamiehannaford](https://github.com/jamiehannaford))


* vSphere:

  * Fix volume detach on node failure. ([#45569](https://github.com/kubernetes/kubernetes/pull/45569), [@divyenpatel](https://github.com/divyenpatel))

  * Report same Node IP as both internal and external. ([#45201](https://github.com/kubernetes/kubernetes/pull/45201), [@abrarshivani](https://github.com/abrarshivani))

  * Filter out IPV6 node addresses. ([#45181](https://github.com/kubernetes/kubernetes/pull/45181), [@BaluDontu](https://github.com/BaluDontu))

  * Fix fetching of VM UUID on Ubuntu 16.04 and Fedora. ([#45311](https://github.com/kubernetes/kubernetes/pull/45311), [@divyenpatel](https://github.com/divyenpatel))


#### Cluster Provisioning
* Juju:

  * Add Kubernetes 1.6 support to Juju charms ([#44500](https://github.com/kubernetes/kubernetes/pull/44500), [@Cynerva](https://github.com/Cynerva))

    * Add metric collection to charms for autoscaling

    * Update kubernetes-e2e charm to fail when test suite fails

    * Update Juju charms to use snaps

    * Add registry action to the kubernetes-worker charm

    * Add support for kube-proxy cluster-cidr option to kubernetes-worker charm

    * Fix kubernetes-master charm starting services before TLS certs are saved

    * Fix kubernetes-worker charm failures in LXD

    * Fix stop hook failure on kubernetes-worker charm

    * Fix handling of juju kubernetes-worker.restart-needed state

    * Fix nagios checks in charms

  * Enable GPU mode if GPU hardware detected ([#43467](https://github.com/kubernetes/kubernetes/pull/43467), [@tvansteenburgh](https://github.com/tvansteenburgh))

  * Fix ceph-secret type to kubernetes.io/rbd in kubernetes-master charm ([#44635](https://github.com/kubernetes/kubernetes/pull/44635), [@Cynerva](https://github.com/Cynerva))

  * Disallows installation of upstream docker from PPA in the Juju kubernetes-worker charm. ([#44681](https://github.com/kubernetes/kubernetes/pull/44681), [@wwwtyro](https://github.com/wwwtyro))

  * Resolves juju vsphere hostname bug showing only a single node in a scaled node-pool. ([#44780](https://github.com/kubernetes/kubernetes/pull/44780), [@chuckbutler](https://github.com/chuckbutler))

  * Fixes a bug in the kubernetes-worker Juju charm code that attempted to give kube-proxy more than one api endpoint. ([#44677](https://github.com/kubernetes/kubernetes/pull/44677), [@wwwtyro](https://github.com/wwwtyro))

  * Added CIFS PV support for Juju Charms ([#45117](https://github.com/kubernetes/kubernetes/pull/45117), [@chuckbutler](https://github.com/chuckbutler))

  * Fixes juju kubernetes master: 1. Get certs from a dead leader. 2. Append tokens. ([#43620](https://github.com/kubernetes/kubernetes/pull/43620), [@ktsakalozos](https://github.com/ktsakalozos))

  * kubernetes-master juju charm properly detects etcd-scale events and reconfigures appropriately. ([#44967](https://github.com/kubernetes/kubernetes/pull/44967), [@chuckbutler](https://github.com/chuckbutler))

 	* Use correct option name in the kubernetes-worker layer registry action ([#44921](https://github.com/kubernetes/kubernetes/pull/44921), [@jacekn](https://github.com/jacekn))

	* Send dns details only after cdk-addons are configured ([#44945](https://github.com/kubernetes/kubernetes/pull/44945), [@ktsakalozos](https://github.com/ktsakalozos))

	* Added support to the pause action in the kubernetes-worker charm for new flag `--delete-local-data` ([#44931](https://github.com/kubernetes/kubernetes/pull/44931), [@chuckbutler](https://github.com/chuckbutler))

	* Add namespace-{list, create, delete} actions to the kubernetes-master layer ([#44277](https://github.com/kubernetes/kubernetes/pull/44277), [@jacekn](https://github.com/jacekn))

	* Using http2 in kubeapi-load-balancer to fix `kubectl exec` uses ([#43625](https://github.com/kubernetes/kubernetes/pull/43625), [@mbruzek](https://github.com/mbruzek))


  * Don't append :443 to registry domain in the kubernetes-worker layer registry action ([#45550](https://github.com/kubernetes/kubernetes/pull/45550), [@jacekn](https://github.com/jacekn))

* kubeadm

  * Enable the Node Authorizer/Admission plugin in v1.7 ([#46879](https://github.com/kubernetes/kubernetes/pull/46879), [@luxas](https://github.com/luxas))

  * Users can now pass extra parameters to etcd in a kubeadm cluster ([#42246](https://github.com/kubernetes/kubernetes/pull/42246), [@jamiehannaford](https://github.com/jamiehannaford))

  * Make kubeadm use the new CSR approver in v1.7 ([#46864](https://github.com/kubernetes/kubernetes/pull/46864), [@luxas](https://github.com/luxas))

  * Allow enabling multiple authorization modes at the same time ([#42557](https://github.com/kubernetes/kubernetes/pull/42557), [@xilabao](https://github.com/xilabao))

  * add proxy client-certs to kube-apiserver to allow it to proxy aggregated api servers ([#43715](https://github.com/kubernetes/kubernetes/pull/43715), [@deads2k](https://github.com/deads2k))* CentOS provider

* hyperkube

  * The hyperkube image has been slimmed down and no longer includes addon manifests and other various scripts. These were introduced for the now removed docker-multinode setup system. ([#44555](https://github.com/kubernetes/kubernetes/pull/44555), [@luxas](https://github.com/luxas))

* Support secure etcd cluster for centos provider. ([#42994](https://github.com/kubernetes/kubernetes/pull/42994), [@Shawyeok](https://github.com/Shawyeok))

* Update to kube-addon-manager:v6.4-beta.2: kubectl v1.6.4 and refreshed base images ([#47389](https://github.com/kubernetes/kubernetes/pull/47389), [@ixdy](https://github.com/ixdy))

* Remove Initializers from admission-control in kubernetes-master charm for pre-1.7 ([#46987](https://github.com/kubernetes/kubernetes/pull/46987), [@Cynerva](https://github.com/Cynerva))

* Added state guards to the idle_status messaging in the kubernetes-master charm to make deployment faster on initial deployment. ([#47183](https://github.com/kubernetes/kubernetes/pull/47183), [@chuckbutler](https://github.com/chuckbutler))

#### Cluster federation
* Features:

  * Adds annotations to all Federation objects created by kubefed. ([#42683](https://github.com/kubernetes/kubernetes/pull/42683), [@perotinus](https://github.com/perotinus))

	* Mechanism of adding `federation domain maps` to kube-dns deployment via `--federations` flag is superseded by adding/updating `federations` key in `kube-system/kube-dns` configmap. If user is using kubefed tool to join cluster federation, adding federation domain maps to kube-dns is already taken care by `kubefed join` and does not need further action.

	* Prints out status updates when running `kubefed init` ([#41849](https://github.com/kubernetes/kubernetes/pull/41849), [@perotinus](https://github.com/perotinus))

	* `kubefed init` now supports overriding the default etcd image name with the `--etcd-image` parameter. ([#46247](https://github.com/kubernetes/kubernetes/pull/46247), [@marun](https://github.com/marun))

	* kubefed will now configure NodeInternalIP as the federation API server endpoint when NodeExternalIP is unavailable for federation API servers exposed as NodePort services ([#46960](https://github.com/kubernetes/kubernetes/pull/46960), [@lukaszo](https://github.com/lukaszo))

	* Automate configuring nameserver in cluster-dns for CoreDNS provider ([#42895](https://github.com/kubernetes/kubernetes/pull/42895), [@shashidharatd](https://github.com/shashidharatd))

	* A new controller for managing DNS records is introduced which can be optionally disabled to enable third party components to manage DNS records for federated services. ([#45034](https://github.com/kubernetes/kubernetes/pull/45034), [@shashidharatd](https://github.com/shashidharatd))

  * Remove the `--secret-name` flag from `kubefed join`, instead generating the secret name arbitrarily. ([#42513](https://github.com/kubernetes/kubernetes/pull/42513), [@perotinus](https://github.com/perotinus))

  *  Use StorageClassName for etcd pvc ([#46323](https://github.com/kubernetes/kubernetes/pull/46323), [@marun](https://github.com/marun))

* Bug fixes:

	* Allow disabling federation controllers through override args ([#44209](https://github.com/kubernetes/kubernetes/pull/44209), [@irfanurrehman](https://github.com/irfanurrehman))

	* Kubefed: Use service accounts instead of the user's credentials when accessing joined clusters' API servers. ([#42042](https://github.com/kubernetes/kubernetes/pull/42042), [@perotinus](https://github.com/perotinus))

	* Avoid panic if route53 fields are nil ([#44380](https://github.com/kubernetes/kubernetes/pull/44380), [@justinsb](https://github.com/justinsb))


#### Credential provider
* add rancher credential provider ([#40160](https://github.com/kubernetes/kubernetes/pull/40160), [@wlan0](https://github.com/wlan0))

#### Information for Kubernetes clients (openapi, swagger, client-go)
* Features:

  * Add Host field to TCPSocketAction ([#42902](https://github.com/kubernetes/kubernetes/pull/42902), [@louyihua](https://github.com/louyihua))

	* Add the ability to lock on ConfigMaps to support HA for self hosted components ([#42666](https://github.com/kubernetes/kubernetes/pull/42666), [@timothysc](https://github.com/timothysc))

	* validateClusterInfo: use clientcmdapi.NewCluster() ([#44221](https://github.com/kubernetes/kubernetes/pull/44221), [@ncdc](https://github.com/ncdc))

	* OpenAPI spec is now available in protobuf binary and gzip format (with ETag support) ([#45836](https://github.com/kubernetes/kubernetes/pull/45836), [@mbohlool](https://github.com/mbohlool))

	* HostAliases is now parsed with hostAliases json keys to be in line with the feature's name. ([#47512](https://github.com/kubernetes/kubernetes/pull/47512), [@rickypai](https://github.com/rickypai))

	* Add redirect support to SpdyRoundTripper ([#44451](https://github.com/kubernetes/kubernetes/pull/44451), [@ncdc](https://github.com/ncdc))

	* Duplicate recurring Events now include the latest event's Message string ([#46034](https://github.com/kubernetes/kubernetes/pull/46034), [@kensimon](https://github.com/kensimon))

* Bug fixes:

  * Fix serialization of EnforceNodeAllocatable ([#44606](https://github.com/kubernetes/kubernetes/pull/44606), [@ivan4th](https://github.com/ivan4th))

	* Use OS-specific libs when computing client User-Agent in kubectl, etc. ([#44423](https://github.com/kubernetes/kubernetes/pull/44423), [@monopole](https://github.com/monopole))


#### Instrumentation
* Bumped Heapster to v1.4.0. More details about the release https://github.com/kubernetes/heapster/releases/tag/v1.4.0

* Fluentd manifest pod is no longer created on non-registered master when creating clusters using kube-up.sh. ([#44721](https://github.com/kubernetes/kubernetes/pull/44721), [@piosz](https://github.com/piosz))

* Stackdriver cluster logging now deploys a new component to export Kubernetes events. ([#46700](https://github.com/kubernetes/kubernetes/pull/46700), [@crassirostris](https://github.com/crassirostris))

* Stackdriver Logging deployment exposes metrics on node port 31337 when enabled. ([#47402](https://github.com/kubernetes/kubernetes/pull/47402), [@crassirostris](https://github.com/crassirostris))

* Upgrade Elasticsearch Addon to v5.4.0 ([#45589](https://github.com/kubernetes/kubernetes/pull/45589), [@it-svit](https://github.com/it-svit))

#### Internal storage layer
* prevent pods/status from touching ownerreferences ([#45826](https://github.com/kubernetes/kubernetes/pull/45826), [@deads2k](https://github.com/deads2k))

* Ensure that autoscaling/v1 is the preferred version for API discovery when autoscaling/v2alpha1 is enabled. ([#45741](https://github.com/kubernetes/kubernetes/pull/45741), [@DirectXMan12](https://github.com/DirectXMan12))

* The proxy subresource APIs for nodes, services, and pods now support the HTTP PATCH method. ([#44929](https://github.com/kubernetes/kubernetes/pull/44929), [@liggitt](https://github.com/liggitt))

* Fluentd now tolerates all NoExecute Taints when run in gcp configuration. ([#45715](https://github.com/kubernetes/kubernetes/pull/45715), [@gmarek](https://github.com/gmarek))


#### Kubernetes Dashboard

* Increase Dashboard's memory requests and limits ([#44712](https://github.com/kubernetes/kubernetes/pull/44712), [@maciaszczykm](https://github.com/maciaszczykm))

* Update Dashboard version to 1.6.1 ([#45953](https://github.com/kubernetes/kubernetes/pull/45953), [@maciaszczykm](https://github.com/maciaszczykm))


#### kube-dns
* Updates kube-dns to 1.14.2 ([#45684](https://github.com/kubernetes/kubernetes/pull/45684), [@bowei](https://github.com/bowei))

   * Support kube-master-url flag without kubeconfig

   * Fix concurrent R/Ws in dns.go

   * Fix confusing logging when initialize server

   * Fix printf in cmd/kube-dns/app/server.go

   * Fix version on startup and `--version` flag

   * Support specifying port number for nameserver in stubDomains

#### kube-proxy
* Features:

  * ratelimit runs of iptables by sync-period flags ([#46266](https://github.com/kubernetes/kubernetes/pull/46266), [@thockin](https://github.com/thockin))

  * Log warning when invalid dir passed to `kubectl proxy --www` ([#44952](https://github.com/kubernetes/kubernetes/pull/44952), [@CaoShuFeng](https://github.com/CaoShuFeng))

  * Add `--write-config-to` flag to kube-proxy to allow users to write the default configuration settings to a file. ([#45908](https://github.com/kubernetes/kubernetes/pull/45908), [@ncdc](https://github.com/ncdc))

	* When switching from the service.beta.kubernetes.io/external-traffic annotation to the new ([#46716](https://github.com/kubernetes/kubernetes/pull/46716), [@thockin](https://github.com/thockin)) externalTrafficPolicy field, the values chnag as follows: * "OnlyLocal" becomes "Local" * "Global" becomes "Cluster".


* Bug fixes:

  * Fix corner-case with OnlyLocal Service healthchecks. ([#44313](https://github.com/kubernetes/kubernetes/pull/44313), [@thockin](https://github.com/thockin))

	* Fix DNS suffix search list support in Windows kube-proxy. ([#45642](https://github.com/kubernetes/kubernetes/pull/45642), [@JiangtianLi](https://github.com/JiangtianLi))

#### kube-scheduler
* Scheduler can receive its policy configuration from a ConfigMap ([#43892](https://github.com/kubernetes/kubernetes/pull/43892), [@bsalamat](https://github.com/bsalamat))

* Aggregated used ports at the NodeInfo level for PodFitsHostPorts predicate. ([#42524](https://github.com/kubernetes/kubernetes/pull/42524), [@k82cn](https://github.com/k82cn))

* leader election lock based on scheduler name ([#42961](https://github.com/kubernetes/kubernetes/pull/42961), [@wanghaoran1988](https://github.com/wanghaoran1988))


#### Storage

* Features

  * The options passed to a Flexvolume plugin's mount command now contains the pod name (kubernetes.io/pod.name), namespace (kubernetes.io/pod.namespace), uid (kubernetes.io/pod.uid), and service account name (kubernetes.io/serviceAccount.name). ([#39488](https://github.com/kubernetes/kubernetes/pull/39488), [@liggitt](https://github.com/liggitt))

  * GCE and AWS dynamic provisioners extension: admins can configure zone(s) in which a persistent volume shall be created. ([#38505](https://github.com/kubernetes/kubernetes/pull/38505), [@pospispa](https://github.com/pospispa))

  * Implement API usage metrics for GCE storage. ([#40338](https://github.com/kubernetes/kubernetes/pull/40338), [@gnufied](https://github.com/gnufied))

  * Add support for emitting metrics from openstack cloudprovider about storage operations. ([#46008](https://github.com/kubernetes/kubernetes/pull/46008), [@NickrenREN](https://github.com/NickrenREN))

  * vSphere cloud provider: vSphere storage policy support for dynamic volume provisioning. ([#46176](https://github.com/kubernetes/kubernetes/pull/46176), [@BaluDontu](https://github.com/BaluDontu))

  * Support StorageClass in Azure file volume ([#42170](https://github.com/kubernetes/kubernetes/pull/42170), [@rootfs](https://github.com/rootfs))

  * Start recording cloud provider metrics for AWS ([#43477](https://github.com/kubernetes/kubernetes/pull/43477), [@gnufied](https://github.com/gnufied))

  * Support iSCSI CHAP authentication ([#43396](https://github.com/kubernetes/kubernetes/pull/43396), [@rootfs](https://github.com/rootfs))

  * Openstack cinder v1/v2/auto API support ([#40423](https://github.com/kubernetes/kubernetes/pull/40423), [@mkutsevol](https://github.com/mkutsevol))

  * Alpha feature: allows users to set storage limit to isolate EmptyDir volumes. It enforces the limit by evicting pods that exceed their storage limits ([#45686](https://github.com/kubernetes/kubernetes/pull/45686), [@jingxu97](https://github.com/jingxu97))

* Bug fixes

  * Fixes issue with Flexvolume, introduced in 1.6.0, where drivers without an attacher would fail (node indefinitely waiting for attach). A driver API addition is introduced: drivers that don't implement attach should return attach: false on init. ([#47503](https://github.com/kubernetes/kubernetes/pull/47503), [@chakri-nelluri](https://github.com/chakri-nelluri))

  * Fix dynamic provisioning of PVs with inaccurate AccessModes by refusing to provision when PVCs ask for AccessModes that can't be satisfied by the PVs' underlying volume plugin. ([#47274](https://github.com/kubernetes/kubernetes/pull/47274), [@wongma7](https://github.com/wongma7))

  * Fix pods failing to start if they specify a file as a volume subPath to mount. ([#45623](https://github.com/kubernetes/kubernetes/pull/45623), [@wongma7](https://github.com/wongma7))

  * Fix erroneous FailedSync and FailedMount events being periodically and indefinitely posted on Pods after kubelet is restarted. ([#44781](https://github.com/kubernetes/kubernetes/pull/44781), [@wongma7](https://github.com/wongma7))

  * Fix AWS EBS volumes not getting detached from node if routine to verify volumes are attached runs while the node is down ([#46463](https://github.com/kubernetes/kubernetes/pull/46463), [@wongma7](https://github.com/wongma7))

  * Improves performance of Cinder volume attach/detach operations. ([#41785](https://github.com/kubernetes/kubernetes/pull/41785), [@jamiehannaford](https://github.com/jamiehannaford))

  * Fix iSCSI iSER mounting. ([#47281](https://github.com/kubernetes/kubernetes/pull/47281), [@mtanino](https://github.com/mtanino))

  * iscsi storage plugin: Fix dangling session when using multiple target portal addresses. ([#46239](https://github.com/kubernetes/kubernetes/pull/46239), [@mtanino](https://github.com/mtanino))


  * Fix log spam due to unnecessary status update when node is deleted. ([#45923](https://github.com/kubernetes/kubernetes/pull/45923), [@verult](https://github.com/verult))

  * Don't try to attach volume to new node if it is already attached to another node and the volume does not support multi-attach. ([#45346](https://github.com/kubernetes/kubernetes/pull/45346), [@codablock](https://github.com/codablock))

  * detach the volume when pod is terminated ([#45286](https://github.com/kubernetes/kubernetes/pull/45286), [@gnufied](https://github.com/gnufied))

  * Roll up volume error messages in the kubelet sync loop. ([#44938](https://github.com/kubernetes/kubernetes/pull/44938), [@jayunit100](https://github.com/jayunit100))

  * Catch error when failed to make directory in NFS volume plugin ([#38801](https://github.com/kubernetes/kubernetes/pull/38801), [@nak3](https://github.com/nak3))



#### Networking

* DNS and name resolution

  * Updates kube-dns to 1.14.2 ([#45684](https://github.com/kubernetes/kubernetes/pull/45684), [@bowei](https://github.com/bowei))

    * Support kube-master-url flag without kubeconfig

    * Fix concurrent R/Ws in dns.go

    * Fix confusing logging when initializing server

    * Support specifying port number for nameserver in stubDomains

  * A new field hostAliases has been added to pod.spec to support adding entries to a Pod's /etc/hosts file. ([#44641](https://github.com/kubernetes/kubernetes/pull/44641), [@rickypai](https://github.com/rickypai))

  * Fix DNS suffix search list support in Windows kube-proxy. ([#45642](https://github.com/kubernetes/kubernetes/pull/45642), [@JiangtianLi](https://github.com/JiangtianLi))

* Kube-proxy

  * ratelimit runs of iptables by sync-period flags ([#46266](https://github.com/kubernetes/kubernetes/pull/46266), [@thockin](https://github.com/thockin))

  * Fix corner-case with OnlyLocal Service healthchecks. ([#44313](https://github.com/kubernetes/kubernetes/pull/44313), [@thockin](https://github.com/thockin))

* Exclude nodes labeled as master from LoadBalancer / NodePort; restores documented behaviour. ([#44745](https://github.com/kubernetes/kubernetes/pull/44745), [@justinsb](https://github.com/justinsb))

* Adds support for CNI ConfigLists, which permit plugin chaining. ([#42202](https://github.com/kubernetes/kubernetes/pull/42202), [@squeed](https://github.com/squeed))

* Fix node selection logic on initial LB creation ([#45773](https://github.com/kubernetes/kubernetes/pull/45773), [@justinsb](https://github.com/justinsb))

* When switching from the service.beta.kubernetes.io/external-traffic annotation to the new externalTrafficPolicy field, the values change as follows: * "OnlyLocal" becomes "Local" * "Global" becomes "Cluster". ([#46716](https://github.com/kubernetes/kubernetes/pull/46716), [@thockin](https://github.com/thockin))

* servicecontroller: Fix node selection logic on initial LB creation ([#45773](https://github.com/kubernetes/kubernetes/pull/45773), [@justinsb](https://github.com/justinsb))

* fixed HostAlias in PodSpec to allow foo.bar hostnames instead of just foo DNS labels. ([#46809](https://github.com/kubernetes/kubernetes/pull/46809), [@rickypai](https://github.com/rickypai))


#### Node controller
* Bug fixes:

  * Fix [transition between NotReady and Unreachable taints](https://github.com/kubernetes/kubernetes/issues/43444). ([#44042](https://github.com/kubernetes/kubernetes/pull/44042), [@gmarek](https://github.com/gmarek))


#### Node Components

* Features

  * Removes the deprecated kubelet flag `--babysit-daemons` ([#44230](https://github.com/kubernetes/kubernetes/pull/44230), [@mtaufen](https://github.com/mtaufen))

  * make dockershim.sock configurable ([#43914](https://github.com/kubernetes/kubernetes/pull/43914), [@ncdc](https://github.com/ncdc))

  * Support running Ubuntu image on GCE node ([#44744](https://github.com/kubernetes/kubernetes/pull/44744), [@yguo0905](https://github.com/yguo0905))

  * Kubernetes now shares a single PID namespace among all containers in a pod when running with docker >= 1.13.1. This means processes can now signal processes in other containers in a pod, but it also means that the `kubectl exec {pod} kill 1` pattern will cause the Pod to be restarted rather than a single container. ([#45236](https://github.com/kubernetes/kubernetes/pull/45236), [@verb](https://github.com/verb))

  * A new field hostAliases has been added to the pod spec to support [adding entries to a Pod's /etc/hosts file](https://kubernetes.io/docs/concepts/services-networking/add-entries-to-pod-etc-hosts-with-host-aliases/). ([#44641](https://github.com/kubernetes/kubernetes/pull/44641), [@rickypai](https://github.com/rickypai))

  * With `--feature-gates=RotateKubeletClientCertificate=true` set, the Kubelet will ([#41912](https://github.com/kubernetes/kubernetes/pull/41912), [@jcbsmpsn](https://github.com/jcbsmpsn))

    * request a client certificate from the API server during the boot cycle and pause

    * waiting for the request to be satisfied. It will continually refresh the certificate

  * Create clusters with GPUs in GCE by specifying `type=<gpu-type>,count=<gpu-count>` to NODE_ACCELERATORS environment variable. ([#45130](https://github.com/kubernetes/kubernetes/pull/45130), [@vishh](https://github.com/vishh))

    * List of available GPUs - [https://cloud.google.com/compute/docs/gpus/#introduction](https://cloud.google.com/compute/docs/gpus/#introduction)

  * Disk Pressure triggers the deletion of terminated containers on the node. ([#45896](https://github.com/kubernetes/kubernetes/pull/45896), [@dashpole](https://github.com/dashpole))

  * Support status.hostIP in downward API ([#42717](https://github.com/kubernetes/kubernetes/pull/42717), [@andrewsykim](https://github.com/andrewsykim))

  * Upgrade Node Problem Detector to v0.4.1. New features added:

    * Add /dev/kmsg support for kernel log parsing. ([#112](https://github.com/kubernetes/node-problem-detector/pull/112), [@euank](https://github.com/euank))

    * Add ABRT support. ([#105](https://github.com/kubernetes/node-problem-detector/pull/105), [@juliusmilan](https://github.com/juliusmilan))

    * Add a docker image corruption problem detection in the default docker monitor config. ([#117](https://github.com/kubernetes/node-problem-detector/pull/117), [@ajitak](https://github.com/ajitak))
    
  * Upgrade CAdvisor to v0.26.1. New features added:

    * Add Docker overlay2 storage driver support.

    * Add ZFS support.

    * Add UDP metrics (collection disabled by default).

  * Roll up volume error messages in the kubelet sync loop. ([#44938](https://github.com/kubernetes/kubernetes/pull/44938), [@jayunit100](https://github.com/jayunit100))
  
  * Allow pods to opt out of PodPreset mutation via an annotation on the pod. ([#44965](https://github.com/kubernetes/kubernetes/pull/44965), [@jpeeler](https://github.com/jpeeler))

  * Add generic Toleration for NoExecute Taints to NodeProblemDetector, so that NPD can be scheduled to nodes with NoExecute taints by default. ([#45883](https://github.com/kubernetes/kubernetes/pull/45883), [@gmarek](https://github.com/gmarek))

  * Prevent kubelet from setting allocatable < 0 for a resource upon initial creation. ([#46516](https://github.com/kubernetes/kubernetes/pull/46516), [@derekwaynecarr](https://github.com/derekwaynecarr))

* Bug fixes

  * Changed Kubelet default image-gc-high-threshold to 85% to resolve a conflict with default settings in docker that prevented image garbage collection from resolving low disk space situations when using devicemapper storage. ([#40432](https://github.com/kubernetes/kubernetes/pull/40432), [@sjenning](https://github.com/sjenning))

  * Mark all static pods on the Master node as critical to prevent preemption ([#47356](https://github.com/kubernetes/kubernetes/pull/47356), [@dashpole](https://github.com/dashpole))

  * Restrict active deadline seconds max allowed value to be maximum uint32 to avoid overflow ([#46640](https://github.com/kubernetes/kubernetes/pull/46640), [@derekwaynecarr](https://github.com/derekwaynecarr))

  * Fix a bug with cAdvisorPort in the KubeletConfiguration that prevented setting it to 0, which is in fact a valid option, as noted in issue [#11710](https://github.com/kubernetes/kubernetes/pull/11710). ([#46876](https://github.com/kubernetes/kubernetes/pull/46876), [@mtaufen](https://github.com/mtaufen))

  * Fix a bug where container cannot run as root when SecurityContext.RunAsNonRoot is false. ([#47009](https://github.com/kubernetes/kubernetes/pull/47009), [@yujuhong](https://github.com/yujuhong))

  * Fix the Kubelet PLEG update timestamp to better reflect the health of the component when the container runtime request hangs. ([#45496](https://github.com/kubernetes/kubernetes/pull/45496), [@andyxning](https://github.com/andyxning))

  * Avoid failing sync loop health check on container runtime errors ([#47124](https://github.com/kubernetes/kubernetes/pull/47124), [@andyxning](https://github.com/andyxning))

  * Fix a bug where Kubelet does not ignore pod manifest files starting with dots ([#45111](https://github.com/kubernetes/kubernetes/pull/45111), [@dwradcliffe](https://github.com/dwradcliffe))

  * Fix kubelet reset liveness probe failure count across pod restart boundaries ([#46371](https://github.com/kubernetes/kubernetes/pull/46371), [@sjenning](https://github.com/sjenning))

  * Fix log spam due to unnecessary status update when node is deleted. ([#45923](https://github.com/kubernetes/kubernetes/pull/45923), [@verult](https://github.com/verult))

  * Fix kubelet event recording for selected events. ([#46246](https://github.com/kubernetes/kubernetes/pull/46246), [@derekwaynecarr](https://github.com/derekwaynecarr))

  * Fix image garbage collector attempting to remove in-use images. ([#46121](https://github.com/kubernetes/kubernetes/pull/46121), [@Random-Liu](https://github.com/Random-Liu))

  * Detach the volume when pod is terminated ([#45286](https://github.com/kubernetes/kubernetes/pull/45286), [@gnufied](https://github.com/gnufied))

  * CRI: Fix StopContainer timeout ([#44970](https://github.com/kubernetes/kubernetes/pull/44970), [@Random-Liu](https://github.com/Random-Liu))

  * CRI: Fix kubelet failing to start when using rkt. ([#44569](https://github.com/kubernetes/kubernetes/pull/44569), [@yujuhong](https://github.com/yujuhong))

  * CRI: `kubectl logs -f` now stops following when container stops, as it did pre-CRI. ([#44406](https://github.com/kubernetes/kubernetes/pull/44406), [@Random-Liu](https://github.com/Random-Liu))

  * Fixes a bug where pods were evicted even after images are successfully deleted. ([#44986](https://github.com/kubernetes/kubernetes/pull/44986), [@dashpole](https://github.com/dashpole))

  * When creating a container using envFrom. ([#42083](https://github.com/kubernetes/kubernetes/pull/42083), [@fraenkel](https://github.com/fraenkel))
    * validate the name of the ConfigMap in a ConfigMapRef
    * validate the name of the Secret in a SecretRef

  * Fix the bug where StartedAt time is not reported for exited containers. ([#45977](https://github.com/kubernetes/kubernetes/pull/45977), [@yujuhong](https://github.com/yujuhong))

* Changes/deprecations

  * Marks the Kubelet's `--master-service-namespace` flag deprecated ([#44250](https://github.com/kubernetes/kubernetes/pull/44250), [@mtaufen](https://github.com/mtaufen))

  * Remove PodSandboxStatus.Linux.Namespaces.Network from CRI since it is not used/needed. ([#45166](https://github.com/kubernetes/kubernetes/pull/45166), [@feiskyer](https://github.com/feiskyer))

  * Remove the `--enable-cri` flag. CRI is now the default, and the only way to integrate with Kubelet for the container runtimes.([#45194](https://github.com/kubernetes/kubernetes/pull/45194), [@yujuhong](https://github.com/yujuhong))

  * CRI has been moved to package pkg/kubelet/apis/cri/v1alpha1/runtime as part of Kubelet API path cleanup. ([#47113](https://github.com/kubernetes/kubernetes/pull/47113), [@feiskyer](https://github.com/feiskyer))


#### Scheduling

* The fix makes scheduling go routine waiting for cache (e.g. Pod) to be synced. ([#45453](https://github.com/kubernetes/kubernetes/pull/45453), [@k82cn](https://github.com/k82cn))

* Move hardPodAffinitySymmetricWeight to scheduler policy config ([#44159](https://github.com/kubernetes/kubernetes/pull/44159), [@wanghaoran1988](https://github.com/wanghaoran1988))

* Align Extender's validation with prioritizers. ([#45091](https://github.com/kubernetes/kubernetes/pull/45091), [@k82cn](https://github.com/k82cn))

* Removed old scheduler constructor. ([#45472](https://github.com/kubernetes/kubernetes/pull/45472), [@k82cn](https://github.com/k82cn))

* Fixes the overflow for priorityconfig- valid range {1, 9223372036854775806}. ([#45122](https://github.com/kubernetes/kubernetes/pull/45122), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))


#### Security
* Features:

  * Permission to use a PodSecurityPolicy can now be granted within a single namespace by allowing the use verb on the podsecuritypolicies resource within the namespace. ([#42360](https://github.com/kubernetes/kubernetes/pull/42360), [@liggitt](https://github.com/liggitt))

  * Break the 'certificatesigningrequests' controller into a 'csrapprover' controller and 'csrsigner' controller. ([#45514](https://github.com/kubernetes/kubernetes/pull/45514), [@mikedanese](https://github.com/mikedanese))

  * `kubectl auth can-i` now supports non-resource URLs ([#46432](https://github.com/kubernetes/kubernetes/pull/46432), [@CaoShuFeng](https://github.com/CaoShuFeng))

  * Promote kubelet tls bootstrap to beta. Add a non-experimental flag to use it and deprecate the old flag. ([#46799](https://github.com/kubernetes/kubernetes/pull/46799), [@mikedanese](https://github.com/mikedanese))

  * Add the alpha.image-policy.k8s.io/failed-open=true annotation when the image policy webhook encounters an error and fails open. ([#46264](https://github.com/kubernetes/kubernetes/pull/46264), [@Q-Lee](https://github.com/Q-Lee))

  * Add an AEAD encrypting transformer for storing secrets encrypted at rest ([#41939](https://github.com/kubernetes/kubernetes/pull/41939), [@smarterclayton](https://github.com/smarterclayton))

  * Add secretbox and AES-CBC encryption modes to at rest encryption. AES-CBC is considered superior to AES-GCM because it is resistant to nonce-reuse attacks, and secretbox uses Poly1305 and XSalsa20. ([#46916](https://github.com/kubernetes/kubernetes/pull/46916), [@smarterclayton](https://github.com/smarterclayton))

* Bug fixes:

  * Make gcp auth provider not to override the Auth header if it's already exits ([#45575](https://github.com/kubernetes/kubernetes/pull/45575), [@wanghaoran1988](https://github.com/wanghaoran1988))

  * The oidc client plugin has reduce round trips and fix scopes requested ([#45317](https://github.com/kubernetes/kubernetes/pull/45317), [@ericchiang](https://github.com/ericchiang))

  * API requests using impersonation now include the system:authenticated group in the impersonated user automatically. ([#44076](https://github.com/kubernetes/kubernetes/pull/44076), [@liggitt](https://github.com/liggitt))

  * RBAC role and rolebinding auto-reconciliation is now performed only when the RBAC authorization mode is enabled. ([#43813](https://github.com/kubernetes/kubernetes/pull/43813), [@liggitt](https://github.com/liggitt))

  * PodSecurityPolicy now recognizes pods that specify runAsNonRoot: false in their security context and does not overwrite the specified value ([#47073](https://github.com/kubernetes/kubernetes/pull/47073), [@Q-Lee](https://github.com/Q-Lee))

  * Tokens retrieved from Google Cloud with application default credentials will not be cached if the client fails authorization ([#46694](https://github.com/kubernetes/kubernetes/pull/46694), [@matt-tyler](https://github.com/matt-tyler))

  * Update kube-dns, metadata-proxy, and fluentd-gcp, event-exporter, prometheus-to-sd, and ip-masq-agent addons with new base images containing fixes for CVE-2016-4448, CVE-2016-9841, CVE-2016-9843, CVE-2017-1000366, CVE-2017-2616, and CVE-2017-9526. ([#47877](https://github.com/kubernetes/kubernetes/pull/47877), [@ixdy](https://github.com/ixdy))

  * Fixed an issue mounting the wrong secret into pods as a service account token. ([#44102](https://github.com/kubernetes/kubernetes/pull/44102), [@ncdc](https://github.com/ncdc))

#### Scalability

* The HorizontalPodAutoscaler controller will now only send updates when it has new status information, reducing the number of writes caused by the controller. ([#47078](https://github.com/kubernetes/kubernetes/pull/47078), [@DirectXMan12](https://github.com/DirectXMan12))


## **External Dependency Version Information**

Continuous integration builds have used the following versions of external dependencies, however, this is not a strong recommendation and users should consult an appropriate installation or upgrade guide before deciding what versions of etcd, docker or rkt to use.

* Docker versions 1.10.3, 1.11.2, 1.12.6 have been validated

    * Docker version 1.12.6 known issues

        * overlay2 driver not fully supported

        * live-restore not fully supported

        * no shared pid namespace support

    * Docker version 1.11.2 known issues

        * Kernel crash with Aufs storage driver on Debian Jessie ([#27885](https://github.com/kubernetes/kubernetes/pull/27885)) which can be identified by the [node problem detector](https://kubernetes.io/docs/tasks/debug-application-cluster/monitor-node-health/)

        * Leaked File descriptors ([#275](https://github.com/docker/containerd/issues/275))

        * Additional memory overhead per container ([#21737](https://github.com/kubernetes/kubernetes/pull/21737))

    * Docker 1.10.3 contains [backports provided by RedHat](https://github.com/docker/docker/compare/v1.10.3...runcom:docker-1.10.3-stable) for known issues

* For issues with Docker 1.13.X please see the [1.13.X tracking issue](https://github.com/kubernetes/kubernetes/issues/42926)

* rkt version 1.23.0+

    * known issues with the rkt runtime are [listed in the Getting Started Guide](https://kubernetes.io/docs/getting-started-guides/rkt/notes/)

* etcd version 3.0.17

* Go version: 1.8.3. [Link to announcement](https://groups.google.com/d/msg/kubernetes-dev/0XRRz6UhhTM/YODWVnuDBQAJ)

    * Kubernetes can only be compiled with Go 1.8. Support for all other versions is dropped.


### Previous Releases Included in v1.7.0
- [v1.7.0-rc.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-rc1)
- [v1.7.0-beta.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-beta2)
- [v1.7.0-beta.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-beta1)
- [v1.7.0-alpha.4](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-alpha4)
- [v1.7.0-alpha.3](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-alpha3)
- [v1.7.0-alpha.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-alpha2)
- [v1.7.0-alpha.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG.md#v170-alpha1)



# v1.7.0-rc.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.0-beta.2

### Action Required

* The following alpha API groups were unintentionally enabled by default in previous releases, and will no longer be enabled by default in v1.8: ([#47690](https://github.com/kubernetes/kubernetes/pull/47690), [@caesarxuchao](https://github.com/caesarxuchao))
    * rbac.authorization.k8s.io/v1alpha1
    * settings.k8s.io/v1alpha1
    * If you wish to continue using them in v1.8, please enable them explicitly using the `--runtime-config` flag of the apiserver (for example, `--runtime-config="rbac.authorization.k8s.io/v1alpha1,settings.k8s.io/v1alpha1"`)
* Paths containing backsteps (for example, "../bar") are no longer allowed in hostPath volume paths, or in volumeMount subpaths ([#47290](https://github.com/kubernetes/kubernetes/pull/47290), [@jhorwit2](https://github.com/jhorwit2))
* Azure: Change container permissions to private for provisioned volumes. If you have existing Azure volumes that were created by Kubernetes v1.6.0-v1.6.5, you should change the permissions on them manually. ([#47605](https://github.com/kubernetes/kubernetes/pull/47605), [@brendandburns](https://github.com/brendandburns))

### Other notable changes

* Update kube-dns, metadata-proxy, and fluentd-gcp, event-exporter, prometheus-to-sd, and ip-masq-agent addons with new base images containing fixes for CVE-2016-4448, CVE-2016-9841, CVE-2016-9843,  CVE-2017-1000366, CVE-2017-2616, and CVE-2017-9526. ([#47877](https://github.com/kubernetes/kubernetes/pull/47877), [@ixdy](https://github.com/ixdy))
* Bump the memory request/limit for ip-masq-daemon. ([#47887](https://github.com/kubernetes/kubernetes/pull/47887), [@dnardo](https://github.com/dnardo))
* HostAliases is now parsed with `hostAliases` json keys to be in line with the feature's name. ([#47512](https://github.com/kubernetes/kubernetes/pull/47512), [@rickypai](https://github.com/rickypai))
* Fixes issue w/Flex volume, introduced in 1.6.0, where drivers without an attacher would fail (node indefinitely waiting for attach). Drivers that don't implement attach should return `attach: false` on `init`. ([#47503](https://github.com/kubernetes/kubernetes/pull/47503), [@chakri-nelluri](https://github.com/chakri-nelluri))
* Tokens retrieved from Google Cloud with application default credentials will not be cached if the client fails authorization ([#46694](https://github.com/kubernetes/kubernetes/pull/46694), [@matt-tyler](https://github.com/matt-tyler))
* ip-masq-agent is now the default for GCE ([#47794](https://github.com/kubernetes/kubernetes/pull/47794), [@dnardo](https://github.com/dnardo))
* Taints support in gce/salt startup scripts.  ([#47632](https://github.com/kubernetes/kubernetes/pull/47632), [@mwielgus](https://github.com/mwielgus))
* Fix VolumeClaims/capacity in "kubectl describe statefulsets" output. ([#47573](https://github.com/kubernetes/kubernetes/pull/47573), [@k82cn](https://github.com/k82cn))
* New 'service.beta.kubernetes.io/aws-load-balancer-extra-security-groups' Service annotation to specify extra Security Groups to be added to ELB created by AWS cloudprovider ([#45268](https://github.com/kubernetes/kubernetes/pull/45268), [@redbaron](https://github.com/redbaron))
* AWS: clean up blackhole routes when using kubenet ([#47572](https://github.com/kubernetes/kubernetes/pull/47572), [@justinsb](https://github.com/justinsb))
* The protobuf serialization of API objects has been updated to store maps in a predictable order to ensure that the representation of that object does not change when saved into etcd. This prevents the same object from being seen as being modified, even when no values have changed. ([#47701](https://github.com/kubernetes/kubernetes/pull/47701), [@smarterclayton](https://github.com/smarterclayton))
* Mark Static pods on the Master as critical ([#47356](https://github.com/kubernetes/kubernetes/pull/47356), [@dashpole](https://github.com/dashpole))
* kubectl logs with label selector supports specifying a container name ([#44282](https://github.com/kubernetes/kubernetes/pull/44282), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Adds an approval work flow to the the certificate approver that will approve certificate signing requests from kubelets that meet all the criteria of kubelet server certificates. ([#46884](https://github.com/kubernetes/kubernetes/pull/46884), [@jcbsmpsn](https://github.com/jcbsmpsn))
* AWS: Maintain a cache of all instances, to fix problem with > 200 nodes with ELBs ([#47410](https://github.com/kubernetes/kubernetes/pull/47410), [@justinsb](https://github.com/justinsb))
* Bump GLBC version to 0.9.5 - fixes [loss of manually modified GCLB health check settings](https://github.com/kubernetes/kubernetes/issues/47559) upon upgrade from pre-1.6.4 to either 1.6.4 or 1.6.5. ([#47567](https://github.com/kubernetes/kubernetes/pull/47567), [@nicksardo](https://github.com/nicksardo))
* Update cluster-proportional-autoscaler, metadata-proxy, and fluentd-gcp addons with fixes for CVE-2016-4448, CVE-2016-8859, CVE-2016-9841, CVE-2016-9843, and CVE-2017-9526. ([#47545](https://github.com/kubernetes/kubernetes/pull/47545), [@ixdy](https://github.com/ixdy))
* AWS: Batch DescribeInstance calls with nodeNames to 150 limit, to stay within AWS filter limits. ([#47516](https://github.com/kubernetes/kubernetes/pull/47516), [@gnufied](https://github.com/gnufied))



# v1.7.0-beta.2

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.0-beta.1

### Action Required

* New and upgraded 1.7 GCE/GKE clusters no longer have an RBAC ClusterRoleBinding that grants the `cluster-admin` ClusterRole to the `default` service account in the `kube-system` namespace. ([#46750](https://github.com/kubernetes/kubernetes/pull/46750), [@cjcullen](https://github.com/cjcullen))
    * If this permission is still desired, run the following command to explicitly grant it, either before or after upgrading to 1.7:
    *     kubectl create clusterrolebinding kube-system-default --serviceaccount=kube-system:default --clusterrole=cluster-admin

### Other notable changes

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



# v1.7.0-beta.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/release-1.7/examples)

## Changelog since v1.7.0-alpha.4

### Action Required

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



# v1.7.0-alpha.4

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.7.0-alpha.3

### Action Required

* `kubectl create role` and `kubectl create clusterrole` no longer allow specifying multiple resource names as comma-separated arguments. Use repeated `--resource-name` arguments to specify multiple resource names.  ([#44950](https://github.com/kubernetes/kubernetes/pull/44950), [@xilabao](https://github.com/xilabao))

### Other notable changes

* avoid concrete examples for missingResourceError ([#45582](https://github.com/kubernetes/kubernetes/pull/45582), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Fix DNS suffix search list support in Windows kube-proxy. ([#45642](https://github.com/kubernetes/kubernetes/pull/45642), [@JiangtianLi](https://github.com/JiangtianLi))
* Fix the bug where StartedAt time is not reported for exited containers. ([#45977](https://github.com/kubernetes/kubernetes/pull/45977), [@yujuhong](https://github.com/yujuhong))
* Update Dashboard version to 1.6.1 ([#45953](https://github.com/kubernetes/kubernetes/pull/45953), [@maciaszczykm](https://github.com/maciaszczykm))
* Examples: fixed cassandra mirror detection that assumes an FTP site will always be presented ([#45965](https://github.com/kubernetes/kubernetes/pull/45965), [@pompomJuice](https://github.com/pompomJuice))
* Removes the deprecated kubelet flag --babysit-daemons ([#44230](https://github.com/kubernetes/kubernetes/pull/44230), [@mtaufen](https://github.com/mtaufen))
* [Federation] Automate configuring nameserver in cluster-dns for CoreDNS provider ([#42895](https://github.com/kubernetes/kubernetes/pull/42895), [@shashidharatd](https://github.com/shashidharatd))
* Add an AEAD encrypting transformer for storing secrets encrypted at rest ([#41939](https://github.com/kubernetes/kubernetes/pull/41939), [@smarterclayton](https://github.com/smarterclayton))
* Update Minio example ([#45444](https://github.com/kubernetes/kubernetes/pull/45444), [@NitishT](https://github.com/NitishT))
* [Federation] Segregate DNS related code to separate controller ([#45034](https://github.com/kubernetes/kubernetes/pull/45034), [@shashidharatd](https://github.com/shashidharatd))
* API Registration is now in beta. ([#45247](https://github.com/kubernetes/kubernetes/pull/45247), [@mbohlool](https://github.com/mbohlool))
* Allow kcm and scheduler to lock on ConfigMaps. ([#45739](https://github.com/kubernetes/kubernetes/pull/45739), [@timothysc](https://github.com/timothysc))
* kubelet config should actually ignore files starting with dots ([#45111](https://github.com/kubernetes/kubernetes/pull/45111), [@dwradcliffe](https://github.com/dwradcliffe))
* Fix lint failures on kubernetes-e2e charm ([#45832](https://github.com/kubernetes/kubernetes/pull/45832), [@Cynerva](https://github.com/Cynerva))
* Mirror pods must now indicate the nodeName they are bound to on creation. The mirror pod annotation is now treated as immutable and cannot be added to an existing pod, removed from a pod, or modified. ([#45775](https://github.com/kubernetes/kubernetes/pull/45775), [@liggitt](https://github.com/liggitt))
* Updating apiserver to return UID of the deleted resource. Clients can use this UID to verify that the resource was deleted or waiting for finalizers. ([#45600](https://github.com/kubernetes/kubernetes/pull/45600), [@nikhiljindal](https://github.com/nikhiljindal))
* OwnerReferencesPermissionEnforcement admission plugin ignores pods/status. ([#45747](https://github.com/kubernetes/kubernetes/pull/45747), [@derekwaynecarr](https://github.com/derekwaynecarr))
* prevent pods/status from touching ownerreferences ([#45826](https://github.com/kubernetes/kubernetes/pull/45826), [@deads2k](https://github.com/deads2k))
* Fix lint errors in juju kubernetes master and e2e charms ([#45494](https://github.com/kubernetes/kubernetes/pull/45494), [@ktsakalozos](https://github.com/ktsakalozos))
* Ensure that autoscaling/v1 is the preferred version for API discovery when autoscaling/v2alpha1 is enabled. ([#45741](https://github.com/kubernetes/kubernetes/pull/45741), [@DirectXMan12](https://github.com/DirectXMan12))
* Promotes Source IP preservation for Virtual IPs to GA. ([#41162](https://github.com/kubernetes/kubernetes/pull/41162), [@MrHohn](https://github.com/MrHohn))
    * Two api fields are defined correspondingly:
        * Service.Spec.ExternalTrafficPolicy <- 'service.beta.kubernetes.io/external-traffic' annotation.
        * Service.Spec.HealthCheckNodePort <- 'service.beta.kubernetes.io/healthcheck-nodeport' annotation.
* Fix pods failing to start if they specify a file as a volume subPath to mount. ([#45623](https://github.com/kubernetes/kubernetes/pull/45623), [@wongma7](https://github.com/wongma7))
* the resource quota controller was not adding quota to be resynced at proper interval ([#45685](https://github.com/kubernetes/kubernetes/pull/45685), [@derekwaynecarr](https://github.com/derekwaynecarr))
* Marks the Kubelet's --master-service-namespace flag deprecated ([#44250](https://github.com/kubernetes/kubernetes/pull/44250), [@mtaufen](https://github.com/mtaufen))
* fluentd will tolerate all NoExecute Taints when run in gcp configuration. ([#45715](https://github.com/kubernetes/kubernetes/pull/45715), [@gmarek](https://github.com/gmarek))
* Added Group/Version/Kind and Action extension to OpenAPI Operations  ([#44787](https://github.com/kubernetes/kubernetes/pull/44787), [@mbohlool](https://github.com/mbohlool))
* Updates kube-dns to 1.14.2 ([#45684](https://github.com/kubernetes/kubernetes/pull/45684), [@bowei](https://github.com/bowei))
    * Support kube-master-url flag without kubeconfig
    * Fix concurrent R/Ws in dns.go
    * Fix confusing logging when initialize server
    * Fix printf in cmd/kube-dns/app/server.go
    * Fix version on startup and --version flag
    * Support specifying port number for nameserver in stubDomains
* detach the volume when pod is terminated ([#45286](https://github.com/kubernetes/kubernetes/pull/45286), [@gnufied](https://github.com/gnufied))
* Don't append :443 to registry domain in the kubernetes-worker layer registry action ([#45550](https://github.com/kubernetes/kubernetes/pull/45550), [@jacekn](https://github.com/jacekn))
* vSphere cloud provider: Fix volume detach on node failure. ([#45569](https://github.com/kubernetes/kubernetes/pull/45569), [@divyenpatel](https://github.com/divyenpatel))
* Remove the deprecated `--enable-cri` flag. CRI is now the default,  ([#45194](https://github.com/kubernetes/kubernetes/pull/45194), [@yujuhong](https://github.com/yujuhong))
    * and the only way to integrate with kubelet for the container runtimes.
* AWS: Remove check that forces loadBalancerSourceRanges to be 0.0.0.0/0.  ([#38636](https://github.com/kubernetes/kubernetes/pull/38636), [@dhawal55](https://github.com/dhawal55))
* Fix erroneous FailedSync and FailedMount events being periodically and indefinitely posted on Pods after kubelet is restarted ([#44781](https://github.com/kubernetes/kubernetes/pull/44781), [@wongma7](https://github.com/wongma7))
* Kubernetes now shares a single PID namespace among all containers in a pod when running with docker >= 1.13.1. This means processes can now signal processes in other containers in a pod, but it also means that the `kubectl exec {pod} kill 1` pattern will cause the pod to be restarted rather than a single container. ([#45236](https://github.com/kubernetes/kubernetes/pull/45236), [@verb](https://github.com/verb))
* azure: add support for UDP ports ([#45523](https://github.com/kubernetes/kubernetes/pull/45523), [@colemickens](https://github.com/colemickens))
    * azure: fix support for multiple `loadBalancerSourceRanges`
    * azure: support the Service spec's `sessionAffinity`
* The fix makes scheduling go routine waiting for cache (e.g. Pod) to be synced. ([#45453](https://github.com/kubernetes/kubernetes/pull/45453), [@k82cn](https://github.com/k82cn))
* vSphere cloud provider: Filter out IPV6 node addresses. ([#45181](https://github.com/kubernetes/kubernetes/pull/45181), [@BaluDontu](https://github.com/BaluDontu))
* Default behaviour in cinder storageclass is changed. If availability is not specified, the zone is chosen by algorithm. It makes possible to spread stateful pods across many zones. ([#44798](https://github.com/kubernetes/kubernetes/pull/44798), [@zetaab](https://github.com/zetaab))
* A small clean up to remove unnecessary functions. ([#45018](https://github.com/kubernetes/kubernetes/pull/45018), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))
* Removed old scheduler constructor. ([#45472](https://github.com/kubernetes/kubernetes/pull/45472), [@k82cn](https://github.com/k82cn))
* vSphere cloud provider: Fix fetching of VM UUID on Ubuntu 16.04 and Fedora. ([#45311](https://github.com/kubernetes/kubernetes/pull/45311), [@divyenpatel](https://github.com/divyenpatel))
* This fixes the overflow for priorityconfig-  valid range {1, 9223372036854775806}. ([#45122](https://github.com/kubernetes/kubernetes/pull/45122), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))
* Bump cluster autoscaler to v0.5.4, which fixes scale down issues with pods ignoring SIGTERM. ([#45483](https://github.com/kubernetes/kubernetes/pull/45483), [@mwielgus](https://github.com/mwielgus))
* Create clusters with GPUs in GKE by specifying "type=<gpu-type>,count=<gpu-count>" to NODE_ACCELERATORS env var. ([#45130](https://github.com/kubernetes/kubernetes/pull/45130), [@vishh](https://github.com/vishh))
    * List of available GPUs - https://cloud.google.com/compute/docs/gpus/#introduction
* Remove deprecated node address type `NodeLegacyHostIP`. ([#44830](https://github.com/kubernetes/kubernetes/pull/44830), [@NickrenREN](https://github.com/NickrenREN))
* UIDs and GIDs now use apimachinery types ([#44714](https://github.com/kubernetes/kubernetes/pull/44714), [@jamiehannaford](https://github.com/jamiehannaford))
* Enable basic auth username rotation for GCI ([#44590](https://github.com/kubernetes/kubernetes/pull/44590), [@ihmccreery](https://github.com/ihmccreery))
* Kubectl taint node based on label selector ([#44740](https://github.com/kubernetes/kubernetes/pull/44740), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))
* Scheduler perf modular extensions. ([#44770](https://github.com/kubernetes/kubernetes/pull/44770), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))



# v1.7.0-alpha.3

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.7.0-alpha.2

### Action Required

* Refactor kube-proxy configuration ([#34727](https://github.com/kubernetes/kubernetes/pull/34727), [@ncdc](https://github.com/ncdc))

### Other notable changes

* kubeadm: Fix invalid assign statement so it is possible to register the master kubelet with other initial Taints ([#45376](https://github.com/kubernetes/kubernetes/pull/45376), [@luxas](https://github.com/luxas))
* Use Docker API Version instead of docker version ([#44068](https://github.com/kubernetes/kubernetes/pull/44068), [@mkumatag](https://github.com/mkumatag))
* bump(golang.org/x/oauth2): a6bd8cefa1811bd24b86f8902872e4e8225f74c4 ([#45056](https://github.com/kubernetes/kubernetes/pull/45056), [@ericchiang](https://github.com/ericchiang))
* apimachinery: make explicit that meta.KindToResource is only a guess ([#45272](https://github.com/kubernetes/kubernetes/pull/45272), [@sttts](https://github.com/sttts))
* Remove PodSandboxStatus.Linux.Namespaces.Network from CRI. ([#45166](https://github.com/kubernetes/kubernetes/pull/45166), [@feiskyer](https://github.com/feiskyer))
* Fixed misspelled http URL in the cluster-dns example ([#45246](https://github.com/kubernetes/kubernetes/pull/45246), [@psiwczak](https://github.com/psiwczak))
* separate discovery from the apiserver ([#43003](https://github.com/kubernetes/kubernetes/pull/43003), [@deads2k](https://github.com/deads2k))
* Remove the `--secret-name` flag from `kubefed join`, instead generating the secret name arbitrarily. ([#42513](https://github.com/kubernetes/kubernetes/pull/42513), [@perotinus](https://github.com/perotinus))
* Added InterPodAffinity unit test case with Namespace. ([#45152](https://github.com/kubernetes/kubernetes/pull/45152), [@k82cn](https://github.com/k82cn))
* Use munged semantic version for side-loaded docker tag ([#44981](https://github.com/kubernetes/kubernetes/pull/44981), [@ixdy](https://github.com/ixdy))
* Increase Dashboard's memory requests and limits ([#44712](https://github.com/kubernetes/kubernetes/pull/44712), [@maciaszczykm](https://github.com/maciaszczykm))
* PodSpec's `HostAliases` now write entries into the Kubernetes-managed hosts file. ([#45148](https://github.com/kubernetes/kubernetes/pull/45148), [@rickypai](https://github.com/rickypai))
* Create and push a docker image for the cloud-controller-manager ([#45154](https://github.com/kubernetes/kubernetes/pull/45154), [@luxas](https://github.com/luxas))
* Align Extender's validation with prioritizers. ([#45091](https://github.com/kubernetes/kubernetes/pull/45091), [@k82cn](https://github.com/k82cn))
* Retry calls we report config changes quickly. ([#44959](https://github.com/kubernetes/kubernetes/pull/44959), [@ktsakalozos](https://github.com/ktsakalozos))
* A new field `hostAliases` has been added to `pod.spec` to support adding entries to a Pod's /etc/hosts file. ([#44641](https://github.com/kubernetes/kubernetes/pull/44641), [@rickypai](https://github.com/rickypai))
* Added CIFS PV support for Juju Charms ([#45117](https://github.com/kubernetes/kubernetes/pull/45117), [@chuckbutler](https://github.com/chuckbutler))
* Some container runtimes share a process (PID) namespace for all containers in a pod. This will become the default for Docker in a future release of Kubernetes. You can preview this functionality if running with the CRI and Docker 1.13.1 by enabling the --experimental-docker-enable-shared-pid kubelet flag. ([#41583](https://github.com/kubernetes/kubernetes/pull/41583), [@verb](https://github.com/verb))
* add APIService conditions ([#43301](https://github.com/kubernetes/kubernetes/pull/43301), [@deads2k](https://github.com/deads2k))
* Log warning when invalid dir passed to kubectl proxy --www ([#44952](https://github.com/kubernetes/kubernetes/pull/44952), [@CaoShuFeng](https://github.com/CaoShuFeng))
* Roll up volume error messages in the kubelet sync loop. ([#44938](https://github.com/kubernetes/kubernetes/pull/44938), [@jayunit100](https://github.com/jayunit100))
* Introduces the ability to extend kubectl by adding third-party plugins. Developer preview, please refer to the documentation for instructions about how to use it. ([#37499](https://github.com/kubernetes/kubernetes/pull/37499), [@fabianofranz](https://github.com/fabianofranz))
* Fixes juju kubernetes master: 1. Get certs from a dead leader. 2. Append tokens. ([#43620](https://github.com/kubernetes/kubernetes/pull/43620), [@ktsakalozos](https://github.com/ktsakalozos))
* Use correct option name in the kubernetes-worker layer registry action ([#44921](https://github.com/kubernetes/kubernetes/pull/44921), [@jacekn](https://github.com/jacekn))
* Start recording cloud provider metrics for AWS ([#43477](https://github.com/kubernetes/kubernetes/pull/43477), [@gnufied](https://github.com/gnufied))
* Bump GLBC version to 0.9.3 ([#45055](https://github.com/kubernetes/kubernetes/pull/45055), [@nicksardo](https://github.com/nicksardo))
* Add metrics to all major gce operations {latency, errors} ([#44510](https://github.com/kubernetes/kubernetes/pull/44510), [@bowei](https://github.com/bowei))
    * The new metrics are:
    *   cloudprovider_gce_api_request_duration_seconds{request, region, zone}
    *   cloudprovider_gce_api_request_errors{request, region, zone}
 
    * `request` is the specific function that is used.
    * `region` is the target region (Will be "<n/a>" if not applicable)
    * `zone` is the target zone (Will be "<n/a>" if not applicable)
    * Note: this fixes some issues with the previous implementation of
    * metrics for disks:
        * Time duration tracked was of the initial API call, not the entire
    *   operation.
        * Metrics label tuple would have resulted in many independent
    *   histograms stored, one for each disk. (Did not aggregate well).
* Update kubernetes-e2e charm to use snaps ([#45044](https://github.com/kubernetes/kubernetes/pull/45044), [@Cynerva](https://github.com/Cynerva))
* Log the error (if any) in e2e metrics gathering step ([#45039](https://github.com/kubernetes/kubernetes/pull/45039), [@shyamjvs](https://github.com/shyamjvs))
* The proxy subresource APIs for nodes, services, and pods now support the HTTP PATCH method. ([#44929](https://github.com/kubernetes/kubernetes/pull/44929), [@liggitt](https://github.com/liggitt))
* cluster-autoscaler: Fix duplicate writing of logs. ([#45017](https://github.com/kubernetes/kubernetes/pull/45017), [@MaciekPytel](https://github.com/MaciekPytel))
* CRI: Fix StopContainer timeout ([#44970](https://github.com/kubernetes/kubernetes/pull/44970), [@Random-Liu](https://github.com/Random-Liu))
* Fixes a bug where pods were evicted even after images are successfully deleted. ([#44986](https://github.com/kubernetes/kubernetes/pull/44986), [@dashpole](https://github.com/dashpole))
* Fix some false negatives in detection of meaningful conflicts during strategic merge patch with maps and lists. ([#43469](https://github.com/kubernetes/kubernetes/pull/43469), [@enisoc](https://github.com/enisoc))
* kubernetes-master juju charm properly detects etcd-scale events and reconfigures appropriately. ([#44967](https://github.com/kubernetes/kubernetes/pull/44967), [@chuckbutler](https://github.com/chuckbutler))
* Add redirect support to SpdyRoundTripper ([#44451](https://github.com/kubernetes/kubernetes/pull/44451), [@ncdc](https://github.com/ncdc))
* Support running Ubuntu image on GCE node ([#44744](https://github.com/kubernetes/kubernetes/pull/44744), [@yguo0905](https://github.com/yguo0905))
* Send dns details only after cdk-addons are configured ([#44945](https://github.com/kubernetes/kubernetes/pull/44945), [@ktsakalozos](https://github.com/ktsakalozos))
* Added support to the pause action in the kubernetes-worker charm for new flag --delete-local-data ([#44931](https://github.com/kubernetes/kubernetes/pull/44931), [@chuckbutler](https://github.com/chuckbutler))
* Upgrade go version to v1.8 ([#41636](https://github.com/kubernetes/kubernetes/pull/41636), [@luxas](https://github.com/luxas))
* Add namespace-{list, create, delete} actions to the kubernetes-master layer ([#44277](https://github.com/kubernetes/kubernetes/pull/44277), [@jacekn](https://github.com/jacekn))
* Fix problems with scaling up the cluster when unschedulable pods have some persistent volume claims. ([#44860](https://github.com/kubernetes/kubernetes/pull/44860), [@mwielgus](https://github.com/mwielgus))
* Feature/hpa upscale downscale delay configurable ([#42101](https://github.com/kubernetes/kubernetes/pull/42101), [@Dmitry1987](https://github.com/Dmitry1987))
* Add short name "netpol" for networkpolicies ([#42241](https://github.com/kubernetes/kubernetes/pull/42241), [@xiangpengzhao](https://github.com/xiangpengzhao))
* Restored the ability of kubectl running inside a pod to consume resource files specifying a different namespace than the one the pod is running in. ([#44862](https://github.com/kubernetes/kubernetes/pull/44862), [@liggitt](https://github.com/liggitt))
* e2e: handle nil ReplicaSet in checkDeploymentRevision ([#44859](https://github.com/kubernetes/kubernetes/pull/44859), [@sttts](https://github.com/sttts))
* Fix false positive "meaningful conflict" detection for strategic merge patch with integer values. ([#44788](https://github.com/kubernetes/kubernetes/pull/44788), [@enisoc](https://github.com/enisoc))
* Documented NodePort networking for CDK. ([#44863](https://github.com/kubernetes/kubernetes/pull/44863), [@chuckbutler](https://github.com/chuckbutler))
* Deployments and DaemonSets are now considered complete once all of the new pods are up and running - affects `kubectl rollout status` (and ProgressDeadlineSeconds for Deployments) ([#44672](https://github.com/kubernetes/kubernetes/pull/44672), [@kargakis](https://github.com/kargakis))
* Exclude nodes labeled as master from LoadBalancer / NodePort; restores documented behaviour. ([#44745](https://github.com/kubernetes/kubernetes/pull/44745), [@justinsb](https://github.com/justinsb))
* Fixes issue during LB creation where ports where incorrectly assigned to a floating IP ([#44387](https://github.com/kubernetes/kubernetes/pull/44387), [@jamiehannaford](https://github.com/jamiehannaford))
* Remove redis-proxy.yaml sample, as the image is nowhere to be found. ([#44801](https://github.com/kubernetes/kubernetes/pull/44801), [@klausenbusk](https://github.com/klausenbusk))
* Resolves juju vsphere hostname bug showing only a single node in a scaled node-pool. ([#44780](https://github.com/kubernetes/kubernetes/pull/44780), [@chuckbutler](https://github.com/chuckbutler))
* kubectl commands run inside a pod using a kubeconfig file now use the namespace specified in the kubeconfig file, instead of using the pod namespace. If no kubeconfig file is used, or the kubeconfig does not specify a namespace, the pod namespace is still used as a fallback. ([#44570](https://github.com/kubernetes/kubernetes/pull/44570), [@liggitt](https://github.com/liggitt))
* This adds support for CNI ConfigLists, which permit plugin chaining. ([#42202](https://github.com/kubernetes/kubernetes/pull/42202), [@squeed](https://github.com/squeed))
* API requests using impersonation now include the `system:authenticated` group in the impersonated user automatically. ([#44076](https://github.com/kubernetes/kubernetes/pull/44076), [@liggitt](https://github.com/liggitt))
* Print conditions of RC/RS in 'kubectl describe' command. ([#44710](https://github.com/kubernetes/kubernetes/pull/44710), [@xiangpengzhao](https://github.com/xiangpengzhao))
* cinder: Add support for the KVM virtio-scsi driver ([#41498](https://github.com/kubernetes/kubernetes/pull/41498), [@mikebryant](https://github.com/mikebryant))
* Disallows installation of upstream docker from PPA in the Juju kubernetes-worker charm. ([#44681](https://github.com/kubernetes/kubernetes/pull/44681), [@wwwtyro](https://github.com/wwwtyro))
* Fluentd manifest pod is no longer created on non-registered master when creating clusters using kube-up.sh. ([#44721](https://github.com/kubernetes/kubernetes/pull/44721), [@piosz](https://github.com/piosz))
* Job controller now respects ControllerRef to avoid fighting over Pods. ([#42176](https://github.com/kubernetes/kubernetes/pull/42176), [@enisoc](https://github.com/enisoc))
* CronJob controller now respects ControllerRef to avoid fighting with other controllers. ([#42177](https://github.com/kubernetes/kubernetes/pull/42177), [@enisoc](https://github.com/enisoc))
* The hyperkube image has been slimmed down and no longer includes addon manifests and other various scripts. These were introduced for the now removed docker-multinode setup system. ([#44555](https://github.com/kubernetes/kubernetes/pull/44555), [@luxas](https://github.com/luxas))
* Refactoring reorganize taints function in kubectl to expose operations ([#43171](https://github.com/kubernetes/kubernetes/pull/43171), [@ravisantoshgudimetla](https://github.com/ravisantoshgudimetla))
* The Kubernetes API server now exits if it encounters a networking failure (e.g. the networking interface hosting its address goes away) to allow a process manager (systemd/kubelet/etc) to react to the problem.  Previously the server would log the failure and try again to bind to its configured address:port. ([#42272](https://github.com/kubernetes/kubernetes/pull/42272), [@marun](https://github.com/marun))
* Fixes a bug in the kubernetes-worker Juju charm code that attempted to give kube-proxy more than one api endpoint. ([#44677](https://github.com/kubernetes/kubernetes/pull/44677), [@wwwtyro](https://github.com/wwwtyro))
* Fixes a missing comma in a list of strings. ([#44678](https://github.com/kubernetes/kubernetes/pull/44678), [@wwwtyro](https://github.com/wwwtyro))
* Fix ceph-secret type to kubernetes.io/rbd in kubernetes-master charm ([#44635](https://github.com/kubernetes/kubernetes/pull/44635), [@Cynerva](https://github.com/Cynerva))



# v1.7.0-alpha.2

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.7.0-alpha.1

### Action Required

* `kubectl create rolebinding` and `kubectl create clusterrolebinding` no longer allow specifying multiple subjects as comma-separated arguments. Use repeated `--user`, `--group`, or `--serviceaccount` arguments to specify multiple subjects.  ([#43903](https://github.com/kubernetes/kubernetes/pull/43903), [@xilabao](https://github.com/xilabao))

### Other notable changes

* Add support for Azure internal load balancer ([#43510](https://github.com/kubernetes/kubernetes/pull/43510), [@karataliu](https://github.com/karataliu))
* Improved output on 'kubectl get' and 'kubectl describe' for generic objects. ([#44222](https://github.com/kubernetes/kubernetes/pull/44222), [@fabianofranz](https://github.com/fabianofranz))
* Add Kubernetes 1.6 support to Juju charms ([#44500](https://github.com/kubernetes/kubernetes/pull/44500), [@Cynerva](https://github.com/Cynerva))
    * Add metric collection to charms for autoscaling
    * Update kubernetes-e2e charm to fail when test suite fails
    * Update Juju charms to use snaps
    * Add registry action to the kubernetes-worker charm
    * Add support for kube-proxy cluster-cidr option to kubernetes-worker charm
    * Fix kubernetes-master charm starting services before TLS certs are saved
    * Fix kubernetes-worker charm failures in LXD
    * Fix stop hook failure on kubernetes-worker charm
    * Fix handling of juju kubernetes-worker.restart-needed state
    * Fix nagios checks in charms
* Users can now specify listen and advertise URLs for etcd in a kubeadm cluster  ([#42246](https://github.com/kubernetes/kubernetes/pull/42246), [@jamiehannaford](https://github.com/jamiehannaford))
* Fixed `kubectl cluster-info dump` to support multi-container pod. ([#44088](https://github.com/kubernetes/kubernetes/pull/44088), [@xingzhou](https://github.com/xingzhou))
* Prints out status updates when running `kubefed init` ([#41849](https://github.com/kubernetes/kubernetes/pull/41849), [@perotinus](https://github.com/perotinus))
* CRI: Fix kubelet failing to start when using rkt. ([#44569](https://github.com/kubernetes/kubernetes/pull/44569), [@yujuhong](https://github.com/yujuhong))
* Remove deprecatedPublicIPs field ([#44519](https://github.com/kubernetes/kubernetes/pull/44519), [@thockin](https://github.com/thockin))
* Remove deprecated ubuntu kube-up deployment. ([#44344](https://github.com/kubernetes/kubernetes/pull/44344), [@mikedanese](https://github.com/mikedanese))
* Use OS-specific libs when computing client User-Agent in kubectl, etc. ([#44423](https://github.com/kubernetes/kubernetes/pull/44423), [@monopole](https://github.com/monopole))
* kube-apiserver now drops unneeded path information if an older version of Windows kubectl sends it. ([#44421](https://github.com/kubernetes/kubernetes/pull/44421), [@mml](https://github.com/mml))
* Extending the gc admission plugin so that a user who doesn't have delete permission of the *owner* cannot modify blockOwnerDeletion field of existing ownerReferences, or add new ownerReference with blockOwnerDeletion=true ([#43876](https://github.com/kubernetes/kubernetes/pull/43876), [@caesarxuchao](https://github.com/caesarxuchao))
* kube-apiserver: --service-account-lookup now defaults to true, requiring the Secret API object containing the token to exist in order for a service account token to be valid. This enables service account tokens to be revoked by deleting the Secret object containing the token. ([#44071](https://github.com/kubernetes/kubernetes/pull/44071), [@liggitt](https://github.com/liggitt))
* CRI: `kubectl logs -f` now stops following when container stops, as it did pre-CRI. ([#44406](https://github.com/kubernetes/kubernetes/pull/44406), [@Random-Liu](https://github.com/Random-Liu))
* Add completion support for --namespace and --cluster to kubectl ([#44251](https://github.com/kubernetes/kubernetes/pull/44251), [@superbrothers](https://github.com/superbrothers))
* dnsprovider: avoid panic if route53 fields are nil ([#44380](https://github.com/kubernetes/kubernetes/pull/44380), [@justinsb](https://github.com/justinsb))
* In 'kubectl describe', find controllers with ControllerRef, instead of showing the original creator. ([#42849](https://github.com/kubernetes/kubernetes/pull/42849), [@janetkuo](https://github.com/janetkuo))
* Heat cluster operations now support environments that have multiple Swift URLs ([#41561](https://github.com/kubernetes/kubernetes/pull/41561), [@jamiehannaford](https://github.com/jamiehannaford))
* Adds support for allocation of pod IPs via IP aliases. ([#42147](https://github.com/kubernetes/kubernetes/pull/42147), [@bowei](https://github.com/bowei))
* alpha volume provisioning is removed and default storage class should be used instead. ([#44090](https://github.com/kubernetes/kubernetes/pull/44090), [@NickrenREN](https://github.com/NickrenREN))
* validateClusterInfo: use clientcmdapi.NewCluster() ([#44221](https://github.com/kubernetes/kubernetes/pull/44221), [@ncdc](https://github.com/ncdc))
* Fix corner-case with OnlyLocal Service healthchecks. ([#44313](https://github.com/kubernetes/kubernetes/pull/44313), [@thockin](https://github.com/thockin))
* Adds annotations to all Federation objects created by kubefed. ([#42683](https://github.com/kubernetes/kubernetes/pull/42683), [@perotinus](https://github.com/perotinus))
* [Federation][Kubefed] Bug fix to enable disabling federation controllers through override args ([#44209](https://github.com/kubernetes/kubernetes/pull/44209), [@irfanurrehman](https://github.com/irfanurrehman))
* [Federation] Remove deprecated federation-apiserver-kubeconfig secret ([#44287](https://github.com/kubernetes/kubernetes/pull/44287), [@shashidharatd](https://github.com/shashidharatd))
* Scheduler can receive its policy configuration from a ConfigMap ([#43892](https://github.com/kubernetes/kubernetes/pull/43892), [@bsalamat](https://github.com/bsalamat))
* AWS cloud provider: fix support running the master with a different AWS account or even on a different cloud provider than the nodes. ([#44235](https://github.com/kubernetes/kubernetes/pull/44235), [@mrIncompetent](https://github.com/mrIncompetent))
* add rancher credential provider ([#40160](https://github.com/kubernetes/kubernetes/pull/40160), [@wlan0](https://github.com/wlan0))
* Support generating Open API extensions for strategic merge patch tags in go struct tags ([#44121](https://github.com/kubernetes/kubernetes/pull/44121), [@mbohlool](https://github.com/mbohlool))
* Use go1.8.1 for arm and ppc64le ([#44216](https://github.com/kubernetes/kubernetes/pull/44216), [@mkumatag](https://github.com/mkumatag))
* Aggregated used ports at the NodeInfo level for `PodFitsHostPorts` predicate. ([#42524](https://github.com/kubernetes/kubernetes/pull/42524), [@k82cn](https://github.com/k82cn))
* Catch error when failed to make directory in NFS volume plugin ([#38801](https://github.com/kubernetes/kubernetes/pull/38801), [@nak3](https://github.com/nak3))
* Support iSCSI CHAP authentication ([#43396](https://github.com/kubernetes/kubernetes/pull/43396), [@rootfs](https://github.com/rootfs))
* Support context completion for kubectl config use-context ([#42336](https://github.com/kubernetes/kubernetes/pull/42336), [@superbrothers](https://github.com/superbrothers))
* print warning when delete current context ([#42538](https://github.com/kubernetes/kubernetes/pull/42538), [@adohe](https://github.com/adohe))
* Add node e2e tests for hostPid ([#44119](https://github.com/kubernetes/kubernetes/pull/44119), [@feiskyer](https://github.com/feiskyer))
* kubeadm: Make `kubeadm reset` tolerant of a disabled docker service. ([#43951](https://github.com/kubernetes/kubernetes/pull/43951), [@luxas](https://github.com/luxas))
* kubelet: make dockershim.sock configurable ([#43914](https://github.com/kubernetes/kubernetes/pull/43914), [@ncdc](https://github.com/ncdc))
* Fix [broken service accounts when using dedicated service account key](https://github.com/kubernetes/kubernetes/issues/44285). ([#44169](https://github.com/kubernetes/kubernetes/pull/44169), [@mikedanese](https://github.com/mikedanese))
* Fix incorrect conflict errors applying strategic merge patches to resources. ([#43871](https://github.com/kubernetes/kubernetes/pull/43871), [@liggitt](https://github.com/liggitt))
* Fix [transition between NotReady and Unreachable taints](https://github.com/kubernetes/kubernetes/issues/43444). ([#44042](https://github.com/kubernetes/kubernetes/pull/44042), [@gmarek](https://github.com/gmarek))
* leader election lock based on scheduler name ([#42961](https://github.com/kubernetes/kubernetes/pull/42961), [@wanghaoran1988](https://github.com/wanghaoran1988))
* [Federation] Remove FEDERATIONS_DOMAIN_MAP references ([#43137](https://github.com/kubernetes/kubernetes/pull/43137), [@shashidharatd](https://github.com/shashidharatd))
* Fix for [federation failing to propagate cascading deletion](https://github.com/kubernetes/kubernetes/issues/44304). ([#44108](https://github.com/kubernetes/kubernetes/pull/44108), [@csbell](https://github.com/csbell))
* Fix bug with service nodeports that have no backends not being rejected, when they should be.  This is not a regression vs v1.5 - it's a fix that didn't quite fix hard enough. ([#43972](https://github.com/kubernetes/kubernetes/pull/43972), [@thockin](https://github.com/thockin))
* Fix for [failure to delete federation controllers with finalizers](https://github.com/kubernetes/kubernetes/issues/43828). ([#44084](https://github.com/kubernetes/kubernetes/pull/44084), [@nikhiljindal](https://github.com/nikhiljindal))
* Fix container hostPid settings. ([#44097](https://github.com/kubernetes/kubernetes/pull/44097), [@feiskyer](https://github.com/feiskyer))
* Fixed an issue mounting the wrong secret into pods as a service account token. ([#44102](https://github.com/kubernetes/kubernetes/pull/44102), [@ncdc](https://github.com/ncdc))



# v1.7.0-alpha.1

[Documentation](https://docs.k8s.io) & [Examples](https://releases.k8s.io/master/examples)

## Changelog since v1.6.0

### Other notable changes

* Juju: Enable GPU mode if GPU hardware detected ([#43467](https://github.com/kubernetes/kubernetes/pull/43467), [@tvansteenburgh](https://github.com/tvansteenburgh))
* Check the error before parsing the apiversion ([#44047](https://github.com/kubernetes/kubernetes/pull/44047), [@yujuhong](https://github.com/yujuhong))
* get-kube-local.sh checks pods with option "--namespace=kube-system" ([#42518](https://github.com/kubernetes/kubernetes/pull/42518), [@mtanino](https://github.com/mtanino))
* Using http2 in kubeapi-load-balancer to fix kubectl exec uses ([#43625](https://github.com/kubernetes/kubernetes/pull/43625), [@mbruzek](https://github.com/mbruzek))
* Support status.hostIP in downward API ([#42717](https://github.com/kubernetes/kubernetes/pull/42717), [@andrewsykim](https://github.com/andrewsykim))
* AWS cloud provider: allow to set KubernetesClusterID or KubernetesClusterTag in combination with VPC. ([#42512](https://github.com/kubernetes/kubernetes/pull/42512), [@scheeles](https://github.com/scheeles))
* changed kubelet default image-gc-high-threshold to 85% to resolve a conflict with default settings in docker that prevented image garbage collection from resolving low disk space situations when using devicemapper storage. ([#40432](https://github.com/kubernetes/kubernetes/pull/40432), [@sjenning](https://github.com/sjenning))
* When creating a container using envFrom, ([#42083](https://github.com/kubernetes/kubernetes/pull/42083), [@fraenkel](https://github.com/fraenkel))
    * 1. validate the name of the ConfigMap in a ConfigMapRef
    * 2. validate the name of the Secret in a SecretRef
* RBAC role and rolebinding auto-reconciliation is now performed only when the RBAC authorization mode is enabled. ([#43813](https://github.com/kubernetes/kubernetes/pull/43813), [@liggitt](https://github.com/liggitt))
* Permission to use a PodSecurityPolicy can now be granted within a single namespace by allowing the `use` verb on the `podsecuritypolicies` resource within the namespace. ([#42360](https://github.com/kubernetes/kubernetes/pull/42360), [@liggitt](https://github.com/liggitt))
* Enable audit log in local cluster ([#42379](https://github.com/kubernetes/kubernetes/pull/42379), [@xilabao](https://github.com/xilabao))
* Fix a deadlock in kubeadm master initialization. ([#43835](https://github.com/kubernetes/kubernetes/pull/43835), [@mikedanese](https://github.com/mikedanese))
* Implement API usage metrics for gce storage ([#40338](https://github.com/kubernetes/kubernetes/pull/40338), [@gnufied](https://github.com/gnufied))
* kubeadm: clean up exited containers and network checkpoints ([#43836](https://github.com/kubernetes/kubernetes/pull/43836), [@yujuhong](https://github.com/yujuhong))
* ActiveDeadlineSeconds is validated in workload controllers now, make sure it's not set anywhere (it shouldn't be set by default and having it set means your controller will restart the Pods at some point) ([#38741](https://github.com/kubernetes/kubernetes/pull/38741), [@sandflee](https://github.com/sandflee))
* azure: all clients poll duration is now 5 seconds ([#43699](https://github.com/kubernetes/kubernetes/pull/43699), [@colemickens](https://github.com/colemickens))
* addressing issue [#39427](https://github.com/kubernetes/kubernetes/pull/39427) adding a flag --output to 'kubectl version' ([#39858](https://github.com/kubernetes/kubernetes/pull/39858), [@alejandroEsc](https://github.com/alejandroEsc))
* Support secure etcd cluster for centos provider. ([#42994](https://github.com/kubernetes/kubernetes/pull/42994), [@Shawyeok](https://github.com/Shawyeok))
* Use Cluster Autoscaler 0.5.1, which fixes an issue in Cluster Autoscaler 0.5 where the cluster may be scaled up unnecessarily. Also the status of Cluster Autoscaler is now exposed in kube-system/cluster-autoscaler-status config map. ([#43745](https://github.com/kubernetes/kubernetes/pull/43745), [@mwielgus](https://github.com/mwielgus))
* Use ProviderID to address nodes in the cloudprovider ([#42604](https://github.com/kubernetes/kubernetes/pull/42604), [@wlan0](https://github.com/wlan0))
* Openstack cinder v1/v2/auto API support ([#40423](https://github.com/kubernetes/kubernetes/pull/40423), [@mkutsevol](https://github.com/mkutsevol))
* API resource discovery now includes the `singularName` used to refer to the resource. ([#43312](https://github.com/kubernetes/kubernetes/pull/43312), [@deads2k](https://github.com/deads2k))
* Add the ability to lock on ConfigMaps to support HA for self hosted components ([#42666](https://github.com/kubernetes/kubernetes/pull/42666), [@timothysc](https://github.com/timothysc))
* OpenStack clusters can now specify whether worker nodes are assigned a floating IP ([#42638](https://github.com/kubernetes/kubernetes/pull/42638), [@jamiehannaford](https://github.com/jamiehannaford))
* Add Host field to TCPSocketAction ([#42902](https://github.com/kubernetes/kubernetes/pull/42902), [@louyihua](https://github.com/louyihua))
* Support StorageClass in Azure file volume ([#42170](https://github.com/kubernetes/kubernetes/pull/42170), [@rootfs](https://github.com/rootfs))
* Be able to specify the timeout to wait for pod for kubectl logs/attach ([#41813](https://github.com/kubernetes/kubernetes/pull/41813), [@shiywang](https://github.com/shiywang))
* Add support for bring-your-own ip address for Services on Azure ([#42034](https://github.com/kubernetes/kubernetes/pull/42034), [@brendandburns](https://github.com/brendandburns))
* kubectl create configmap has a new option --from-env-file that populates a configmap from file which follows a key=val format for each line. ([#38882](https://github.com/kubernetes/kubernetes/pull/38882), [@fraenkel](https://github.com/fraenkel))
* kubectl create secret has a new option --from-env-file that populates a secret from file which follows a key=val format for each line.
* update the signing key for percona debian and ubuntu packages ([#41186](https://github.com/kubernetes/kubernetes/pull/41186), [@dixudx](https://github.com/dixudx))
* fc: Drop multipath.conf snippet ([#36698](https://github.com/kubernetes/kubernetes/pull/36698), [@fabiand](https://github.com/fabiand))
