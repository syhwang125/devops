# devops

# K-mooc DevOps 

#####################################################
1주차 – DevOps와 오픈소스 소프트웨어
#####################################################
1차시. DevOps 와 오픈소스 
환경의 변화 : 새로운 SW기반 서비스 등장 , 빠른 대응, 빠른 시도/실패를 통한 점진적 서비스 개선 변경, 검증, 반복, 개선 가능
DevOps 란 ? 기술과 시장의 빠른 변화에 대응하기 위한 최신 소프트웨어 개발/운영 트렌드 임
Development (개발) : 요구사항, 아키텍처, 설계/개발 
Quality Assurance (품질, 테스팅) : 정적분석, 리팩토링, 자동화테스트
Opeprations (운영) : 지속적 통합/전달/배포 
-> ※ DevOps 는 위의 3가지 요소의 교집합, 통합적 관점
---------------------------------------------------------------------
2차시. DevOps 공정 
DevOps 수명주기 
과거방식 : 계획 -> 개발 -> 빌드 ->테스트  (설치형, 패키지SW) 
           -> 릴리즈 -> 배포 -> 운영 -> 모니터링 (전산실, 데이터센터) 
DevOps 방식 : 개발x운영 반복 iteration  (최소 2주단위~1개월) 
DevOps 수명주기 : SaaS 기반 
          
DevOps 구간별 활동 - 애자일개발, 지속적 전달/배포, 지속적 서비스 개선
ㅇ 계획 - 서비스 개선을 계획하고 추적 
   ㄴ 변경 요구 검토 및 개선 작업 계획 수립
   ㄴ 우선 순위에 따른 요구사항 관리
   ㄴ 작업상황 가시화 및 추적
   ㄴ 스크럼, 칸반
ㅇ 개발 - SW를 설계하고 코드 작성 
   ㄴ 소스코드저장소를 통한 버전관리필수
   ㄴ 테스트자동화를 위한 테스트코드 작성
   ㄴ 소스코드인스펙션, 동료검토, 리팩토링 수행
   ㄴ SaaS 개발을 위한 필수 요건 반영 
ㅇ 빌드/테스트 - 실행가능한 SW산출물을 만들고 테스트하는 활동
   ㄴ 소스코드컴파일, 단위테스트, 패키징, 통합테스트
   ㄴ 통합된 최신코드 지속적 업데이트, 작은 단위로 수행
   ㄴ 완벽한 빌드 테스트 후 즉각적 변경 반영 
ㅇ 릴리즈/배포 - 언제나 배포 실행 가능한 상태를 유지하는 활동
   ㄴ 가장  큰 병목과 지연 발생 구간 
   ㄴ 운영환경준비 및 문제발생시 롤백(rollback) 대응
   ㄴ UI테스트,부하테스트,통합테스트 등 다양한 테스트 수행 
   ㄴ 지속적 전달의 경우 테스트 성공시 스테이징 환경까지 배포
   ㄴ 지속적 배포의 경우 자동 프로덕션 환경까지 배포
ㅇ 운영/모니터링 - 사용자에게 중단없는 서비스 제공
   ㄴ 장애,성능,보안,용량, 가용성관리   
---------------------------------------------------------------------
3차시. DevOps 사례 
ㅇ 스크럼활동 : 
   ㄴ jira 등 도구를 통해 백로그 아이템 관리 
   ㄴ 스프린트 수행 및 일감 추적 관리 (2주~1개월 반복활동)
   ㄴ 도메인 주도 설계 : 업무 중심의 SW설계 및 개발 
   ㄴ 이벤트 스토밍 : 전략적 설계를 통한 서비스 식별 
   ㄴ 전술적 설계 : 전략적 설계의 결과로 구체적인 클래스들을 식별하고 모델링하는 작업
       (소스코드 역공학 -> 설계/개발의 갭을 줄임)
   ㄴ SaaS 구현 패턴 : 단일한 코드를 기반으로 서비스 구현 
      개발환경(application-dev.yml), 스테이징(application-stage.yml), 프로덕션(application-prod.yml) 실행환경 
 
ㅇ 통합 DevOps 환경 서비스
  ㄴ Dashboard : platform을 구성하는 자원관리 (kubernetes 기반의 resource 관리) 
  ㄴ CI/CD pipeline : platform기반의 자동화된 Appl. 배포관리 (Container 방식의 Appl관리와 무중단 배포)
  ㄴ Monitoring&Logging : 물리자원,container자원을 다양한 형태의 view로 모니터링 수행 (physical, cluster, service usage정보)
  ㄴ Catalog&Registry : Appl에서 사용하는 Pre-Configured Backing service 관리기능 (redis, mq) 
  
  ci/cd (jenkins) 
  
---------------------------------------------------------------------  
4차시. 오픈소스 DevOps 도구 
ㅇ 단계별 도구
  ㄴ 계획 : 협업/일간관리 도구 (redmine)
  ㄴ 개발 : 코드버전관리 (git, subversion) 
  ㄴ 빌드 : compile, packaging단위 테스팅 도구 (maven) 
  ㄴ 테스트 : 다양한 테스트 도구 (sonarqube)
  ㄴ 릴리즈/배포 : 애플리케이션 관리 도구 사용  (docker)
  ㄴ 운영 : container orchestration 도구 인프라를 토대로 다룰 수 있는 도구
  ㄴ 모니터링 : 로깅관리, 가시화 대시보드 도구 사용 

ㅇ 실습할 환경 예시 
   ㄴ 통합개발환경(IDE): eclipse , spring tool suite , spring boot (SaaS서비스 개발에 용이) 
   ㄴ Git : 소스코드관리를 위한 분산형 버전관리 시스템 
ㅇ GitHub : Git의 SaaS 버전 . Git기반의 글로벌 Git저장소 서비스 
ㅇ maven : java소스코드를 배포용 산출물로 빌드하기 위한 도구, 의존성 라이브러리 
ㅇ jenkins : 지속적 통합을 자동화 (빌드->테스트->배포 자동화) 
ㅇ sonarqube : 소스코드 정적분석을 통해 품질대시보드 제공, 소스코드 품질점검 
ㅇ docker : 컨테이너 기반의 app 관리하는 가상화 플랫폼 . 동일한 환경,구성 유지 및 쉽게 관리
             리눅스 컨테이너 방식의 사용으로 성능저하 문제 해결

