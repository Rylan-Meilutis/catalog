---
hide:
  - toc
---

# Security Overview

<link href="https://truecharts.org/_static/trivy.css" type="text/css" rel="stylesheet" />

## Helm-Chart

##### Scan Results

#### Chart Object: docker-compose/templates/common.yaml



| Type         |    Misconfiguration ID   |   Check  |  Severity |                   Explaination                   | Links  |
|:----------------|:------------------:|:-----------:|:------------------:|-----------------------------------------|-----------------------------------------|
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv001">https://avd.aquasec.com/appshield/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv001">https://avd.aquasec.com/appshield/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV009   |   Access to host network  |  HIGH | <details><summary>Expand...</summary> Sharing the host’s network namespace permits processes in the pod to communicate with processes bound to the host’s loopback adapter. <br> <hr> <br> StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should not set &#39;spec.template.spec.hostNetwork&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv009">https://avd.aquasec.com/appshield/ksv009</a><br></details>  |
| Kubernetes Security Check         |    KSV011   |   CPU not limited  |  LOW | <details><summary>Expand...</summary> Enforcing CPU limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;resources.limits.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv011">https://avd.aquasec.com/appshield/ksv011</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;autopermissions&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV015   |   CPU requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have resource requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;resources.requests.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv015">https://avd.aquasec.com/appshield/ksv015</a><br></details>  |
| Kubernetes Security Check         |    KSV016   |   Memory requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have memory requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;resources.requests.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv016">https://avd.aquasec.com/appshield/ksv016</a><br></details>  |
| Kubernetes Security Check         |    KSV017   |   Privileged container  |  HIGH | <details><summary>Expand...</summary> Privileged containers share namespaces with the host system and do not offer any security. They should be used exclusively for system containers that require high privileges. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.privileged&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv017">https://avd.aquasec.com/appshield/ksv017</a><br></details>  |
| Kubernetes Security Check         |    KSV017   |   Privileged container  |  HIGH | <details><summary>Expand...</summary> Privileged containers share namespaces with the host system and do not offer any security. They should be used exclusively for system containers that require high privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.privileged&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv017">https://avd.aquasec.com/appshield/ksv017</a><br></details>  |
| Kubernetes Security Check         |    KSV018   |   Memory not limited  |  LOW | <details><summary>Expand...</summary> Enforcing memory limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;resources.limits.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv018">https://avd.aquasec.com/appshield/ksv018</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV022   |   Non-default capabilities added  |  MEDIUM | <details><summary>Expand...</summary> Adding NET_RAW or capabilities beyond the default set must be disallowed. <br> <hr> <br> Container &#39;RELEASE-NAME-docker-compose&#39; of StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should not set &#39;securityContext.capabilities.add&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv022">https://avd.aquasec.com/appshield/ksv022</a><br></details>  |
| Kubernetes Security Check         |    KSV023   |   hostPath volumes mounted  |  MEDIUM | <details><summary>Expand...</summary> HostPath volumes must be forbidden. <br> <hr> <br> StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should not set &#39;spec.template.volumes.hostPath&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv023">https://avd.aquasec.com/appshield/ksv023</a><br></details>  |
| Kubernetes Security Check         |    KSV029   |   A root primary or supplementary GID set  |  LOW | <details><summary>Expand...</summary> Containers should be forbidden from running with a root primary or supplementary GID. <br> <hr> <br> StatefulSet &#39;RELEASE-NAME-docker-compose&#39; should set &#39;spec.securityContext.runAsGroup&#39;, &#39;spec.securityContext.supplementalGroups[*]&#39; and &#39;spec.securityContext.fsGroup&#39; to integer greater than 0 </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv029">https://avd.aquasec.com/appshield/ksv029</a><br></details>  |

## Containers

##### Detected Containers

          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/docker-in-docker:v20.10.14@sha256:7ba99af4bdbea6b6cb39c8df207c43d72b53cb5eac6c4ac29e0dfe40ed368e3b

##### Scan Results


