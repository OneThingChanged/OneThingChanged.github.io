---
title:  "[CS] 메모리 구조" 

categories:
  -  Computer Science
tags:
  - [Memory, Computer Science]

toc: true
toc_sticky: true

date: 2023-12-09
last_modified_at: 2023-12-09
---

## 개념

프로그램이 실행되기 위해서는 먼저 프로그램이 메모리에 로드(load)되어야 합니다.
또한, 프로그램에서 사용되는 변수들을 저장할 메모리도 필요합니다.

따라서 컴퓨터의 운영체제(OS)는 프로그램의 실행을 위해 다양한 메모리 공간을 제공하고 있습니다.
프로그램이 운영체제로부터 할당받는 대표적인 메모리 공간은 다음과 같습니다.

1. 코드(code) 영역
2. 데이터(data) 영역
3. 스택(stack) 영역
4. 힙(heap) 영역

메모리 구조는 프로그램의 실행 흐름과 데이터 관리를 위해 중요한 역할을 합니다. 이러한 구조를 이해하고 올바르게 활용하는 것은 프로그래밍 및 소프트웨어 개발에서 핵심적인 부분 중 하나입니다.

다음 그림은 운영체제가 제공하는 메모리 공간을 표현하고 있습니다.

![MemoryStructure](https://github.com/user-attachments/assets/78cf06aa-8f7a-4dd8-93ec-97cfd7866edc)

## 코드 세그먼트 (Code Segment):

- 코드 세그먼트는 프로그램의 명령어 (코드)를 저장하는 영역입니다.
- CPU는 코드 세그먼트에서 명령어를 읽어와 실행합니다.
- 코드 세그먼트는 읽기 전용(read-only)으로 설정되며, 프로그램 실행 중에 수정할 수 없습니다.



## 데이터 세그먼트 (Data Segment):

- 데이터 세그먼트는 초기화된 전역 변수와 정적 변수(static variables)를 저장하는 영역입니다.
- 이러한 변수들은 프로그램이 시작될 때 메모리에 할당되며, 프로그램 실행 중에 변경될 수 있습니다.



## 스택 메모리 (Stack Memory):

- 스택 메모리는 함수 호출 및 지역 변수(local variables)와 같은 정적인 크기의 데이터를 저장하기 위한 영역입니다.
- 스택은 함수가 호출될 때마다 호출 스택(call stack)에 프레임(frame)을 추가하고, 함수가 반환될 때 이를 제거하여 함수 호출의 상태를 관리합니다.
- 스택 메모리는 LIFO(Last-In-First-Out) 구조를 따르며, 함수 호출 및 복귀에 대한 정보를 추적하는 데 사용됩니다.



## 힙 메모리 (Heap Memory):

- 힙 메모리는 프로그램 실행 중에 동적으로 할당되고 해제되는 데이터를 저장하기 위한 영역입니다.
- 힙 메모리는 프로그래머가 필요에 따라 메모리를 동적으로 할당하고 사용할 수 있게 해주는 곳입니다. 이것은 주로 동적으로 생성된 데이터 구조 (예: 객체, 배열) 및 동적 할당된 메모리를 관리하기 위해 사용됩니다.
- 힙 메모리는 메모리 누수(memory leaks)와 같은 문제를 유발할 수 있으므로 메모리 할당과 해제에 주의가 필요합니다. 대부분의 프로그래밍 언어에서 힙 메모리를 관리하기 위한 메커니즘을 제공합니다.



<script src="https://utteranc.es/client.js"
        repo="OneThingChanged/OneThingChanged.github.io"
        issue-term="pathname"
        label="utterances"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