#####################################################
2주차 – DevOps를 위한 기초 이해

1차시. 로컬 개발 환경 

ㅇ 간단한 로컬 개발 환경 
   JDK 8 / Eclipse (Git plugin, maven plugin) / STS 
   Git 로컬 저장소 , Git 원격 저장소 

ㅇ 객체지향개발언어 자바 (jdk )
   ㄴ 자바가상머신 - wirte once, run anyware 
   ㄴ 자바 컴파일러 - 바이트코드 
   ㄴ API 패키지 - app 개발을 위한 라이브러리 

ㅇ OpenJDK : java standard edition의 오픈소스 구현체 
   ㄴ JCP (java community process) : java 표준 관리
   ㄴ JSR (Java Specification Request) : java 스펙의 요구사항 정의
   ㄴ Open JDK : JSR의 공식 레퍼런스 구현체  ( https://github.com/ojdkbuild/ojdkbuild ) 

ㅇ spring framework : 스프링 기반 애플리케이션 개발 지원 도구    
ㅇ sts : 스프링부트 애플리케이션 개발을 위한 eclipse 기반의 통합 개발환경 
ㅇ GitHub : Git의 글로벌 웹 호스팅 서비스, 세계 최대의  오픈소스 공유 플랫폼 (비공개/공개저장소 등)


   
---------------------------------------------------------------------  

2차시. 소스코드 관리 (1/2)
ㅇ 깃헙 - 원격저장소 생성 
ㅇ 깃 - 원격저장소 복제 : 원격 -> 로컬 저장소로 가져오기
ㅇ Git 로컬 저장소 Commit 
   - commit 절차 : git 관리를 위한 파일 등록
     ㄴ working tree : 개발자가 작업은 하지만 git으로 관리하지 않는 공간 
     ㄴ index : git 으로 관리하기 원하는 내용만 commit
	 ㄴ staging : working tree 의 내용을 저장소에 commit 하기 위해 인덱스에 먼저 등록. 원하는 부분만 선별적으로 commit 
	 ㄴ commit : local repo 에 저장              

ㅇ 깃 - 원격 저장소 푸시 : 로컬 변경사항을 원격 저장소로 push 
	 ㄴ push : local에서 변경된 내용을 원격저장소에 업로드 (local repo -> remote repo)    Team < push branch 'master' 

ㅇ pull : 원격저장소에서 local로 내용을 당겨오는 것. 
          pull실행시 github 원격저장소의 최신 변경 내역을 다운로드하여 local적용 
	        원격에서 수정한 후 sts에서 team > pull 해보자
ㅇ git 소스코드 충돌과 해결
   ㄴ push 명령 리젝트
   ㄴ 업데이트 내용 확인 후 merge 작업 직접 수행 
       예시) 원격저장소 먼저 수정하고, 로컬 내용 수정한 후 commit and push 
          -> git push 에서 충돌 오류 발생 -> git pull (오류발생) 
		  -> 머지) $ git add newfile.txt	(원격의 head 내용이 로컬 해당문서에 추가됨)
		  -> add index -> staged -> commit -> team>push branch master

https://backlog.com/git-tutorial/kr/stepup/stepup2_4.html
git status
git checkout master
git pull 

---------------------------------------------------------------------  
3차시. 소스코드 관리 (2/2) 
ㅇ github _ fork & pull 리퀘스트 
   기업의 프로젝트나 오픈소스 프로젝트의 경우 일반 개발자는 원격 저장소의 읽기 권한만 갖는 경우가 많다. 
   내용을 수정해서 반영하고 싶은 경우 해당 repo를 나의 로컬에 fork 하여 clone 한 후 project import 한 후 작업함

   ㄴ 워킹 트리 작업 공간은 깃으로 관리하지 않는 파일도 위치하는 공간 입니다. 
       깃으로 관리하는 공간은 워킹 스테이지 공간입니다.
   ㄴ 워킹트리내용을 저장소에 커밋하기 위해서는 인덱스에 먼저 등록해야 한다. 
	
ㅇ 브랜치 
   애플리케이션 개발시 소스코드를 공유하며 생성되는 여러 버전의 코드를 효과적으로 관리하기 위한 기능 
   동시에 다양한 작업 진행 가능
   여러 버전의 코드를 각각 독립적으로 유지관리, 통합 가능 
   - 유형
     ㄴ 마스터 브랜치 : git이 기본적으로 생성하는 이름 
	 ㄴ 통합 브랜치 : 항상 배포가능한 버전 . 정상 작동
	 ㄴ ★토픽 브랜치 : 기능추가나 버그 수정등의 변경 작업 발생시 작업별로 브랜치 생성하여 진행 

ㅇ 체크아웃 : 다른 브랜치로 전환하는 것 
             체크아웃 실행시 브랜치가 전환되므로 commit 실행하면 전환된 브랜치에 적용  
ㅇ 헤드 : 현재 사용중인 브랜치. 기본적으로 마스터의 선두  
ㅇ 머지 : 브랜치를 따로 만든 후 commit/push 후 Team > merge 를 하면 master 에 merge 됨
	 
---------------------------------------------------------------------  
4차시. 프로젝트 빌드 관리 
ㅇ 메이븐 : SW객체 모델 기반 프로젝트 관리 도구. 
            디렉토리 구조 - 정형화된 구조
			빌드 절차 - 일관된 방식으로 프로젝트 관리/운영
			의존성 라이브러리 관리 - 라이브러리 저장소를 통해 의존관계있는 라이브러리 자동관리
            -> 플러그인을 통한 다양한 기능 확장. 
 	        -> 아키타입 기능을 통한 프로젝트 템플릿 기능 (표준화된 템플릿) 
	ㄴ settings.xml : maven build 시 다운로드되는 라이브러리 로컬 저장소 경로 지정 
	ㄴ pom.xml (project object model) : 프로젝트마다 생성되는 기본정도 및 속성정보. 
	                                    다른 라이브러리와의 의존성, 플러그인, 빌드정보  (model version, groupId, artifactId, version) 
