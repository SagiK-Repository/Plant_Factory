문서정보 : 2023.02.05.~ 작성, 작성자 [@SAgiKPJH](https://github.com/SAgiKPJH)

<br>

# Plant_Factory
식물 자동 관리 장치 제작

### 목표

- [ ] 1. 식물 자동 관리 장치 프로그램 개요
  - [ ] 개요
  - [ ] 요구사항
  - [ ] 요구사항 총족을 위한 기술적 내용
- [ ] 2. 식물 자동 관리 장치 설계
  - [ ] 개발 환경 설계
  - [ ] 개발 구조 설계
  - [ ] 개발 일정 설계
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

<br>

## 1-3 요구사항 총족을 위한 기술적 내용

### 공통 내용

- 단계적으로 차례로 개발한다. (1차, 2차, ...)
- 품질관리를 위해 Test를 구성한다
- Git을 이용해 코드를 관리한다

### 1차 기술적 내용

- 구현 보드 : Raspberry-Pi 활용
- DB 활용
- UI
  - 관리자 UI (시스템 관리 부분)
    - 활용 여부 설계 필요
  - 외부 UI (DB 데이터 가공부분)
    - Docker 또는 React 등을 활용해본다.

<br>

## 1-4. 요구사항 총족을 위한 물리적 내용

### 1차 물리적 내용

- RaspberryPi 보드
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
  - python

### DB
- RabbitMQ

### 개발 서버
- React?

### Test
- xUnit
- FluentAssertion

<br><br><br>

# 3. ArtistHelper 기본 구축

<br><br><br>

# 4. ArtistHelper 기본 구축
