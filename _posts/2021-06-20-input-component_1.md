---
layout: post
title: 입력 컴포넌트 (1)
excerpt: Vue로 만들어진 입력 컴포넌트. 다양한 형식으로 출력 가능

categories: 
 - Blog

toc: true
toc_sticky: true

date: 2021-06-20
last_modified_at: 2021-06-20
---

## 개요
입력 컴포넌트중 jquery같은 라이브러리를 사용하면 주민번호나 전화번호 형식으로 출력이 가능하다.
그러나 중간에 1111-****-****-2222 같은 형식을 구현하려면 입력컴포넌트를 4개를 사용해야할 것이므로
한 입력 컴포넌트에서 모두 지원되도록 구현할 계획

# 1. 입력 형식
![input_result_0](/assets/images/input_result0.png)
위 그림과 같이 value엔 실제 값을 넣고 mask엔 value를 출력할 형식을 지정한다.

# 2. 출력 결과
![input_result_1](/assets/images/input_result1.png)
위 그림과 같이 입력된 값이 정상적으로 출력됨을 확인할 수 있음.

# 3. 실제 값 출력 결과
![input_result_2](/assets/images/input_result2.png)
위 그림과 같이 실제값을 확인할 수 있음