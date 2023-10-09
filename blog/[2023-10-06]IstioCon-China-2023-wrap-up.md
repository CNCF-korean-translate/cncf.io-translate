---
title: IstioCon China 2023 마무리
origin: https://www.cncf.io/blog/2023/10/06/istiocon-china-2023-wrap-up/
published: 2023-10-06
category: project post
---

*[Istio 블로그](https://istio.io/latest/blog/2023/istiocon-china/) 에 게시된 프로젝트 게시물*

상하이에서 열린 Istio at KubeCon + CloudNativeCon + Open Source Summit China를 간략하게 요약했습니다.

안전한 상황에서 다시 모일 수 있게되어 기쁩니다. 2년간 온라인 이벤트로만 2023년을 채웠습니다. 4월에 [Istio Day Europe](https://istio.io/latest/blog/2023/istio-at-kubecon-eu/)가 열렸고, 11월에는 [Istio Day North America](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/co-located-events/istio-day/)가 열립니다.

IstioCon은 실제 Istio 배포에서 얻은 인사이트를 탐구하고, 핸즈온을 통한 상호작용에 참여하며 전체 Istio 생태계의 메인테이너와 연결할 수 있는 플랫폼을 제공하는 업계 최고의 서비스 메시에 전념하고 있습니다.

[virtual IstioCon 2023](https://events.istio.io/) 이벤트와 함께 [IstioCon China 2023](https://www.lfasiallc.com/kubecon-cloudnativecon-open-source-summit-china/co-located-events/istiocon-cn/)이 9월 26일 중국 상하이에서 열렸습니다. KubeCon + CloudNativeCon + Open Source Summit China의 일부인 이 이벤트는 Istio 메인테이너들과 CNCF가 주최했습니다. 우리는 상하이에서 IstioCon을 위한 강력한 프로그램을 갖게 된 것을 매우 자랑스럽게 생각하며 중국 Istio 커뮤니티 구성원을 한자리에 모을 수 있게 되어 기뻤습니다. 이번 행사는 아시아 태평양 생태계에서 Istio의 엄청난 인기를 입증하는 것이었습니다.

![IstioCon 중국 2023](https://www.cncf.io/wp-content/uploads/2023/10/image-3-1800x1201.jpeg)

IstioCon China는 프로그램 위원회 위원인 Jimmy Song과 Zhonghu Xu의 기조연설로 시작되었습니다. 이 이벤트는 새로운 Istio ambient mesh에 중점을 두고 새로운 기능부터 end user talk까지 훌륭한 콘텐츠로 가득 차 있었습니다.

![IstioCon 중국 2023, 환영합니다](https://www.cncf.io/wp-content/uploads/2023/10/image-4-1800x1201.jpeg)

환영 연설에 이어 구글의 Justin Pettit가 스폰서 키노트로 "관리형 인프라스트럭처로서의 Istio Ambient Mesh"가 이어졌고, 이 키노트에서는 Istio 커뮤니티, 특히 Google Cloud와 같은 top supporters에게 ambient model의 중요성과 우선순위를 강조했습니다.

![IstioCon China 2023, Google Cloud 후원 기조연설](https://www.cncf.io/wp-content/uploads/2023/10/image-6.png)

키노트 이후 완벽하게 배치된 Intel의 Huailong Zhang과 Alibaba의 Yuxing Zeng은 Ambient와 Sidecar의 공존을 위한 구성에 대해 논의했습니다. 새로운 ambient model을 실험하려는 기존 사용자에게 매우 관련된 주제입니다.

![IstioCon China 2023, Ambient와 Sidecar의 공존을 위한 Istio 네트워크 흐름 및 구성에 대한 심층 분석](https://www.cncf.io/wp-content/uploads/2023/10/image-5-1800x1201.jpeg)

eBPF를 기반으로 하는 Huawei의 새로운 Istio data plane은 커널에서 L4 및 L7의 기능을 구현하여 kernel-state 및 user-mode 스위칭을 방지하고 data plane의 대기 시간을 줄이려는 의도를 가지고 있습니다. 이는 Xie SongYang과 Zhonghu Xu의 흥미로운 강연을 통해 설명되었습니다. Intel의 Chun Li와 Iris Ding도 "Istio ambient mode의 Traffic Redirection을 위한 eBPF 활용"이라는 강연을 통해 eBPF를 Istio와 통합하여 더욱 흥미로운 토론을 이끌었습니다. DaoCloud도 행사에 참석하여 Kebe Liu가 Merbridge의 eBPF 혁신을 공유하고 Xiaopeng Han이 현지화된 Istio 개발을 위한 MirageDebug에 대해 발표했습니다.

![](https://www.cncf.io/wp-content/uploads/2023/10/image-6-1800x1201.jpeg)

Tetrate의 Jimmy Song의 다양한 GitOps와 Observability 도구의 완벽한 결합에 대한 강연도 매우 호평을 받았습니다. Huawei의 Chaomeng Zhang은 cert-manager가 Istio 인증서 관리 시스템의 보안과 유연성을 향상시키는 데 어떻게 도움이 되는지 설명했고, Alibaba Cloud의 Xi Ning Wang과 Zehuan Shi는 VK(Virtual Kubelet)를 사용하여 serverless mesh를 구현하는 아이디어를 공유했습니다.

Shivanshu Raj Shrivastava가 "Wasm으로 Istio 확장 및 커스터마이징" 이라는 강연을 통해 WebAssembly를 완벽하게 소개했고, 인도네시아 GoTo Financial의 Zufar Dhiyaulhaq는 Coraza Proxy Wasm을 사용하여 Envoy를 확장하고 커스텀 웹 애플리케이션 방화벽을 신속하게 구현하는 방법을 공유했습니다. Tetrate의 Huabing Zhao는 Boss Direct의 Qin Shilin과 Aeraki Mesh의 Dubbo 서비스 거버넌스 방식을 공유했습니다. multi-tenancy가 Istio에서 항상 화제가 되고 있지만, HP의 John Zheng은 HP OneCloud Platform의 multi-tenant 관리에 대해 자세히 설명했습니다.

모든 세션의 슬라이드는 [IstioCon China 2023 일정](https://istioconchina2023.sched.com/)에서 확인할 수 있으며, 모든 프레젠테이션은 곧 CNCF YouTube 채널을 통해 전 세계 다른 지역의 청중에게도 공개될 예정입니다.

# 쇼 플로어에서

Istio는 KubeCon + CloudNativeCon + Open Source Summit China 2023 프로젝트 파빌리온에서 풀타임 키오스크를 운영했으며, 대부분의 질문은 ambient mesh에 관한 질문이었습니다. 많은 회원들과 메인테이너들이 부스에서 지원을 제공하여 흥미로운 토론이 이루어졌습니다.

![KubeCon + CloudNativeCon + Open Source Summit China 2023, Istio Kiosk](https://www.cncf.io/wp-content/uploads/2023/10/image-7-1800x1200.jpeg)

또 다른 하이라이트는 Istio 운영 위원회 회원이자 Istio 책 "Cloud Native Service Mesh Istio" 및 "Istio: the Definitive Guide"의 저자인 Zhonghu Xu와 Chaomeng Zhang이 Istio 부스에서 사용자 및 컨트리뷰터들과 소통하는 시간을 보낸 것입니다.

![저자를 만나보세요](https://www.cncf.io/wp-content/uploads/2023/10/image-8.jpeg)

IstioCon 2023을 지원해주신 다이아몬드 스폰서인 Google Cloud에 진심으로 감사드립니다!

![IstioCon 2023, 다이아몬드 스폰서](https://www.cncf.io/wp-content/uploads/2023/10/image-7.png)

마지막으로, IstioCon China Program 위원회 회원들의 노고와 지원에 감사드립니다!

![IstioCon China 2023, 프로그램 위원회 위원(사진 없음: Iris Ding)](https://www.cncf.io/wp-content/uploads/2023/10/image-9-1800x1200.jpeg)

[11월에 시카고에서 만나요!](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/co-located-events/istio-day/)