ㅇ 메이븐 빌드 수명주기 (phase 단계로 구성) 
   ㄴ 빌드 수명주기 : compile -> test -> package -> install (로컬저장소에 패키징 결과 배포) -> deploy (원격 저장소에 결과물 배포) 
   ㄴ 클린 수명주기 : 생성된 산출물을 삭제 (/target 폴더 삭제) 
   ㄴ 사이트 수명주기 : site (문서 산출물 생성) -> site-deploy (문서산출물을 서버에 배포) 
   
ㅇ 메이븐 컴파일 
   ㄴ 소스코드 및 자원파일을 타깃 디렉토리로 복사한 후 소스코드를 컴파일  
      (run > maven build > test-compile  입력 후 run 실행) 

ㅇ 메이븐 테스트 
   ㄴ 단위테스트 코드 실행
   ㄴ 테스트 스킵속성을 true로 설정하고 빌드하면 단위테스트 실패하더라도 계속 진행함 

ㅇ 패키징, 인스톨 및 배포 
   ㄴ package 컴파일과 테스트 완료 후 빌드산출물을 jar 또는 war로 패키징
      -> 패키징 후 배포  (install 로컬 -> deploy 원격저장소)   -> clean (타겟디렉토리 모든 내용 삭제) 

ㅇ 저장소 및 의존성 관리 
   ㄴ 중앙저장소(원격) : 메이븐의 중앙저장소. 일반개발자 임의 배포 불가
   ㄴ 사설저장소(원격) : 사내 또는 프로젝트용으로 구축
   ㄴ 로컬저장소 : 개발자PC의 저장소
   
   
ㅇ 프로젝트와 모듈
   ㄴ 프로젝트 : 하나의 프로젝트로 진행 또는 규모가 커지는 경우 프로젝트 분리
   ㄴ 마이크로서비스 : 매우 작은 단위로 프로젝트 구성 또는 멀티 모듈 프로젝트로 관리 
   
ㅇ 멀티모듈 프로젝트 
   ㄴ 상속 : 모든 POM은 최상위 POM을 상속. 필요시 부모 POM을 하위 모듈에서 상속 
   ㄴ 집합 : 상위 POM에서 <modules>로 관리
   ㄴ 모듈간 의존성 : <modules> 설정을 통해 여러 모듈 한번에 빌드
                      모듈간의 의존성은 기존 디펜던시 설정과 동일 
ㅇ 공통템플릿, 라이브러리 및 샘플 프로젝트 전파 유용
    ㄴ 넥서스 : 자체 저장소 
    ㄴ 아키타입 : 공통라이브러리, 공통설정	
   
      
#####################################################
3주차 – DevOps를 위한 도커 이해

3-1차시. 가상화와 컨테이너 - 클라우드 컴퓨팅 환경에서의 가상화와 컨테이너 개념 이해 

ㅇ IT인프라 운영방식의 전환 : IT환경이 클라우드 컴퓨팅환경으로 급속히 전환되고 있음 
   1) 온 프레미스 (On-Premise) 
      ㄴ 전통적인 시스템 운영방식. 자체적으로 데이터센터 보유, 직접 구축/운영유지 수행 
      ㄴ 단점 : 초기 투자비용 높고 운영유지 어려움. 
	           고정된 방식으로 컴퓨팅 자원을 활용하기 때문에 운영탄력성/자원 활용 비효율적 
   2) 오프프레이미 (off-premise) 
      ㄴ 클라우드 컴퓨팅을 활용하는 방식 
	  ㄴ 사용 요금을 내고 컴퓨팅 자원을 빌려 쓰는 방식
	  ㄴ 초기 구축비용 낮고, 보안이 중요하지 않은 업무에 적용 
   3) 클라우드 컴퓨팅의 핵심 기술 "가상화" 
      ㄴ 물리적 하드웨어를 논리적으로 추상화하는 것
	  ㄴ 하나의 물리적 하드웨어 -> 여러개인것처럼 동작 
	  ㄴ 여러개의 물리적 하드웨어 -> 하나인것처럼 동작

   4) 서버 - 특정 피크타임에 집중적으로 많은 자원이 사용. 보통의 경우 20% 이하 평균 사용. 
      사용하지 않는 80%의 유휴자원으로 다른 서버 운영한다면 "자원의 사용률 극대화"   
	※ 가상화를 통해 유휴 자원의 사용 효율성을 증대. CPU,메모리, 스토리지, 네트워크 등 가상화하여 사용 가능 

ㅇ 클라우드 컴퓨팅 
   ㄴ 기존의 서버, 스토리지, 네트워크 등의 하드웨어 위에서 동작하는 가상화 환경 
   ㄴ 하드웨어 구매/운영유지를 효과적으로 관리하여 비용 절감
   ㄴ 동적으로 급변하는 변경 수요에 효과적 대응 가능 

ㅇ 하드웨어 리소스별 가상화
   1) CPU 가상화 : 물리적 CPU의 코어에 가상의 CPU를 할당하여 사용하는 것
   2) 메모리 가상화 : 물리적 메모리의 특정영역에 가상메모리를 할당하여 사용하는 것
   3) 스토리지 가상화 : 물리적 스토리지에 특정 영역을 가상 스토리지로 할당하여 사용하는 것
   4) 네트워크 가상화 : 1) 가상의 네트워크 인터페이스를 할당하는 것
                        2) 가상의 네트워크를 구성하여 사용 

ㅇ 사용 유형별 가상화 
   1) 서버 가상화 : 하나의 물리서버를 기반으로 여러개의 OS를 설치하고 구동하여 여러대의 서버를 가상화
   2) 데스크톱 가상화 (VDI) : 원격지의 데이터센터 서버에서 가상의 PC 데스크톱 환경을 제공. 로컬PC사용하는 것처럼 가상화
   3) 데이터 가상화
   4) 어플리케이션 가상화   

