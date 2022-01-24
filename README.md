# Azure Basic

> [Microsoft Azure 설명서](https://github.com/MicrosoftDocs/azure-docs.ko-kr)

- 3-tier 기반의 Sample 을 Azure Cloud 에 구성하는 과정을 통해 익숙해지는 것을 목표로 함

## AS-IS
- Apache, Tomcat, MySQL/MariaDB 로 이루어진 서비스
- Apache : Static 문서 처리
- Tomcat : SpringBoot 기반 Biz 서비스 처리

## 일정
| 월 | 화 | 수 | 목 | 금 |
|:---:|:---:|:---:|:---:|:---:|
| |  | | 2022.01.27</br> [Azure1](./0.ENV/Azure1.md) </br> [Azure2](./0.ENV/Azure2.md) | |
| | [2022.02.08](./1.IaaS/2022-02-08.md) | | [2022.02.10](./1.IaaS/2022-02-10.md) | |
| [2022-02-14](./1.IaaS/2022-02-14.md) | [2022-02-15](./1.IaaS/2022-02-15.md) | | | [2022-02-18](./1.IaaS/2022-02-18.md) |  
| [2022-02-21](./2.AKS/2022-02-21.md) | [2022-02-22](./2.AKS/2022-02-22.md) | | | [2022-02-25](./2.AKS/2022-02-25.md) | 
| | | [2022-03-03](./2.AKS/2022-03-03.md) | [2022-03-04](./3.LandingZone/2022-03-04.md) |

## 과정 내용
### 공통
|| 항목 | 날짜 | 내용 | 
|:---|:---|:---|:---|  
| Azure1 | 아키텍처 구성을 위한 기본 | 2022.01.25 | 3-tier 구성의 웹 전환을 대상으로 할 때 Azure 구독 획득 후 해야 할 일에 대한 설명 </br> 구독, RBAC, 자원그룹, VNet, subnet, VM, disk, Storage Account, PaaS, SaaS 구성 및 배포 방법 </br>  - Naming Rule 및 필수 Label 포함 </br> 아키텍처 작성, Azure 계산기 를 사용하여 비용 산출하기 </br> - Network 설계서 및 Infra Hybrid Cloud 자료 참조 |  
| Azure2 | 배포 실습을 위한 공통 환경/도구 구성 | 2022.01.27 | azure portal, azure cli, visual studio code, powershell, git cli, github, md, devops 환경 구성 </br>
- 간단한 md/git 사용법 </br>
- PowerShell 에서 배포 및 삭제 |  

### IaaS
|| 항목 | 날짜 | 내용 | 
|:---|:---|:---|:---|  
| Azure3 | 3-tier 기본 환경 구성 | 2022.02.08 | Vnet, subnet, NSG, apache, tomcat, mysql 구성 </br> - VM, disk, Storage Account, Internal L4, VMSS, AppGateway 구성 |
| Azure4 | 3-tier 기본 환경 외부 접근 구성 | 2022.02.10 | 3-tier 기본 환경에 CDN 적용, Azure DNS 설정, AppGateway 구성 변경 </br> - Application Gateway 구성 </br> - Azure DNS 구성 </br> |
| Azure5 | CDN 적용을 통한 고도화 | 2022.02.14 | 3-tier 기본 환경에 CDN 적용, Azure DNS 설정, AppGateway 구성 변경 </br> - Storage Account Blob 배포 및 Storage Exploror/SAS 를 이용한 Static 문서 Upload </br> - Azure CDN 배포 및 구성 </br> - 정상 동작 테스트 </br> - apache 서버 삭제  | 
| Azure6 | Azure Cli 를 통한 자원 배포(IaC - 1) | 2022.02.15 | azure cli, powershell, ARMTemplate 사용한 배포 테스트 |    
| Azure7 | Azure DevOps 를 통한 자원 배포(IaC - 2) | 2022.02.18 | azure devops 에 저장소 설정 및 Pipeline 을 만들어 배포 하기 |  

### AKS
|| 항목 | 날짜 | 내용 | 
|:---|:---|:---|:---|  
| Azure8 | Docker/Kubernetes | 2022.02.21 | Container 란 ? </br> - 설치 및 간단한 Docker Image 만들기 </br> Kubernetes 란 ? </br> - Minikube 설치 및 사용 |
| Azure9 | Azure Kubernetes Service 구성 | 2022.02.22 | AKS Cluster 설계 및 생성, 로깅, 모니터링 하기 </br> - 3 tier 를 Pod 롤 배포하기 </br> - CDN, mysql(Managed, DaemonSet) 구성 </br> - Ingress Controller 구성 </br>- DNS 에 등록 외부에서 접근하기 |
| Azure10 | AutoScaler 구성 | 2022.02.25 | Pod, Node AutoScaler 구성 및 모니터링 하기 </br> - deployment </br> - Storage Class </br> - Prometheus/AlertManager, Grafana |
| Azure11 | Azure DevOps 를 통한 Pod 배포 | 2022.03.03 | Repos 구성, Pipeline 구성, Pod 배포 </br> - blue/green 배포 |  
| Azure12 | OSS 를 통한 Pod 배포 | 2022.03.03 | Gitea, Jenkins, Harbor, ArgoCD 를 통한 GitOps 구성 </br> - webhook, Jenkinsflies 구성/작성 </br> - blue/green 배포 |

### SKT 환경 고려 사항
|| 항목 | 날짜 | 내용 | 
|:---|:---|:---|:---|  
| Azure13 | SKT랜딩존 환경 고려사항 | 2022.03.04 | SKT랜딩존 환경 고려사항 |

## 공통 환경  
| 항목 | 날짜 | 내용 | 
|:---|:---|:---|  
| choco | 2022.01.25 | 윈도우 패키지 관리자 |  
| git | 2022.01.27 | 형상관리, 사용법 |  
| MarkDown | 2022.01.27 | Markdown Language, Github 사용(README.md), 표준 문서 포맷, 사용법 |  
| Visual Studio Code | 2022.01.27 | 편집기 |  
| az cli | 2022.01.27 | azure client |  
| PowerShell | 2022.01.27 | 배포 삭제 |  
| java | 2022.01.27 |  https://jdk.java.net/17/ |

---

## Azure IaaS + PaaS(MySQL)  
| 항목 | 날짜 | 내용 |  
|:---|:---|:---|  
| Apache | 2022.02.08 | 웹서버 구성 확인 |
| Tomcat | 2022.02.08 | WAS 서버 구성 확인 | 
| MariaDB | 2022.02.08 | DB 구성 확인 | 

| 항목 | 날짜 | 내용 |
|:---|:---|:---| 
| resource group | 2022.02.08 | 자원 그룹 | 
| VNet | 2022.02.08 | 구독당 하나의 VNet 구성 | 
| subnet | 2022.02.08 | DMZ, frontend, backend 로 구분 생성 | 
| vm | 2022.02.08 | WEB, WAS VM 으로 생성 | 
| MariaDB/MySQL | 2022.02.08 | PaaS(Managed DB) 형태로 생성 |  
| Azure App Service 도메인 | 2022.02.10 | Domain 생성/관리 |   
| Azure DNS | 2022.02.10 | Azure 인프라를 사용하여 이름 확인을 제공하는 DNS 도메인에 대한 호스팅 서비스 |  
| Application Gateway | 2022.02.10 | 웹 애플리케이션에 대한 트래픽을 관리할 수 있도록 하는 웹 트래픽 부하 분산 장치 | 
| CDN | 2022.02.10 | CDN(콘텐츠 배달 네트워크)은 사용자에게 웹 콘텐츠를 효율적으로 제공할 수 있는 서버의 분산 네트워크 |  

---

## Azure CaaS(AKS) + PaaS(MySQL)  
| 과정 | 날짜 | 내용 |
|:---|:---|:---|  
| Docker | 2022.02.21 | Container |
| Kubernetes | 2022.02.21 | Container as a Service, 아키텍처 | 
| AKS | 2022.02.22 ~ 23 | Azure Kubernetes Service | 
| DevOps | 2022.03.03 | OSS 기반, Azure DevOps 기반 |  
| Landing Zone | 2022.03.04 | Azure Landing Zone 요소 설명 | 

---
