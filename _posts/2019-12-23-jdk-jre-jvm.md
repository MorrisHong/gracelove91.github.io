--
title: JDK, JVM, JRE
date: 2019-12-23
categories:
    - java
tag
    - java
    - jvm
--



# JDK, JVM, JRE
> JDK > JRE > JVM, Library



## JDK - Java Development Kit
- JRE + 개발에 필요한 툴
- 소스코드를 작성할 때 사용하는 자바 언어는 플랫폼에 독립적이다.
- 자바 11부터는 JDK만 제공하며, JRE를 따로 제공하지는 않는다.

## JRE - Java Runtime Environment
- 자바 애플리케이션을 싱행할 수 있도록 구성된 배포판.
- JVM과 핵심라이브러리 및 자바 런타임 환경에서 사용하는 프로퍼티 셋팅이나 리소스파일을 가지고 있다. (JVM + 라이브러리)
- 개발관련 도구는 포함되지않는다. (JDK에서 제공)

## JVM - Java Virtual Machine
 - 자바 가상 머신으로 바이트코드(.class)를 OS에 특화된 코드로 변환(인터프리터와 JIT컴파일러)하여 실행한다.
	 - OS에 특화된 코드이기 때문에 특정 플랫폼에 종속적이다.
 - 바이트코드를 실행하는 표준이자 구현체다
	 - JVM자체는 표준. 구현체로는 오라클, 아마존, Azul, 레드햇 ... 등등이 있다.


참조 : > [더 자바, 코드를 조작하는 다양한 방](https://www.inflearn.com/course/the-java-code-manipulation/)


