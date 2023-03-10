문서정보 : 2023.02.05.~ 작성, 작성자 [@SAgiKPJH](https://github.com/SAgiKPJH)

<br>

# Plant_Factory
식물 자동 관리 장치 제작

### 목표

- [x] 1. 식물 자동 관리 장치 프로그램 개요
  - [x] 개요
  - [x] 요구사항
  - [x] 요구사항 총족을 위한 기술적 내용
  - [x] 요구사항 총족을 위한 물리적 내용
- [x] 2. 식물 자동 관리 장치 설계
  - [x] 개발 환경 설계
  - [x] 개발 구조 설계
  - [x] 개발 관리 설계
  - [x] 개발 일정 설계
- [ ] PPT 제작 (설계)
- [ ] 3. 식물 자동 관리 장치 기본 구축
- [ ] 4. 식물 자동 관리 장치 개발


### 제작자
[@SAgiKPJH](https://github.com/SAgiKPJH)

### 참조

- [참조링크](참조링크)

<br>

---

# 1. 식물 자동 관리 장치 프로그램 개요

## 1-1 개요

사람들은 식물, 동물을 키우는 데에서 많은 영감을 얻고, 행복을 얻는다. 하지만 무언가를 책임져 키우는 일은 매우 어려운 일이다.  
식물을 기르는 초심자에게 있어서 보조할 수 있는 장치, 식물을 많이 키우는 사람들을 위해 보조할 수 있는 장치를 만들어, 식물을 키우는데 보다 더 쉽게 관리할 수 있는 장치를 만들고자 한다.  
개인적으로도 식물을 키우고 싶고, 이를 통해 식물을 더 자세히 이해하고 공부, 연구하며 더 나아가 IoT 분야의 실력을 기르는데 목적이 있다.

<br>

## 1-2 요구사항

- 자동으로 식물을 관리한다.
  - 식물에게 자동으로 물을 준다.
  - 식물에게 자동으로 빛을 조정한다.
- 외부에서 인터넷을 통해 식물의 상태를 확인할 수 있다.
- 식물의 상태를 자동으로 확인하여 보고한다.

<br>

## 1-3 요구사항 총족을 위한 기술적 내용

### 공통 내용

- 단계적으로 차례로 개발한다. (1차, 2차, ...)
- 품질관리를 위해 Test를 구성한다
- Git을 이용해 코드를 관리한다

### 1차 기술적 내용

- 구현 보드 : Raspberry-Pi 활용
- DB 활용
  - PostgreSQL
- UI
  - 관리자 UI (시스템 관리 부분)
    - 활용 여부 설계 필요
  - 외부 UI (DB 데이터 가공부분)
    - Docker 또는 React 등을 활용해본다.

<br>

## 1-4. 요구사항 총족을 위한 물리적 내용

### 1차 물리적 내용

- RaspberryPi 4 model B 보드
- 외부 UI 사이트 운영, DB 서버를 위한 보조장비 (win or linux)
- 카매라
- 급수 부품
- 급수 모터
- 양분 주입
- 전원

<br><br><br>

# 2. 식물 자동 관리 장치 설계

## 2-1 개발환경 설계

### 개발 보드
- 사용 언어
  - python 3

### 서버 장비
- Latte Panda (or Laptop or Jetson Nano)

### DB
- PostgreSQL

### 개발 서버
- React?
- Grafana

### Test
- xUnit
- FluentAssertion

<br><br>

## 2-2 개발 구조 설계

### 개발 요점
- 장비
  - 식물 자동 관리 부문
  - 장비 자체 관리 부문
  - 서버 전송 부문
- 서버
  - 수집
  - 가공
- 클라이언트 (웹)

### 폴더 구조

- RaspberryPi
  - Fish : 프로젝트 폴더
    - Model : 학습 Model을 저장하는 폴더
    - Code : .py등 코드를 저장하는 폴더
      - Test : Test를 저장하는 폴더 
    - Image : Image를 저장하는 폴더
    - Log : 로그를 저장하는 폴더
- Server
  - Server : 서버와 관련되 내용을 저장하는 폴더
  - Data : 데이터를 저장하는 폴더
  - Log : 로그를 저장하는 폴더

### 코드 구조 (기능별 분리)

- RaspberryPi
  - main : 메인 py
  - camera : 카메라 handling과 관련된 py
  - control : 기타 장비에 대한 py
  - server : server와의 관계에 대한 py
  - selfChecking : 장비 자가 검진에 대한 py
- Server
  - selfChecking : 서버 자가 검진에 대한 내용
  - DB : DB 운영에 대한 내용
- Test
  -  각 코드별로 Test가 각각 존재한다. 

<br><br>

## 2-3 개발 관리 설계

### 관리 툴

- Git
- Git Hub
- Git Fork

### Git repository 구성
- / : README.md을 배치
- /Doc : [문서].md를 배치
- /Code : 코드를 배치
- /Presentation : PPT 등을 배치

### Git Branch 구성

- main : Release 배포, README.md 문서 (public)
- Develop : 개발 통합 (private)
- Feature(n) : 기능 구현 (private)
- Release : 배포용, 모든 개발 결과가 이곳에 저장 (private)
- Test : Test 공간 (private)

<br><br>

## 2-4 개발 일정 설계

### 6개월 (대략) (4W = 1M)
- (2W) 개요 작성                              (2023.02.05.~02.21.)
- (1M) 설계                                   (02.22.~03.22.)
- (1M) 개발                                   (03.23.~04.23.)
- (2W) 추가 설계                              (04.24.~05.08.)
- (2W) 추가 개발                              (05.09.~05.23.)
- (1M) Test 및 개선                           (05.24.~06.24.)
- (2W) 최종 Test                              (06.25.~07.09.)
- (1M) 예비 일                                (1M, 30d)
- (1W) 배포 준비 및 출시                       (08.10.~08.16.)

<br><br><br>

# 3. ArtistHelper 기본 구축

<br><br><br>

# 4. ArtistHelper 기본 구축
