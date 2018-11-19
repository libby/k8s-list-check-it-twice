## :santa: K8s Checking It Twice :santa:

Top X lists of misconfigurations and vulnerablities relating to Kubernetes, as well
as aggregating more in depth resources, blogs, etc. from around The Internet.
**warning** - :alien: this documentent is alive and is subject to change.

## [First Twitter Responders](https://twitter.com/viskobatz/status/1064554599409958914)
*  @jpetazzo, @jessfraz, @raesene, @jbeda, @tallclair, @anapsix, @bradgeesaman

## Helpful Resources
* [kubesec.io](https://kubesec.io/)
* [Maya Kaczorowski - googleNext18 security journey slide](https://twitter.com/MattiasGees/status/1050355323318542336) 
* [Top 9 Kubernetes Setting You Should Check To Optimize Security](https://containerjournal.com/2018/07/03/top-9-kubernetes-settings-you-should-check-to-optimize-security/)
* [CIS Center For Internet Security](https://www.cisecurity.org/benchmark/kubernetes/)
* [Hardening Linux Containers - NCC Group Whitepaper](https://www.nccgroup.trust/us/our-research/understanding-and-hardening-linux-containers/)



## K8s Native List
 0. Stay up to date with upstream Kubernetes, try not to fall more than 3 months behind.
 1. Exposed Dashboard :fearful: 
    * :smiley: disable it
    * [On Securing the Kubernetes Dashboard - Joe Beda](https://blog.heptio.com/on-securing-the-kubernetes-dashboard-16b09b1b7aca?gi=8e23ff250468)
 2. CAdvisor: insecure port
 3. Misconfigured RBAC (vague, build out examples and links)
 4. Allowing anon access `--anonymous-auth` allows for compromising cluster with the service token access
    * [Kubernetes Attack Surface @raesene](https://raesene.github.io/blog/2017/04/02/Kubernetes-Service-Tokens/) 
 5. Unauthenticated kubelet
 6. Unauthenticate etcd
 7. Mounts the docker socket, e.g. docker in docker 
 8. Your Pod is too strong :fearful:
     * [Lock down your ``podSecurityPolicy` @tallclair](https://gist.githubusercontent.com/tallclair/11981031b6bfa829bb1fb9dcb7e026b0/raw/d302781b5eb773ea514341723c42fb7054b5bf96/restricted-psp.yaml)
     * AppArmor to lock down capabilities.
        * [Containers, Security, and Echo Chambers @jessfraz](https://blog.jessfraz.com/post/containers-security-and-echo-chambers/)
 9. Pods with containers running applications as "root"
10. Unencrypted etcd at rest
11. Not Protecting The Instance metadata in cloud providers like AWS and GCP

## K8's Friends Issues List
* [Exploring The Security Of Helm bitnami (Tiller is too strong)](https://engineering.bitnami.com/articles/helm-security.html)


## Attacks Against K8
* [Tesla Cloud Resources Are Hacked To Run Cyprtocurrenty-Mining Malware](https://arstechnica.com/information-technology/2018/02/tesla-cloud-resources-are-hacked-to-run-cryptocurrency-mining-malware/)
