# examples

This folder contains some examples showing the usage of the Golang
packages provided by Inspektor Gadget. These examples are designed for
developers that want to use the Golang packages exposed by Inspektor
Gadget directly. End-users do not need this and can use `kubectl-gadget`
or `ig` directly.

- [container-hook](container-hook/): Use of the container-hook package to
  - receive notifications when a container starts or terminates
  - execute PreStart and PostStop hooks
- [container-collection](container-collection/): Use the
  container-collection package
  ("github.com/inspektor-gadget/inspektor-gadget/pkg/container-collection") to
  print a message when a container is created or removed.
- [kube-container-collection](kube-container-collection/): Use the
  container-collection package
  ("github.com/inspektor-gadget/inspektor-gadget/pkg/container-collection") in
  order to be notified when a new container is started and to attach the
  OCI config.json as a Kubernetes event.
- (image-based) gadgets:
  - Check list of examples in [gadgets](gadgets)
- built-in gadgets:
  - [basic](builtin-gadgets/basic/): Examples showing how to create a tracer
    without any filtering capabilities.
    - [trace/dns](builtin-gadgets/basic/trace/dns/): shows how to use
      [trace/dns](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/pkg/gadgets/trace/dns)
      package to trace DNS requests in the host.
    - [trace/exec](builtin-gadgets/basic/trace/exec/): shows how to use
      [trace/exec](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/pkg/gadgets/trace/exec)
      package to trace the creation of new processes in the host.
    - [top/file](builtin-gadgets/basic/top/file/): shows how to use
      [top/file](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/pkg/gadgets/top/file)
      package to get a list of the files with a higher number of write
      operations on the host.
    - [snapshot/basic/process](builtin-gadgets/basic/snapshot/process/): shows how to use
      [snapshot/process](https://github.com/inspektor-gadget/inspektor-gadget/tree/main/pkg/gadgets/snapshot/process)
      package to get a list the running processes on the host.
  - [withfilter](builtin-gadgets/withfilter/): Examples showing how to create a
    tracer that uses the container collection and trace collection
    packages to filter events by container.
    - [trace/exec](builtin-gadgets/withfilter/trace/exec/): traces creation of
      new processes inside a particular container.
    - [trace/network](builtin-gadgets/withfilter/trace/network): traces network
      connections inside containers.
  - [formatter](builtin-gadgets/formatter/): Examples showing how to use a formatter to
    print events in a column format.
    - [trace/exec](builtin-gadgets/formatter/trace/exec/): traces creation of
      new processes inside a particular container.
