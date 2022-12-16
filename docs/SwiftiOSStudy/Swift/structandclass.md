---
layout: default
title: Struct and Class
nav_order: 1
parent: Swift
grand_parent: Swift & iOS Study

---

# **Struct and Class**

([학습 참고 자료 링크 - Swift 문서](https://docs.swift.org/swift-book/LanguageGuide/ClassesAndStructures.html))

([학습 참고 자료 링크 - Apple developer documentation](https://developer.apple.com/documentation/swift/choosing-between-structures-and-classes))

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

```swift
let hd = Resolution(width: 1920, height: 1080)
var cinema = hd
cinema.width = 2048
// hd.width : 1920, cinema.width : 2048
```

## class은 참조 타입
참조 타입은 변수 또는 상수에 할당되거나 함수에 전달될 때 복사되지 않고, 동일한 기존의 인스턴스에 대한 **참조**가 사용된다.

```swift
let tenEighty = VideoMode()
tenEighty.frameRate = 25.0
let alsoTenEighty = tenEighty
alsoTenEighty.frameRate = 30.0
// tenEighty.frameRate : 30, alsoTenEighty.frameRate : 30
```

## struct와 class 중에 어떤 것을 선택해야 하는가
애플 문서에는 다음과 같은 권장 사항이 있다.
- 기본적으로 struct를 사용
  - struct는 값 타입이므로 코드 일부에 대해 더 쉽게 추론 가능
  - 의도하지 않은 변경 사항이 발생하지 않음

- Object-C 상호 운용이 필요할 떄 class를 사용
  - Objc를 사용해야 하는 경우 상속이 필요할 수 있기 때문

- 고유한 값을 제어해야 하는 경우 class를 사용
  - swift의 class는 참조 타입으로 고유한 값으로 사용되므로, 여러 곳에 쓰여도 한 곳에서 수정한 사항이 다른 곳에서도 적용됨. 파일 관리나 네트워크 연결에 주로 사용

- 상속과 공유 동작을 모델링할 때는 struct와 protocol 사용
  - struct와 protocol은 protocol만 채택할 수 있으며 class는 상속할 수 없으나, protocol을 이용하여 상속 계층을 구현할 수 있음. class는 다른 class하고만 호환되지만, protocol은 class, enum, struct가 모두 채택할 수 있음


---