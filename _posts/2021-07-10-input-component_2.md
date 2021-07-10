---
layout: post
title: 입력 컴포넌트 (2)
excerpt: 입력컴포넌트. 복붙시 설정한 마스크보다 긴 문자열도 붙여넣기되는 오류 발견!!

categories: 
 - Blog

toc: true
toc_sticky: true

date: 2021-06-20
last_modified_at: 2021-06-20
---

## 개요
이전에 작성한 포스트에서 코딩을 진행하던중 붙여넣기시 mask 길이보다 더 긴 문자열이 복붙되는 현상을
수정하였다.

#
![input_result_0](/assets/images/20210710/20210710_1.png)
위 그림과 같이 입력시 마스크가 출력된다.

#
![input_result_1](/assets/images/20210710/20210710_2.png)
아래와 같이 실제 마스크보다 범위가 긴 문자열을 입력하여.

#
![input_result_2](/assets/images/20210710/20210710_3.png)
복사 붙여넣기 (CTRL + C / CTRL + V)

#
![input_result_3](/assets/images/20210710/20210710_4.png)
코드를 수정하자. maxlength만큼 자르도록 수정~!!(replace로 썻다가 왜 안되지??라며 10분가까이 헤멘 바보....)

#
![input_result_4](/assets/images/20210710/20210710_5.png)
정상출력된다

# 다음에 수정할 오류? 라기보단 개선사항
원래 의도는 카드번호나 주민번호처럼 숫자만 이루어진 특수패턴의 입력방식과 
알파벳만 입력되도록 할 예정이었다
그런데 현재는 숫자 알파벳 구별이 없다
예정은 L(10)으로 쓸 경우 문자열 10개 
LLLL-LLLL-LLLL-LLLL으로 쓸경우 문자열이 저 형태대로 나오도록
0(10)으로 쓸경우 숫자10개 등 숫자 문자를 구분하게 할 예정

![input_result_5](/assets/images/20210710/20210710_6.png)
잘들어간다...

![input_result_6](/assets/images/20210710/20210710_7.png)
심지어 값도 잘나온다