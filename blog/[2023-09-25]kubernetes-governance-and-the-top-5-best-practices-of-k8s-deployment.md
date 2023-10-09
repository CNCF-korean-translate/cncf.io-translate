---
title: 쿠버네티스의 거버넌스 & K8s 배포 모범 사례 5가지
origin: https://www.cncf.io/blog/2023/09/25/kubernetes-governance-the-top-5-best-practices-of-k8s-deployment/
published: 2023-09-25
author: Joe Pelletier
category: member post
---

*Joe Pelletier의 [Fairwinds 블로그](https://www.fairwinds.com/blog/kubernetes-governance-the-top-5-best-practices-of-k8s-deployment)에 게시된 회원 게시물*

컨테이너화된 애플리케이션은 조직이 소프트웨어 인프라 스트럭처를 개발, 배포 및 관리하는 방식을 근본적으로 변화시켰습니다. 쿠버네티스는 컨테이너화된 워크로드와 서비스를 규모에 맞게 관리할 수 있도록 만들어주어 이러한 변화에 근간이 되는 역할을 합니다. 그 중요한 운영의 기반 요소 중 하나인 쿠버네티스의 거버넌스는, 쿠버네티스가 어떻게 설정, 관리 및 보안되는지를 규정하는 정책과 절차입니다.

쿠버네티스 거버넌스가 없으면, 플랫폼 팀은 새로운 애플리케이션과 팀을 도입하는 데 어려움을 겪게 됩니다. 거버넌스는 일관성, 예측성, 반복성을 제공하여 플랫폼 팀이 프로덕션을 위한 "잘 닦여진 길(paved roads)"를 구축하여 엔지니어링 팀이 클라우드 네이티브 인프라를 사용하여 애플리케이션을 더 자주 배포할 수 있도록 하는 핵심 지표인 DevOps Research and Assessment 팀(DORA)에 중요한 역할을 합니다.

# 쿠버네티스 거버넌스란 무엇인가요?

[쿠버네티스 거버넌스](https://www.fairwinds.com/blog/what-is-kubernetes-governance)는 쿠버네티스 환경에서의 작동 규칙을 규정하여 쿠버네티스 클러스터를 조정하고 관리할 수 있도록 보장합니다. 이것은 쿠버네티스 리소스, [역할 기반(role-based) 접근 제어](https://kubernetes.io/docs/concepts/security/rbac-good-practices/), 스케줄링 및 업그레이드의 관리를 포함합니다. 거버넌스에는 쿠버네티스와 관련된 의사결정을 하는 프로세스도 포함되어 있습니다. 이는 기능 요청, 보안 문제 및 버그 수정의 관리 방법을 포함합니다. 쿠버네티스는 개발, 운영 및 보안 팀에 대한 다양한 복잡성과 새로운 기술을 도입하기 때문에 거버넌스가 필요합니다. 거버넌스가 없으면 다음과 같은 문제가 발생할 수 있습니다:

- 쿠버네티스 클러스터 활동 및 성장에 대한 충분한 가시성 부족
- 조직 전체에서 여러 소프트웨어 버전을 관리하는 어려움
- 여러 팀 및 환경에서 사용자 역할, 책임 및 권한을 추적하는 문제
- 역할 위반을 식별하고 지배 위험을 평가하며 규정 준수 확인을 위한 상당한 시간이 소요
- 팀 간에 정책 및 절차를 강제하는 문제

쿠버네티스 거버넌스 이니셔티브는 쿠버네티스가 조직의 정책 요구 사항을 준수하고 모범 사례를 준수하며 관련 규정 요구 사항을 충족하도록 보장합니다.

# 쿠버네티스 배포의 모범 사례

쿠버네티스 구현의 이득을 극대화하려면 다음의 5가지 모범 사례를 따르세요:

1. 보안 [구성](https://www.fairwinds.com/blog/kubernetes-misconfigurations)
    
    보안 팀에 의해 이상적으로 자동화 및 견고한 정책을 통해 설정되고 강제화되어야 합니다.
    
2. [비용 최적화](https://www.fairwinds.com/blog/6-kubernetes-cost-control-strategies-you-need-for-2023)
    
    워크로드의 리소스 요청과 제한을 설정하여 인프라 활용도를 극대화하면서 최적의 애플리케이션 성능을 보장해야 합니다.
    
3. [신뢰성](https://www.fairwinds.com/blog/you-can-establish-reliable-kubernetes-clusters-without-losing-sleep)
    
    워크로드가 [liveness probes](https://www.fairwinds.com/blog/a-guide-to-understanding-kubernetes-liveness-probes-best-practices) 및 [readiness probes](https://www.fairwinds.com/blog/increase-kubernetes-reliability-a-best-practices-guide-for-readiness-probes)로 구성되어 있는지 확인하고, [Infrastructure as Code](https://www.fairwinds.com/blog/why-infrastructure-as-code-kubernetes) (IaC)의 모범 사례를 따라야 합니다. IaC는 인프라가 감사 가능하고 일관성 있게 유지될 수 있도록 도와줍니다.
    
4. [정책 강화](https://www.fairwinds.com/blog/why-kubernetes-policy-enforcement)
    
    쿠버네티스 배포가 단일 애플리케이션을 초과하는 경우 정책 강화가 중요합니다. 도구와 자동화를 사용하여 일반적인 잘못된 구성을 방지하고 IT 규정 준수를 가능하게 할 수 있습니다. 이는 정책을 강제하기 위한 가드레일이 설정되어 있기 때문에 사용자들이 정책을 준수하면서 배포하는 데 안전하다고 느낄 수 있도록 장려할 수 있습니다. 클라우드 네이티브 환경을 위한 하나의 오픈 소스 도구로 [Open Policy Agent](https://www.openpolicyagent.org/) (OPA)가 있으며 이 도구는 정책 기반 제어를 제공합니다.
    
5. [모니터링](https://www.fairwinds.com/blog/building-a-kubernetes-platform-what-you-need-to-monitor-and-why) 및 경보
    
    쿠버네티스 같은 일시적인 환경에서 인프라와 애플리케이션이 실행되고 있는지 확인하는 것이 중요합니다. 모니터링을 최적화하기 위한 여러 도구가 있습니다.
    

# 쿠버네티스 거버넌스에 중요한 정책

## 클러스터 전체 정책

조직은 [클러스터 전체](https://insights.docs.fairwinds.com/first-steps/policy-enforcement/) 및 네임스페이스별 (또는 애플리케이션별) 정책을 배포할 수 있습니다. 보통 클러스터 전체 정책은 모든 워크로드에 적용되며 보안, 효율성 및 신뢰성과 관련이 있을 수 있습니다. 몇 가지 중요한 정책은 다음과 같습니다:

- 메모리 및 CPU 요청이 설정되어야 함
- liveness 및 readiness 프로브가 설정되어야 함
- [이미지 풀 정책](https://www.fairwinds.com/blog/kubernetes-basics-tutorial-how-to-set-image-pull-policy-to-always)은 "항상"으로 설정되어야 함
- 컨테이너에 [위험한 기능](https://www.fairwinds.com/blog/fairwinds-insights-basics-tutorial-avoid-containers-running-with-dangerous-capabilities)이 없어야 함

## 네임스페이스 정책

네임스페이스별 정책은 특정 애플리케이션 팀이나 서비스에 대한 표준을 강요할 때 적용됩니다. 보안, 효율성 또는 신뢰성의 높은 수준을 요구하는 경우에 사용할 수 있습니다. [네임스페이스](https://www.fairwinds.com/blog/kubernetes-governance-what-is-opa)를 사용하여 팀 내에서 일관성 없는 배포나 보안 위반과 같은 다른 클러스터 테넌트에 대한 방해를 피하도록하고, 리소스 고갈이나 보안 위반이 발생하지 않도록 하는 공통 모범 사례를 준수해야 합니다.

## 시행 지점

[정책을 시행](https://www.fairwinds.com/enforce-kubernetes-policy)하는 것은 여러 단계에서 발생할 수 있습니다. 쿠버네티스 거버넌스는 엔지니어들에게 필요한 시점에 사용하는 도구를 통해 피드백을 제공하여 정책을 시행합니다.

## 비용 할당

쿠버네티스 소비는 클러스터 수, 애플리케이션이 배포되는 위치 및 구성 방식에 비례하여 증가합니다. 플랫폼 엔지니어링 팀은 비즈니스 관련 맥락에서 [비용을 할당](https://www.fairwinds.com/blog/how-to-implement-finops-and-increase-your-kubernetes-cost-avoidance)하고 보여주기 위해 노력해야 합니다.

## 리소스 라벨링

비용을 쿠버네티스 구성요소에 할당하기 위해 네임스페이스 또는 라벨을 사용하는 것이 도움이 됩니다. 쿠버네티스 Vertical Pod Autoscaler (VPA)는 워크로드의 메모리 및 CPU 사용량을 과거 데이터와 현재 pod 사용량과 함께 사용하여 [리소스 요청 및 제한](https://www.fairwinds.com/blog/how-to-correctly-set-resource-requests-and-limits)에 대한 권장 사항을 생성합니다.

## 비용 절감 및 최적화

[비용 절감](https://www.fairwinds.com/blog/how-to-accelerate-your-kubernetes-cost-journey)은 사용량을 줄이고 비용을 최적화하여 더 나은 클라우드 요금을 얻는 것을 의미합니다. 플랫폼 엔지니어링 팀은 애플리케이션을 더 빨리 출시하고 클라우드 사용을 최적화하며 리스크를 줄여 비용 절감 및 최적화 목표를 달성할 수 있습니다.

## **Infrastructure as Code** 스캔

[IaC](https://www.fairwinds.com/blog/why-infrastructure-as-code-kubernetes)를 사용하면 구성 언어를 사용하여 인프라를 프로비저닝하고 관리하여 현대 소프트웨어 개발의 반복 가능성, 투명성 및 테스트를 적용할 수 있습니다. IaC는 오류와 [설정 드리프트](https://www.fairwinds.com/blog/configuration-drift-kubernetes)를 줄이고 엔지니어가 대규모 비즈니스 목표에 기여하는 작업에 중점을 둘 수 있도록 도와줍니다.

## 컨테이너 이미지 스캔

[베이스 이미지](https://www.fairwinds.com/blog/introducing-base-image-finder-an-open-source-tool-for-identifying-base-images)의 취약성은 해당 베이스 이미지를 포함하는 모든 컨테이너에 존재합니다. 프로덕션 배포에 필요하지 않은 이미지를 제거하고 권한을 제어하며 베이스 이미지에 대한 패치를 최신 상태로 유지하여 컨테이너 이미지의 보안을 강화할 수 있습니다.

## 사라진 API

쿠버네티스는 오래된 API를 유지 보수할 필요성을 최소화하고 더 안전하고 최신 버전을 사용하도록 조직을 격려하기 위해 API 버전을 폐기합니다. 응용 프로그램이나 서비스에 [사용되지 않거나 제거된 API 버전](https://www.fairwinds.com/blog/find-deprecated-and-removed-apis)이 포함되어 있는 경우 해당 API를 최신 안정 버전으로 찾아 업데이트해야 합니다.

## 애드온 업그레이드

[애드온](https://www.fairwinds.com/kube-clinic-installing-addons-reg)은 추가적인 쿠버네티스 기능을 제공합니다. 때로는 애드온이 업그레이드가 필요할 수 있지만 최신 버전이 클러스터와 호환되는지 확인하는 것이 중요합니다. 이 프로세스는 [애드온 변경을 자동으로 감지](https://www.fairwinds.com/blog/gonogo-checks-kubernetes-add-ons)하는 도구 없이는 느리고 어려울 수 있습니다.

## 정책 강화 및 가드레일

다수의 쿠버네티스 클러스터와 개발 팀으로 구성된 쿠버네티스 환경에서 [정의된 정책](https://www.fairwinds.com/enforce-kubernetes-policy)과 정책을 자동으로 시행하는 방법이 중요합니다. 이러한 가드레일은 프로덕션에서 무엇인가를 망가뜨리거나 데이터 누출을 허용하거나 적절하게 확장되지 않는 구성을 가능하게 하는 변경 사항을 배포하지 못하도록 방지합니다.

## 규정 준수 분석

대부분의 조직은 [SOC 2](https://www.fairwinds.com/kubernetes-compliance-soc2-paper-reg), [HIPAA](https://www.fairwinds.com/hubfs/Datasheets/Fairwinds_Insights_Healthcare_Datasheet.pdf), [ISO27001](https://www.fairwinds.com/blog/now-available-automated-compliance-evidence-collection-in-fairwinds-insights), [GDPR](https://www.fairwinds.com/blog/5-ways-cloud-native-guardrails-help-your-development-team-deliver), PIPEDA 및 기타 여러 보안 및 개인 정보 보호 규정을 준수해야 합니다. [정의된 쿠버네티스 규정 준수](https://www.fairwinds.com/kubernetes-compliance) 요구 사항 정책을 채택하고 모든 클러스터에서 이를 자동으로 시행하는 것은 규정 준수 목표를 달성하기 위해 중요하며, 변경된 요구 사항을 충족하고 있는지 평가하기 위해 규정 준수 분석을 자동화하는 것이 중요합니다.

# 쿠버네티스 거버넌스 구현

쿠버네티스 거버넌스는 클라우드 네이티브 컴퓨팅 전략과 일치하여 플랫폼 팀이 정책을 실행하고 강제하는 가드레일을 자동으로 적용할 수 있도록 합니다. 이러한 정책은 쿠버네티스를 신뢰성 있게, 안전하게 및 비용 효율적으로 실행하도록 도와줍니다. 이로써 귀하의 K8s 플랫폼 투자를 최대화할 수 있으며 조직의 정책 요구 사항을 충족하고 있는지 걱정하지 않아도 됩니다.