ㅇ 가상화의 구현 방식 
    1. 가상머신 기반 가상화    
	   1) 가상머신 : 컴퓨팅 환경을 소프트웨어로 모방하여 구현한 것
	      ㄴ 운영체제 및 애플리케이션을 설치, 운영가능 
	      ㄴ 하나의 하드웨어에서 다수의 가상 머신을 구동하여 독립적인 역할 수행 
	      ㄴ 가상머신 간에는 하드웨어를 공유하면서도 각각 서로 다른 환경을 갖출 수 있으며 독립성 보장 
	      -> 하나의 가상머신에 오류가 발생하거나 중단되더라도 문제가 전체로 확장되지 않음 
	    2) 하이퍼바이저 (Hypervisor) 	
	       ㄴ 하나의 하드웨어 위에서 가상머신을 구동하게 해주는 것 (SW 또는 임베디드로 구현)
		   ㄴ 하드웨어와 가상 머신 사이에서 중간자 역할 (자원 할당 및 분리) 
		   -> 하드웨어를 직접적으로 사용하는 것보다 하이퍼바이저를 통해 가상머신을 활용하면 한정된 하드웨어 자원을 효과적으로 사용할 수 있음
		   
		   ※ 하이퍼바이저의 2가지 유형 
		   <Type-1> Native Hypervisor 
	               - 구성 : 하드웨어 > Hypervisor(Native) > 가상머신1(Guest OS > Application) ~ 가상머신N(OS, App) 
				   예) MS사의 Hyper-V
           <Type-2> Hosted Hypervisor 
                   - 구성 : 하드웨어 >> Host OS >> Hypervisor(App) > 가상머신 (Guest OS > Application) 		   
	               네이티브 방식에 비해 성능은 상대적으로 떨어짐 
                   예) 오라클사의 virtual box 
           
	-> "가상머신 기반 가상화는  "하이퍼바이저 위에 게스트OS를 여러개 구동시키기 때문에 자원 소모가 많고 성능 저하 문제 발생 
	    이에 대한 단점 해결을 위해 "컨테이너 기반 가상화" 
		
	2. 컨테이너 기반 가상화 
	   - 등장배경 : 
	     ㄴ 애플리케이션 실행시 환경에 따른 각종 문제 발생. 
		 ㄴ 컴퓨팅 환경이 바뀌더라도 안정적 실행 보장. 
		 ㄴ 실행하기 위한 모든 구성을 패키징하여 쉽게 배포/실행 
	   - 가상머신방식 : HW > OS > Hypervisor > 가상머신 (GuestOS, App, Bins, Libs) N개 
	     성능 느리고 자원 많이 사용. 게스트OS가 추가 설치되어 동작 
	   - 컨테이너방식 : HW > OS > Container Engine > App/bins/libs 가 N개 로 구성 
	    ★ 별도의 게스트 OS설치 및 운영 불필요. 가볍고 빠름 

		   
---------------------------------------------------------------------  
3-2차시. 도커 (Docker) 
ㅇ 도커란 : 2013년 등장한 컨테이너 기반 가상화 도구
   ㄴ 컨테이너를 위한 플폼, 도커 엔진을 통해 컨테이너 관리
   ㄴ 도커가 설치된 곳은 컴퓨팅 환경에 구애받지 않고 애플리케이션 신속 배포 및 확장
   ㄴ 이식성을 위해 애플리케이션을 표준화된 유닛으로 패키징 
      ㄴ 도커 이미지 : 라이브러리, 시스템도구, 코드, 런타임 등 실행에 필요한 파일 
      ㄴ 도커 컨테이너 : 도커 이미지가 실행된 인스턴스  
	   * 프로그램 : 실행 가능한 파일 (도커 이미지)
	   * 프로세스 : 프로그램이 실행된 상태 (도커 컨테이너) 
	   
ㅇ 과거 실행 환경 및 방식 
   개발환경 (HW, OS, 라이브러리,설정, 개발App)  -> 테스트 환경 -> 운영 환경 
   -> 모두 상이하며 정상 작동 어려움
   -> 전형적인 가변 인프라의 문제로 끊임없이 변경사항 갱신/관리 어려움
   -> 클라우드 컴퓨팅으로 전환 
   -> 서버 대수 급격히 증가
   -> 기존 방식대로 스크립트로 자동화하여 관리하는 것도 한계 
   -> 이러한 요소들이 DevOps를 실천하는데 매우 큰 장애요소가 됨
   
ㅇ 도커 기반 실행환경 및 방식 
   개발환경 (HW, Linux, Docker, 도커 이미지(런타임, 라이브러리,설정, 개발App))  -> 테스트 환경 -> 운영 환경 
   변경 사항 발생시 새로운 도커 이미지를 생성하여 대체 
   -> 실행환경이 변경되더라도 애플리케이션이 정상적으로 작동
   -> 가변적이 상황이 발생하더라도 쉽게 대응 
   -> 불변 인프라를 통해 이식성을 극대화하였음
   -> DevOps의 구체적 실현 가능성 높힘 
   
ㅇ 도커를 사용하는 이유
   1) 애플리케이션 운영 표준화 : 운영하면서 겪는 시행착오 쉽게 파악/개선
   2) 지속적 배포/전달 및 안정적 서비스 제공 속도 증대
   3) 서비스 제공을 위한 노력 감소, 자원사용률 증대 
   4) 비용 절감 

ㅇ 도커 구조 
   Docker CLI -> REST API ->  Docker Host (Host OS > Docker Daemon > Containers, Images) -> Docker Registry (Docker Image저장소) 

