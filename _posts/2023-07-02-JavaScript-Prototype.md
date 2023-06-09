---
title: 자바스크립트 프로토타입
author: syboosyboo
date: 2023-07-02 12:17:00 +0900
categories: [Front-End]
tags: [JavaScript, Prototype]
pin: true
math: true
mermaid: true
---


# 프로토 타입

## 정의
- 자바스크립트 라이브러리를 뭔가 해보겠다고 하면 깊이 있는 메서드를 찾아봐야한다.
- 일반적인 상속이랑은 다른 개념이다
  - 자바스크립트에는 클래스 정의를 사용한 클래스가 없다
  - 자바스크립트에서 ‘복사’를 통한 상속은 없다
  - 프로토타입 체인을 이용한 속성의 상속은 있다.
- 프로토타입은 클래스, 객체의 내용 복사 없이도 상속을 구현할 수 있게 해주는 방법이다
- 프로토타입은 연결(__proto__)이다

## 프로토타입 체이닝

- 특정 객체의 프로퍼티나 메서도에 접근하려고 할 때 객체에 접근하려는 프로퍼티 또는 메소드가 없다면
- __proto__가 가리키는 링크를 따라 자신의 부모 역할을 하는 프로토타입 객체의 프로퍼티나 메소드를 차례대로 검색한다.
- 이러한 상속 관계를 프로토타입 체인이라고 한다.

### Prototype Object(프로토타입 객체)
- 모든 함수(function) 객체는 "prototype"이라는 속성을 가진다
  - prototype 속성은 해당 함수의 프로토타입 객체를 가리킨다.

### Constructor(생성자)
- 프로토타입 객체를 가지고 있는 함수를 생성자라고 한다. 
- 생성자를 사용하여 새로운 객체를 생성하면, 해당 객체는 생성자 함수의 프로토타입을 상속한다.

### Object.create()
- 자바스크립트에서 객체를 생성하는 데 사용하는 메서드이다
- 지정된 프로토타입을 가진 새로운 객체를 생성한다다.

## 자바스크립트 동작 방식(class)

1. new 연산자가 새로운 빈 객체를 메모리 상에 생성한다
2. 생성된 빈 객체가 this에 바인딩 된다
3. this 객체의 속성을 채우는 동작이 수행된다
4. return 하는 것이 없다면 그렇게 만들어진 this가 return이 된다.

### 출처
- [코딩애플 유튜브](https://www.youtube.com/@codingapple)
- [우아한테크코스 유튜브](https://www.youtube.com/@woowatech)
- [위키백과](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%ED%86%A0%ED%83%80%EC%9E%85_%EA%B8%B0%EB%B0%98_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)
