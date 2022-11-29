---
layout: default
title: Six Sigma
nav_order: 1
parent: Production
grand_parent: Engineering Study

---

## 6 Sigma

### 표준편차(Standard Deviation, 𝜎)
- 통계 집단의 분산의 정도 또는 자료의 산포도를 나타내는 수치이다.

### 정규분포(Normal Distibution)
![img](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Standard_deviation_diagram.svg/700px-Standard_deviation_diagram.svg.png)
- 평균을 중심으로 ±𝜎 범위는 전체의 68.3%, ±2𝜎 범위는 전체의 95.5%, ±3𝜎 범위는 전체의 99.7%이 된다.
  (±6𝜎 범위는 전체의 99.99%, 100만개 중 3.4개만 벗어남)

### CP(공정능력, Capability of Process)
- 공정 능력은 규격의 상한(USL)과 규격의 하한(LSL) 사이에 얼마나 촘촘하게 데이터가 생산되느냐로 측정한다.
- USL과 LSL 사이에 6개 표준편차가 들어가는 정도를 CP=1으로 기준으로 잡는다. 표준편차가 작아서 규격 안에 보다 많이 들어간다면 CP 값이 커진다.
- CP=(USL-LSL)/6𝜎
- CP는 규격 내에서 데이터의 치우쳐짐이 고려되지 않은 수치이므로, 치우침을 고려할 때는 CPK를 사용한다. 
- CPK=(1-k)xCP
- k=｜규격중심-데이터중심｜/(규격공차/2)
- 일반적으로 CPK 1.33 기준으로 평가한다. (4𝜎 수준, 99.4%)


### 6 시그마
- 완벽에 가까운 제품이나 서비스를 개발하고 제공하기 위한 목적으로 정립된 품질 경영 기법
- 정규분포에서 ±6𝜎 범위를 추구. 100만개 중 3.4개 불량 수준

---