ㅇ 도커 기반 기술 
   ㄴ 컨테이너라는 격리된 실행환경 생성 
   ㄴ 리눅스 커널의 네임스페이스 기술 사용 
   
   1. 네임스페이스 
       1) PID (Process ID) : 프로세스에 할당된 고유 ID
	   2) NET (Networking) :  네트워크 인터페이스 관리
	   3) IPC (InterProcess Communication) : 공유 통신 자원 관리 
	   4) MNT (Mount) : 파일시스템 마운트 포인트 관리 (네임스페이스가 다르면 접근 불가)
	   5) UTS (Unix Time Sharing) : 호스트명, 도메인명 관리  
   2. 도커 컨테이너는 물리 하드웨어의 자원을 여러 컨테이너가 공유 -> 리눅스 커널의 Control Groups 기능 사용 
   3. CGroups (Control Groups) : 자원의 할당 관리, 프로세스와 스레드를 그룹화하여 그룹별로 CPU나 메모리 등의 자원 사용 제한 
     -> 하나의 컨테이너가 자원을 독점적으로 사용하는 등 다른 컨테이너에 영향을 주는 일 방지    
   4. Union File System : 도커 엔진이 사용하는 파일 시스템 
      ㄴ 가볍고 빠른 읽기 전용 레이어로 구성 
	  ㄴ 컨테이너 생성 (기존의 이미지 레이어 > 쓰기 전용 레이어) 
	  

 ---------------------------------------------------------------------  
3-3차시. 도커 (Docker) 설치 및 작동
ㅇ 도커 에디션 종류 
   1) Docker Comminuty Edition (CE) : 오픈소스 버전, 무료사용, 개인용
   2) Docekr Enterprise Edition (EE) : 기업용 상용버전. 인증된 플러그인 및 보안기능 등 추가 기능 제공 
   
ㅇ Docker CE 지원 프랫폼 
   1) Desktop : MacOS , MS Windows 10 (64bit pro) Hyper-V  (win 10 미만은 docker toolbox 설치 필요 )
   2) Server(Linux) : CentOS, Debian, Fedora, Ubuntu 
   
   windows10 설치 syacorn / ymcar (syhwang125@poscoict.com) 
   
   "C:\Program Files\Docker\Docker\Docker for Windows.exe"
   
ㅇ 도커 설치 및 환경 
   도커 CLI (powershell 실행) 
   $ docker version    (버전정보 확인) 
   $ docker system info 
   $ docker container run ubuntu:latest /bin/echo 'Hello World!' 
     ( docker container run : 도커 컨테이너 실행 / ubuntu:latest 는 ubuntu의 최신 버전 이미지  / /bin/echo 'Hello World!'  는 생성한 컨테니어에서 실행할 명령어) 
	 -> ubuntu:latest 이미지가 없으면 레지스트리에서 다운로드 받아서 실행함 

   PS C:\Users\황 서연> docker container run ubuntu:latest /bin/echo 'Hello World!'
	Hello World!
	
ㅇ Nginx 웹서버 작동 
   $ docker container run -d -p 80:80 --name webserver nginx 
    (-d : 컨테이너생성, 백그라운드에서 실행, -p 80:80 호스트 80번 포트와 컨테이너 80번 포트를 연결하고 접근 허가 / --name webserver 컨테이너의 이름을 webserver로 지정)
	 
   PS C:\Users\황 서연> docker container run -d -p 80:80 --name webserver nginx
	Unable to find image 'nginx:latest' locally
	latest: Pulling from library/nginx
   
   PS C:\Users\황 서연> docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS        S
586da1d2d2cc        nginx               "nginx -g 'daemon of…"   3 minutes ago       Up 2 minutes    server 

   http://localhost/  실행해 보세요~~ 
   