#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| busybox         |    CVE-2022-28391   |   CRITICAL  |  1.34.1-r4 | 1.34.1-r5 | <details><summary>Expand...</summary><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch</a><br><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch</a><br><a href="https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661">https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-28391">https://nvd.nist.gov/vuln/detail/CVE-2022-28391</a><br></details>  |
| ssl_client         |    CVE-2022-28391   |   CRITICAL  |  1.34.1-r4 | 1.34.1-r5 | <details><summary>Expand...</summary><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch</a><br><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch</a><br><a href="https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661">https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-28391">https://nvd.nist.gov/vuln/detail/CVE-2022-28391</a><br></details>  |
| zlib         |    CVE-2018-25032   |   HIGH  |  1.2.11-r3 | 1.2.12-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/03/25/2">http://www.openwall.com/lists/oss-security/2022/03/25/2</a><br><a href="http://www.openwall.com/lists/oss-security/2022/03/26/1">http://www.openwall.com/lists/oss-security/2022/03/26/1</a><br><a href="https://access.redhat.com/security/cve/CVE-2018-25032">https://access.redhat.com/security/cve/CVE-2018-25032</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032</a><br><a href="https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531">https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531</a><br><a href="https://github.com/madler/zlib/compare/v1.2.11...v1.2.12">https://github.com/madler/zlib/compare/v1.2.11...v1.2.12</a><br><a href="https://github.com/madler/zlib/issues/605">https://github.com/madler/zlib/issues/605</a><br><a href="https://github.com/sparklemotion/nokogiri/releases/tag/v1.13.4">https://github.com/sparklemotion/nokogiri/releases/tag/v1.13.4</a><br><a href="https://github.com/sparklemotion/nokogiri/security/advisories/GHSA-v6gp-9mmm-c6p5">https://github.com/sparklemotion/nokogiri/security/advisories/GHSA-v6gp-9mmm-c6p5</a><br><a href="https://groups.google.com/g/ruby-security-ann/c/vX7qSjsvWis/m/TJWN4oOKBwAJ">https://groups.google.com/g/ruby-security-ann/c/vX7qSjsvWis/m/TJWN4oOKBwAJ</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html">https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/NS2D2GFPFGOJUL4WQ3DUAY7HF4VWQ77F/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/NS2D2GFPFGOJUL4WQ3DUAY7HF4VWQ77F/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2018-25032">https://nvd.nist.gov/vuln/detail/CVE-2018-25032</a><br><a href="https://ubuntu.com/security/notices/USN-5355-1">https://ubuntu.com/security/notices/USN-5355-1</a><br><a href="https://ubuntu.com/security/notices/USN-5355-2">https://ubuntu.com/security/notices/USN-5355-2</a><br><a href="https://ubuntu.com/security/notices/USN-5359-1">https://ubuntu.com/security/notices/USN-5359-1</a><br><a href="https://www.debian.org/security/2022/dsa-5111">https://www.debian.org/security/2022/dsa-5111</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/24/1">https://www.openwall.com/lists/oss-security/2022/03/24/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/1">https://www.openwall.com/lists/oss-security/2022/03/28/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/3">https://www.openwall.com/lists/oss-security/2022/03/28/3</a><br></details>  |


