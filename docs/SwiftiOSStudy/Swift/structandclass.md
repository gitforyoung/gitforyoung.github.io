---
layout: default
title: Struct and Class
nav_order: 1
parent: Swift
grand_parent: Swift & iOS Study

---

# **Struct and Class**

([학습 참고 자료 링크 - Swift 문서](https://docs.swift.org/swift-book/LanguageGuide/ClassesAndStructures.html))

## Struct와 Class의 차이점
차이점만 간략히 정리하여 비교해보았다.
- struct는 다른 struct를 상속할 수 없음
- struct는 초기화 함수 initializer 생략 가능
- class는 deinitializer가 있음
- struct는 값 타입, class 참조 타입
- struct는 내부의 method를 통해 자기 자신의 property를 바꿀 수 없음(mutating을 써서 변경)


## 정의
구조는 둘다 비슷하다. 첫글자는 대문자로 하여 구분한다.
```swift
struct SomeStructure {
    // code
}
class SomeClass {
    // code
}
```

## 인스턴스 생성
인스턴스 생성 및 초기화도 비슷하다.
```swift
let someStructure = SomeStructure()
let someClass = SomeClass()
```

## property 접근
점으로 구분하여 접근가능하고, 변수에 값 할당 가능하다.
```swift
someStructure.width
someClass.height = 100
```

## struct와 enum은 값 타입
값 타입은 변수 또는 상수에 할당되거나 함수에 전달될 때 값이 **복사**된다.


---