---------------------------------------------------------------------  
3-4차시. 도커 (Docker) 설치 및 작동
ㅇ 도커 허브 : 도커 공식 레파지토리 (http://hub.docker.com) 
ㅇ 도커 이미지 기본 명령어
   - 도커 이미지 검색 : $docker search [옵션] <검색키워드> 
     PS D:\DevOps> docker search ubuntu                     (docker hub 에서 ubuntu image 검색됨)
     PS D:\DevOps> docker search nginx --filter=stars=100   (repository 에서 별 100개 이상의 nginx 웹서버 이미지만 검색)

   - 도커 이미지 다운로드 : $docker image pull [옵션] 이미지명[:태그명]    
	 PS D:\DevOps> docker search centos   
     PS D:\DevOps> docker pull centos    (가장 최신 centos image 를 다운로드함) 
   
   - 도커 이미지 목록 확인 : $docker image ls [옵션][레파지토리명]    
     PS D:\DevOps> docker image ls                 (다운로드된 이미지 목록 확인)
     REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
	  nginx               latest              2bcb04bdb83f        6 days ago          109MB
	  ubuntu              latest              94e814e2efa8        2 weeks ago         88.9MB
	 PS D:\DevOps> docker image ls --digests     (보유 식별자가 추가됨) 
	 
  - 다운로드 받은 이미지 상세 정보 확인 : $docker image inspect [옵션] 이미지명 [이미지명]  (결과형식이 json으로 표현됨) 
	PS D:\DevOps> docker image inspect nginx        (다운로드된 이미지 목록 중 nginx 상세 정보 보기)
	[
		{
        "Id": "sha256:2bcb04bdb83f7c5dc30f0edaca1609a716bda1c7d2244d4f5fbbdfef33da366c",
        "RepoTags": [
            "nginx:latest"
			],
	]       환경정보, 도커버전 등 확인 가능  
   
   - 도커 이미지 삭제 : $docker image rm [옵션] 이미지명[이미지명]     
     (이미지를 삭제하면 중간 이미지도 삭제됨. --no-prune : 중간이미지를 삭제하지 않는 옵션  )
	 PS D:\DevOps> docker image rm nginx:1.10-alpine    (Tag로 삭제)
	 PS D:\DevOps> docker image rm 79e                  (Image ID로 삭제)
	 PS D:\DevOps> docker image rm --force ubuntu       (강제로 삭제)
	
3-5차시. 도커 (Docker) 컨테이너 기본 명령
ㅇ 도커 컨테이너 기본 명령 
   - 컨테이너 실행             : $docker container run
   PS D:\DevOps> docker container run -it --name "runtest" centos /bin/ls -al     
     (-it : 컨테이너의 표준 출력을 열고 tty를 확보한다는 의미임
	  "runtest" : 컨테이너 이름 
	  컨테이너 목록을 출력하는 명령  
	  -a 옵션은 실행정지 중인것을 포함하여 모든 컨테이너의 상태를 확인할 수 있음) 
   
   - 컨테이너 목록 확인        : $docker container ls 
   PS D:\DevOps> docker container ls -a
   PS D:\DevOps> docker container run -it --name "runtest" centos /bin/ls -al
   PS D:\DevOps> docker container run --rm -it --name "runtest3" centos /bin/ls -al	 
   (--rm 옵션은 컨테이너 실행이 종료되면 자동으로 컨테이너가 삭제됨) 
   
   PS D:\DevOps> docker container ls --all (정지상태인 컨테이너까지 표시) 
   
   - 컨테이너 정지 : $docker container start, stop, restart 
                                 $docker container stop [옵션] <컨테이너 식별자>   (--time, -t 컨테이너 정지시간 지정) 
	PS D:\DevOps> docker container run -d centos /bin/ping localhost
	77438858de2c4c197aae22d43a0abfed8363d2a382813e2d0df721681116be82
	PS D:\DevOps> docker container ls
	CONTAINER ID        IMAGE               COMMAND                 CREATED             STATUS              PORTS               NAMES
	77438858de2c        centos              "/bin/ping localhost"   9 seconds ago       Up 7 seconds                            nifty_pasteur
	PS D:\DevOps> docker container logs -t 774    (774 는 container id일부) 
	PS D:\DevOps> docker container stop 774       (해당 컨테이너를 stop)
	774
	PS D:\DevOps> docker container ls -a		   (목록에서 제거된 것을 확인) 
	
    - 컨테이너 시작 : 
	PS D:\DevOps> docker container start 774
	774
	PS D:\DevOps> docker container ls -a          (정지되었던 컨테이너가 다시 start 됨) 
	CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS                NAMES
	77438858de2c        centos              "/bin/ping localhost"    6 minutes ago       Up 2 seconds                                     nifty_pasteur
								 
   - 컨테이너 삭제             :     $docker container rm [옵션] [컨테이너 식별자]   (--force, -f 실행중인 커테이너 강제제거) 
    PS D:\DevOps> docker container ls -a
	CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS                NAMES
	77438858de2c        centos              "/bin/ping localhost"    9 minutes ago       Up 2 minutes                                     nifty_pasteur
	f96e40eb585d        centos              "/bin/ls -al"            17 minutes ago      Exited (0) 17 minutes ago                        runtest2
	PS D:\DevOps> docker container rm runtest            (종료된 컨테이너 삭제)
	runtest
	PS D:\DevOps> docker container rm nifty_pasteur		 (실행중인 컨테이너 삭제하면 오류) 
	Error response from daemon: You cannot remove a running container 77438858de2c4c197aae22d43a0abfed8363d2a382813e2d0df721681116be82. 
	Stop the container force remove
	PS D:\DevOps> docker container rm nifty_pasteur -f       (실행중인 커테이너 강제 삭제를 위해 -f 옵션 추가)    
	nifty_pasteur
	PS D:\DevOps> docker container ls -a
	CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS                NAMES
	f96e40eb585d        centos              "/bin/ls -al"            18 minutes ago      Exited (0) 18 minutes ago                        runtest2
	586da1d2d2cc        nginx               "nginx -g 'daemon of…"   4 days ago          Exited (255) 11 hours ago   0.0.0.0:80->80/tcp   webserver
	288086c1d4bb        94e814e2efa8        "/bin/echo 'Hello Wo…"   4 days ago          Exited (0) 4 days ago                            infallible_jennin
	08b6f3f7163f        94e814e2efa8        "/bin/echo 'Hello Wo…"   4 days ago          Exited (0) 4 days ago                            xenodochial_gagar
   
   - 컨테이너 로그 확인        : $docker container logs  
   
	
#####################################################
4주차 – 도커를 활용한 DevOps 환경 구축

4-1차시. Dockerfile 기초
ㅇ Dockerfile 이란? 텍스트형식으로 구성된 이미지를 생성하는 명령어의 집합 

	FROM centos ... 명령어 ...   -> docker build -> 이미지 생성 -> docker 이미지 

ㅇ Dockerfile 명령어
   - FROM : 베이스 이미지 지정
   - MAINTAINER : 작성자  (이름, 메일 등) 
   - RUN : 베이스 이미지에서 스크립트나 명령어를 실행하는 명령  
   - CMD : 데몬 실행. 컨테이너에서 실행할 명령어를 실행시키는 명령  
   - EXPOSE : 포트설정. 호스트와 연결할 포스번호를 설정하는 명령  
   - WORKDIR : 작업 위치 설정 . 명령을 실행하는 작업 디렉토리 설정 
   - ENV : 환경별수 설정 
   - ADD : 파일 추가 . 이미지에 호스트의 파일과 디렉토리 추가
   - COPY : 파일 복사. ADD보다 더 단순하게 호스트의 파일만을 복사하는 작업만 수행 가능  
   - ENTRYPOINT : 데몬실행. 컨테이너 시작시 스크립트나 명령을 실행시키는 명령  
   - USER : 사용자 계정 설정 
   - VOLUME : 이미지에 볼륨을 할당하는 명령 

ㅇ FROM <이미지명> : <태그>        (태그 생략시 최신버전 적용) 
   MAINTAINER <이름> <이메일> 등   예) MAINTAINER James Lee james@gmailcom    
   RUN <실행명령어>				   예) RUN echo hello, shell   (/bin/sh -c 로 실행하는 방식과 동일) 
									   RUN ["echo", "Hello, exec"]  (쉘을 거치지 않음. JSON형식) 
   CMD <실행명령어>					(마지막 한개의 CMD명령어만 적용) 
                                    예) CMD echo Hello, shell       (/bin/sh -c 로 실행하는 방식과 동일) 
									   RUN ["echo", "Hello, exec"]  (쉘을 거치지 않음. JSON형식) 
   ENTRYPOINT <실행명령어> 		     (실행 시점에 명령어의 값을 입력받을 경우에 CMD명령어와 함께 사용) 
									예) ENTRYPOINT ["bin/echo", "Hello, entrypoint"] 
   EXPOSE <포트번호>			    예) EXPOSE 8080	(실제 포트와 바인딩되지 않고 Docker RUN명령어의 -p옵션과 함께 사용)							
									    EXPOSE 80 443 
   WORKDIR <작업디렉토리>           예) WORKDIR /path    (상대경로 가능)
   ENV <key> <값> 					예) ENV SONATYPE_WORK /sonatype-work 
   ENV <key> = <값> 		 	    예) ENV NEXUS_VERSIOn 2.14.1-01 
								    예) ENV NEXUS_HOME=/opt/sonatype/nexus/ 
   ADD <복사할 파일 경로> <Docker 이미지 파일 경로> 
   ADD ["복사할 파일 경로", "Docker 이미지 파일 경로"] 			예) ADD test.html /web 
   VOLUMN <"/마운트포인트"> 			예) VOLUMN /var/log 
   
