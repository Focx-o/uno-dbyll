---
title:  "python plt default"
excerpt: "rcParams"

categories:
  - Blog
tags:
  - Blog
last_modified_at: 2022,03.03. 16:01:00
---

# 2022.03.03 <br>
[파이썬 plt 기본 설정](https://financedata.github.io/posts/faq_matplotlib_default_chart_size.html) <br>

[파이썬 matplotlib의 rcParams default 세팅하기, style 초기화하기](https://mirandaherr.tistory.com/18) <br>
[초기화 방법] <br>
1. matplotlib pkg의 import 없이도 가능한 방법: plt.style.use('default') <br>
2. matplotlib pkg로 하는 방법: plt.rcdefaults() <br>
위의 두 방법은 figure 사이즈가 변함. <br>
3. matplotlib.rcParams.update() 함수를 사용하는 방법: matplotlib.rcParams.update(matplotlib.rcParamsDefault) <br>
[rcParams 한 번에 쓰기]~~@(LSH`s library...)~~ <br>
```python
sns.set(~~~, rc = {'':~~~, '':~~~, '':~~~}, ~~~)


# 예시
sns.set(font="NanumBarunGothic", 
        rc={"axes.unicode_minus":False},
        style='darkgrid')
```
<br><br>

[Matplotlib의 구조](https://jrc-park.tistory.com/274) <br>
    ``` 
    alt + enter : 해당 줄의 code 또는 str 한 줄 위로 올리기
    ```

[기본 개념 및 용어 figure 등](https://soooprmx.com/matplotlib%EC%9D%98-%EA%B8%B0%EB%B3%B8-%EC%82%AC%EC%9A%A9%EB%B2%95-%EB%B0%8F-%EB%8B%A4%EB%A5%B8-%EC%8B%9C%EA%B0%81%ED%99%94-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC/)<br>
figure 단위는 inch, <br>
dpi는 pixel 크기 조절 <br>


[plot 자체에 대한 기본 설명](https://smartreporter3.tistory.com/m/356) <br>

[sns.set(~, rc = {~:~}, ~)](https://mingchin.tistory.com/80?category=971417) <br>

[Matplotlib 한글 폰트 사용하기](https://programmers.co.kr/learn/courses/21/lessons/950) <br>
