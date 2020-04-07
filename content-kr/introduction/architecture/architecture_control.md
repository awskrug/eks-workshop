---
title: "콘트롤 플레인"
date: 2018-10-03T10:18:27-07:00
draft: false
weight: 100
---

{{<mermaid>}}
graph TB
kubectl{kubectl}
  subgraph ControlPlane
    api(API Server)
    controller(Controller Manager)
    scheduler(Scheduler)
    etcd(etcd)
  end

  kubectl-->api
  controller-->api
  scheduler-->api
  api-->kubelet
  api-->etcd

  classDef green fill:#9f6,stroke:#333,stroke-width:4px;
  classDef orange fill:#f96,stroke:#333,stroke-width:4px;
  classDef blue fill:#6495ed,stroke:#333,stroke-width:4px;
  class api blue;
  class internet green;
  class kubectl orange;
{{< /mermaid >}}

* 1개 이상의 API 서버: kubectl 의 REST 진입점

* etcd: 분산 키/벨류 저장소

* 콘트롤 매니저: 항상 현재 상태와 원하는 상태를 평가

* 스케줄러: 작업 노드에 파드를 스케줄링

[쿠버네티스 공식 문서](https://kubernetes.io/docs/concepts/overview/components/#master-components)에서 콘트롤 플레인에 대해 더 깊이 있는 설명을 확인할 수 있습니다.