ㅇ Dockerfile 작성 
   FROM busybox 
   MAINTAINER James Lee (jameslee@gmail.com)
   ENTRYPOINT ["/bin/cat"]
   CMD ["/etc/passwd"] 
   
   * docker RUN으로 실행할때 별도의 입력값이 없으면 CMD 지정값이 사용됨

ㅇ docker 이미지 생성 및 실행 
   docker builde 명령으로 dockerfile로 이미지 생성 
   $docker build -t <생성할이미지>:<태그명><Dockerfile위치> 
   
	PS D:\DevOps\dockerfile> type .\Dockerfile      (도커파일 내용확인) 
	FROM busybox
	MAINTAINER James Lee (jameslee@gmail.com)
	ENTRYPOINT ["/bin/cat"]
	CMD ["/etc/passwd"]
	
	PS D:\DevOps\dockerfile> docker build -t sample:1.0 .        (도커 빌드) 
	PS D:\DevOps\dockerfile> docker images
	REPOSITORY          TAG                 IMAGE ID            CREATED              SIZE
	sample              1.0                 ff9a3b2208bb        About a minute ago   1.2MB
    busybox             latest              d8233ab899d4        6 weeks ago          1.2MB
         
	PS D:\DevOps\dockerfile> docker run sample:1.0				(도커이미지의 CMD /etc/passwd 가 실행됨 ) 
		root:x:0:0:root:/root:/bin/sh
		daemon:x:1:1:daemon:/usr/sbin:/bin/false
	PS D:\DevOps\dockerfile> docker run sample:1.0 /etc/group   (도커이미지에 RUN 명령어로 /etc/group을 주면 실행됨) 
	
---------------------------------------------------------------------  
									
4-2차시. 애플리케이션을 도커 이미지로 생성하기 

ㅇ 애플리케이션을 도커 이미지로 생성하기 
PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> type ./Dockerfile
PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker build -t gs-spring-boot-docker .
PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker images
REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
gs-spring-boot-docker   latest              12cc79803804        29 seconds ago      121MB


PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker run -p 8080:8080 gs-spring-boot-docker

http://localhost:8080 

ㅇ 애플리케이션 도커 이미지 공유 
   - 공식 도커 레지스트리인 Docker Hub에 이미지를 등록하여 활용 가능 
   - 프라이빗 네트워크에서 직접 도커 레지스트리를 구축하여 활용 가능 
   
ㅇ DOcker Registry 구축 (5000 port 사용)
   PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker run -d -p 5000:5000 registry:2.0 

ㅇ Docker 이미지 업로드  (이미지 태그를 부착)
    docker tag <로컬이미지명> <레지스트리주소 : 포트번호>/<이미지명>
	docker push 
	
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker ps (docker registry 동작여부 확인)
	CONTAINER ID        IMAGE                   COMMAND                  CREATED             STATUS              PORTS
    NAMES
	5cfb5533a8df        registry:2.0            "registry cmd/regist…"   9 minutes ago       Up 9 minutes        0.0.0.0:5000->5000/t
	cp   flamboyant_lalande	

	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker images
	REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
	gs-spring-boot-docker   latest              12cc79803804        19 minutes ago      121MB

	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker tag gs-spring-boot-docker localhost:5000/gs-spring-boot-docker
	(도커 이미지 태그 지정) 
	
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker images
	REPOSITORY                             TAG                 IMAGE ID            CREATED             SIZE
	localhost:5000/gs-spring-boot-docker   latest              12cc79803804        20 minutes ago      121MB
	gs-spring-boot-docker                  latest              12cc79803804        20 minutes ago      121MB

    ( 로컬 레지스트리에 push)
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker push localhost:5000/gs-spring-boot-docker

ㅇ 도커 이미지 도커 허브 업로드	
	docker login
	docker tag <image명> <도커허브username>/<이미지명>
	docker push 
	
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker login
	Authenticating with existing credentials...
	Login Succeeded
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker tag gs-spring-boot-docker syacorn/gs-spring-boot-docker
	
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker images
	REPOSITORY                             TAG                 IMAGE ID            CREATED             SIZE
	gs-spring-boot-docker                  latest              12cc79803804        28 minutes ago      121MB
	syacorn/gs-spring-boot-docker          latest              12cc79803804        28 minutes ago      121MB
	
	(도커 허브에 업로드)
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker push syacorn/gs-spring-boot-docker
	
	(로컬 레지스트리의 이미지 삭제_)
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker rmi syacorn/gs-spring-boot-docker
	Untagged: syacorn/gs-spring-boot-docker:latest
	Untagged: syacorn/gs-spring-boot-docker@sha256:cce6e74b9efadcb098934548fe6d3cb2444e25cb5a1cfaa9de5f0c325581e30b
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker rmi localhost:5000/gs-spring-boot-docker
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker rmi gs-spring-boot-docker

	(로컬 레지스트리에서 다운로드) 
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker pull localhost:5000/gs-spring-boot-docker
	
	(도커 허브에서 다운로드)
	PS D:\DevOps\sts4workspace\gs-spring-boot-docker-complete> docker pull syacorn/gs-spring-boot-docker

---------------------------------------------------------------------  
	
4-3차시. Docker Compose 기초 
ㅇ Docker Compose : 여러개의 컨테이너를 일괄적으로 관리하는 도구 
ㅇ docker-compose.yml
   docker compose의 구성파일 
   한 파일 안에 여러 컨테이너 설정 내용 저장 
   도커 애플리케이션을 위한 서비스,네트워크, 볼륨을 정의함 (최신버전 version3)
   docker-compose의 구성파일은 텍스트파일인 YAML형식을 사용 
   
