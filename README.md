你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# OpenEBS

[![Build Status](https://img.shields.io/travis/openebs/openebs/master.svg?style=flat-square)](https://travis-ci.org/openebs/jiva)
[![Docker Pulls](https://img.shields.io/docker/pulls/openebs/jiva.svg?style=flat-square)](https://hub.docker.com/r/openebs/jiva/)
[![Releases](https://img.shields.io/github/release/openebs/openebs/all.svg?style=flat-square)](https://github.com/openebs/openebs/releases)
[![Slack](https://img.shields.io/badge/chat!!!-slack-ff1493.svg?style=flat-square)]( https://openebsslacksignup.herokuapp.com/)
[![Twitter](https://img.shields.io/twitter/follow/openebs.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=openebs)

http://www.openebs.io/
 
**OpenEBS** enables the use of containers for mission-critical, persistent workloads. OpenEBS is containerized storage and related storage services.
 
**OpenEBS** allows you to treat your persistent workload containers, such as DBs on containers, just like other containers. OpenEBS itself is deployed as just another container on your host and enables storage services that can be designated on a per pod, application, cluster or container level, including:
- Data persistence across nodes, dramatically reducing time spent rebuilding Cassandra rings for example.
- Synchronization of data across availability zones and cloud providers.
- Use of commodity hardware plus a container engine to deliver so called container attached block storage.
- Integration with Kubernetes, so  developer and application intent flows into OpenEBS configurations automatically.
- Management of tiering to and from S3 and other targets.
  
**Our vision** is simple: let storage and storage services for persistent workloads be fully integrated into the environment and hence can be managed automatically that it almost disappears into the background as just yet another infrastructure service that just works. 

## Why OpenEBS Scales
 
OpenEBS can scale to include an arbitrarily large number of containerized storage controllers. Thanks in part to some advancements in the metadata management which remove a common bottleneck to scaling out storage performance. 

## Installation and Getting Started
 
OpenEBS can be setup in few easy steps. You can get going on your choice of Kubernetes cluster by having open-iscsi installed on the Kubernetes nodes and running the openebs-operator using kubectl. 

**Start the OpenEBS Services using operator**
```bash
# apply this yaml
kubectl apply -f https://openebs.github.io/charts/openebs-operator.yaml
```

**Apply OpenEBS StorageClasses**
```bash
# apply this yaml
kubectl apply -f https://openebs.github.io/charts/openebs-storageclasses.yaml
```

You could also follow our [QuickStart Guide](https://docs.openebs.io/docs/overview.html).

OpenEBS can be deployed on any Kubernetes cluster - either in cloud, on-premise or developer laptop (minikube). Please follow our [OpenEBS Setup](https://docs.openebs.io/docs/overview.html) documentation. Also, we have a Vagrant environment available that includes a sample Kubernetes deployment and synthetic load that you can use to simulate the performance of OpenEBS. You may also find interesting the related project called Litmus (https://www.openebs.io/litmus) which helps with chaos engineering for stateful workloads on Kubernetes.

## Status
We are approaching beta stage with active development underway. See our [Project Tracker](https://github.com/openebs/openebs/wiki/Project-Tracker) for more details.  Please note that as of June 2018 we have cStor which is about to be released for additional funcitons and somewhat improved performance; please contact us on Slack if you are interested in this engine.
 
## Contributing
 
OpenEBS welcomes your feedback and contributions in any form possible.
 
- Join us at [Slack](https://openebsslacksignup.herokuapp.com/)
  - Already signed up? Head to our discussions at [#openebs-users](https://openebs-community.slack.com/messages/openebs-users/)
- Want to raise an issue?
  - If it is a generic (or `not really sure`), you can still raise it at [issues](https://github.com/openebs/openebs/issues)
  - Project (repository) specific issues also can be raised at [issues](https://github.com/openebs/openebs/issues) and tagged with the individual repository labels like *repo/maya*.
- Want to help with fixes and features?
  - See [open issues](https://github.com/openebs/openebs/labels)
  - See [contributing guide](./CONTRIBUTING.md)
  - Want to join our community, [check this out](./community/README.md). 

## Show me the Code

This is a meta-repository for OpenEBS. The source code is available at the following locations:
- The source code for the initial storage engine is under [openebs/jiva](https://github.com/openebs/jiva).
- The storage orchestration source code is under [openebs/maya](https://github.com/openebs/maya).
- While *jiva* and *maya* contain significant chunks of source code, some of the orchestration and automation code is also distributed in other repositories under the OpenEBS organization. 

Please start with the pinned repositories or with [OpenEBS Architecture](./contribute/design/README.md) document. 


## License

OpenEBS is developed under Apache 2.0 license at the project level. 
Some components of the project are derived from other open source projects like Nomad, Longhorn and are distributed under their respective licenses. 