#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| busybox         |    CVE-2022-28391   |   CRITICAL  |  1.34.1-r4 | 1.34.1-r5 | <details><summary>Expand...</summary><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch</a><br><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch</a><br><a href="https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661">https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-28391">https://nvd.nist.gov/vuln/detail/CVE-2022-28391</a><br></details>  |
| ssl_client         |    CVE-2022-28391   |   CRITICAL  |  1.34.1-r4 | 1.34.1-r5 | <details><summary>Expand...</summary><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0001-libbb-sockaddr2str-ensure-only-printable-characters-.patch</a><br><a href="https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch">https://git.alpinelinux.org/aports/plain/main/busybox/0002-nslookup-sanitize-all-printed-strings-with-printable.patch</a><br><a href="https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661">https://gitlab.alpinelinux.org/alpine/aports/-/issues/13661</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-28391">https://nvd.nist.gov/vuln/detail/CVE-2022-28391</a><br></details>  |
| zlib         |    CVE-2018-25032   |   HIGH  |  1.2.11-r3 | 1.2.12-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/03/25/2">http://www.openwall.com/lists/oss-security/2022/03/25/2</a><br><a href="http://www.openwall.com/lists/oss-security/2022/03/26/1">http://www.openwall.com/lists/oss-security/2022/03/26/1</a><br><a href="https://access.redhat.com/security/cve/CVE-2018-25032">https://access.redhat.com/security/cve/CVE-2018-25032</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032</a><br><a href="https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531">https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531</a><br><a href="https://github.com/madler/zlib/compare/v1.2.11...v1.2.12">https://github.com/madler/zlib/compare/v1.2.11...v1.2.12</a><br><a href="https://github.com/madler/zlib/issues/605">https://github.com/madler/zlib/issues/605</a><br><a href="https://github.com/sparklemotion/nokogiri/releases/tag/v1.13.4">https://github.com/sparklemotion/nokogiri/releases/tag/v1.13.4</a><br><a href="https://github.com/sparklemotion/nokogiri/security/advisories/GHSA-v6gp-9mmm-c6p5">https://github.com/sparklemotion/nokogiri/security/advisories/GHSA-v6gp-9mmm-c6p5</a><br><a href="https://groups.google.com/g/ruby-security-ann/c/vX7qSjsvWis/m/TJWN4oOKBwAJ">https://groups.google.com/g/ruby-security-ann/c/vX7qSjsvWis/m/TJWN4oOKBwAJ</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html">https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/NS2D2GFPFGOJUL4WQ3DUAY7HF4VWQ77F/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/NS2D2GFPFGOJUL4WQ3DUAY7HF4VWQ77F/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2018-25032">https://nvd.nist.gov/vuln/detail/CVE-2018-25032</a><br><a href="https://ubuntu.com/security/notices/USN-5355-1">https://ubuntu.com/security/notices/USN-5355-1</a><br><a href="https://ubuntu.com/security/notices/USN-5355-2">https://ubuntu.com/security/notices/USN-5355-2</a><br><a href="https://ubuntu.com/security/notices/USN-5359-1">https://ubuntu.com/security/notices/USN-5359-1</a><br><a href="https://www.debian.org/security/2022/dsa-5111">https://www.debian.org/security/2022/dsa-5111</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/24/1">https://www.openwall.com/lists/oss-security/2022/03/24/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/1">https://www.openwall.com/lists/oss-security/2022/03/28/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/3">https://www.openwall.com/lists/oss-security/2022/03/28/3</a><br></details>  |


#### Container: tccr.io/truecharts/docker-in-docker:v20.10.14@sha256:7ba99af4bdbea6b6cb39c8df207c43d72b53cb5eac6c4ac29e0dfe40ed368e3b (alpine 3.15.4)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| xz         |    CVE-2022-1271   |   HIGH  |  5.2.5-r0 | 5.2.5-r1 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-1271">https://access.redhat.com/security/cve/CVE-2022-1271</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-1271">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-1271</a><br><a href="https://lists.gnu.org/r/bug-gzip/2022-04/msg00011.html">https://lists.gnu.org/r/bug-gzip/2022-04/msg00011.html</a><br><a href="https://ubuntu.com/security/notices/USN-5378-1">https://ubuntu.com/security/notices/USN-5378-1</a><br><a href="https://ubuntu.com/security/notices/USN-5378-2">https://ubuntu.com/security/notices/USN-5378-2</a><br><a href="https://ubuntu.com/security/notices/USN-5378-3">https://ubuntu.com/security/notices/USN-5378-3</a><br><a href="https://ubuntu.com/security/notices/USN-5378-4">https://ubuntu.com/security/notices/USN-5378-4</a><br><a href="https://www.openwall.com/lists/oss-security/2022/04/07/8">https://www.openwall.com/lists/oss-security/2022/04/07/8</a><br></details>  |
| xz-libs         |    CVE-2022-1271   |   HIGH  |  5.2.5-r0 | 5.2.5-r1 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-1271">https://access.redhat.com/security/cve/CVE-2022-1271</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-1271">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-1271</a><br><a href="https://lists.gnu.org/r/bug-gzip/2022-04/msg00011.html">https://lists.gnu.org/r/bug-gzip/2022-04/msg00011.html</a><br><a href="https://ubuntu.com/security/notices/USN-5378-1">https://ubuntu.com/security/notices/USN-5378-1</a><br><a href="https://ubuntu.com/security/notices/USN-5378-2">https://ubuntu.com/security/notices/USN-5378-2</a><br><a href="https://ubuntu.com/security/notices/USN-5378-3">https://ubuntu.com/security/notices/USN-5378-3</a><br><a href="https://ubuntu.com/security/notices/USN-5378-4">https://ubuntu.com/security/notices/USN-5378-4</a><br><a href="https://www.openwall.com/lists/oss-security/2022/04/07/8">https://www.openwall.com/lists/oss-security/2022/04/07/8</a><br></details>  |