ㅇ YAML형식
    계층구조의 데이터 표현 양식. xml,json보다 가벼움
	탭대신 공백사용. 배열데이터의 경우 - 기호 붙임. #은 주석 

ㅇ docker-compose 명령어 
   up 
   ps 
   logs 
   run  
   start/stop
   rm    

---------------------------------------------------------------------  
   
4-4차시. CI 환경 구축하기 
ㅇ 지속적 통합 환경 
   GitLab (계획,일감관리등 깃) -> Jenkins (소스통합,빌드,정적분석 등) -> SonarQube (소스품질점검)  

ㅇ 용어 
   GitLab : DevOps 생명주기 전반을 지원하는 도구 
   GitLab DevOps 생명주기 
     Manage > Plan > Create (소스/데이터 생성관리) > Verify > Package (도커컨테이너 레지스트리) > Release > Configure > Monitor > Secure) 
   Jenkins : 소스코드설정(Gut, SUbversion), 빌드유발설정, 빌드환경설정 등 
   SonarQube : Projects(테스트커버리지, 코드중복, 버그,코드스멜 등), Issues (코딩규칙위반사항), Rules(코딩규칙), Quality Profiles(품질정책) , QUality Gates 
   
   
ㅇ 실습   
STS 에서 git clone  (https://github.com/hussainweb/gitlab-jenkins-sonarqube) 
PS D:\DevOps\gitRepo\gitlab-jenkins-sonarqube> type docker-compose.yml
PS D:\DevOps\gitRepo\gitlab-jenkins-sonarqube> type Dockerfile.jenkinns 
PS D:\DevOps\gitRepo\gitlab-jenkins-sonarqube> docker-compose up -d      (구동시키기 위해서 명령 실행) 

PS D:\DevOps\gitRepo\gitlab-jenkins-sonarqube> docker ps
CONTAINER ID        IMAGE                              COMMAND                  CREATED             STATUS
    PORTS                                                                                 NAMES
01c15ff9e145        sonarqube:7.6-community            "./bin/run.sh"           4 minutes ago       Up 4 minutes
    0.0.0.0:9000->9000/tcp                                                                gitlab-jenkins-sonarqube_sonarqube_1
88d668bacb2b        gitlab/gitlab-ce:latest            "/assets/wrapper"        4 minutes ago       Up 4 minutes (health: starting
)   80/tcp, 0.0.0.0:22->22/tcp, 0.0.0.0:8000->8000/tcp, 0.0.0.0:8443->8443/tcp, 443/tcp   gitlab-jenkins-sonarqube_web_1
84ab10435cf6        gitlab-jenkins-sonarqube_jenkins   "/sbin/tini -- /usr/…"   4 minutes ago       Up 4 minutes
     0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp                                      gitlab-jenkins-sonarqube_jenkins_1
	 
	 
★  여기서부터 안됨... 5:30초 영상부터 시작 	 

PS D:\DevOps\gitRepo\gitlab-jenkins-sonarqube> docker logs gitlab-jenkins-sonarqube_jenkins_1 

    브라우저에서  http://localhost:8080 접속 후 패스워드 복사하면 플러그인이 설치됨   
  
  
ㅇ 지속적 통합 환경 : gitlab, maven, jenkins,
계획 (협업/일감관리) -> 개발(코드버전관리) -> 빌드(컴파일/패키징) -> 테스트 (정적분석) 


#####################################################
•5 주차 - 정적분석과 소스 품질


5-1차시. 정적분석의 이해와 관련도구 소개 

ㅇ 정적분석 유형
   - 피어리뷰 : 2~3명이 진행. 코드설명, 아이디어/결함발견. 시간 많이 소요
   - 패스 어라운드 : 작성자가 리뷰 메일
   - 팀리뷰 : 
   - 워크스루 : 발표자가 리뷰 주제발표 . 참여자의견/아이디어 듣는 방식 
   - 코드 인스펙션 

ㅇ 소스코드 분석 후 작업 수행 : Rule기반으로 소스검사. 오류/위험 식별 
   오픈소스 도구 
   * checkstyle : 자바소스코드 코딩규칙에 대한 위반사항 분석 
   * FindBugs : 코딩모범사례 BP중점. 컴파일된 클래스 파일인 바이트코드 분석, 작성. 자바7이상 
   * PMD : 자바,자바스크립트,XML,JSP등의 언어로 작성된 소스코드 분석
   * PML Rule 설정 : Best Practice, 코드스타일, 디자인, 문서화, 오류,멀티스레딩, 성능, 보안 등 
   
---------------------------------------------------------------------  

5-2차시. SW구조 분석 도구 

ㅇ Architectural Viewpoint 
ㅇ 산출물 현황화에 소요되는 시간을 단축시키는 도구 
   - SchemaSpy 
     JDBC로부터 얻은 메타데이터를 분석, 관련 상세정보르르 HTML형식으로 생성하는 무료 오픈소스 자바툴 
     그래픽 뷰 형태. 개별 HTML 하이퍼링크 
   - Doxygen 
     소스코드 기반으로 HTML,PDF, RTF, Latex 포맷 등의 문서 생성 도구 
	 애플리케이션 구조 파악 용이 
     javaDoc 주석 연계 자동생성 
   - UMLgraph 
   - Enterprise Architect    


---------------------------------------------------------------------  

5-3차시. SonarQube 
제품군 : SonarQube, SonarLint, SonarCloud
water Leak Paradigm 을 통해 소스추가, 변경시 새로 발견된 문제들을 제어 
sonarqube 결함등급 : 

#####################################################
•6 주차 - 리팩토링

6-1차시. 소스코드 리팩토링의 개념과 필요성
ㅇ 리팩토링 : 명명규칙 (클래스,객체이름 - 동사,명사구 / 메서드이름 - 동사,동사구)



6-2차시. 소스코드의 실질적 품질을 높이기 위한 리팩토링 방법을 적용할 수 있다.
