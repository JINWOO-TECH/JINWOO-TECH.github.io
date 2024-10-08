---
layout: post
title: Github 블로그 만들기 (markdown 문법)
description: >
  이미지 추가, 코드 박스, 글 크기 등등
categories: github_blog
tags: github_블로그_만들기_공통
---


> 이번에는 이미지 추가, 코드 박스, 글 크기 등등 페이지를 만들 때 사용하는 markdown 문법들에 대해 소개하겠습니다.

<br>

<h2>
    <span class = "jjw_h2_style">1. Text 수정 </span>
</h2>


<table id="rwd-table">
  <tbody>
    <tr>
        <td data-label="markdown (설명)" style="background-color: lightblue;">적용예</td>
        <td data-label="**text** (굵게)" class="markdown-cell">**text**</td>
        <td data-label="*text* (기울게)" class="markdown-cell">*text*</td>
        <td data-label="~~text~~ (취소선)" class="markdown-cell">~~text~~</td>
        <td data-label="<ins>text</ins> (밑줄)"><ins>text</ins></td>
        <td data-label="A<sup>text</sup> (윗첨자)">A<sup>text</sup></td>
        <td data-label="A<sub>text</sub> (아래첨자)">A<sub>text</sub></td>
    </tr>
  </tbody>
</table>

<h2>
    <span class = "jjw_h2_style">2. 제목 headers </span>
</h2>

`#` 으로 시작하여 `#` 이 늘어날때마다 제목의 수준은 내려 감

<table id="rwd-table">
  <tbody>
    <tr>
        <td data-label="markdown" style="background-color: lightblue;">적용예</td>
        <td data-label="#h1" class="markdown-cell">#h1</td>
        <td data-label="##h2" class="markdown-cell">##h2</td>
        <td data-label="###h3" class="markdown-cell">###h3</td>
        <td data-label="####h4" class="markdown-cell">####h4</td>
        <td data-label="#####h5" class="markdown-cell">#####h5</td>
        <td data-label="######h6" class="markdown-cell">######h6</td>
    </tr>
  </tbody>
</table>


<h2>
    <span class = "jjw_h2_style">3. Code 박스  </span>
</h2>


`~~~` 또는 <span style="color: red;" >```</span>  -> 코드 첫줄과 마지막 줄에 삽입

~~~
~~~ㅤ
code 박스
~~~ㅤ
~~~

~~~
code 박스
~~~

또한 언어 별 문법 하이라이트를 할 수 있습니다
`~~~` 또는 <span style="color: red;" >```</span> 첫줄에 언어를 입력해주세요

~~~
~~~python
a = "hello word"
print(a)
~~~ㅤ
~~~

~~~python
a = "hello word"
print(a)
~~~

<h2>
    <span class = "jjw_h2_style">4. 인용문  </span>
</h2>

~~~
> 인용문1 
>> 인용문2
>>> 인용문2
~~~

> 인용문1
> > 인용문2
>>> 인용문2


<h2>
    <span class = "jjw_h2_style">5. 리스트  </span>
</h2>


#### 5-1. 순서없는 리스트는 `*` 를 첫번째에 삽입 <br>

~~~
* number1
* number2
* number3
~~~

적용예)  <br>
* number1 
* number2
* number2

<br>

#### 5-2. 순서있는 리스트는 `번호.` 를 삽입 <br>

~~~
1. number1
2. number2
3. number3
~~~

적용예)  <br>
1. number1 
2. number2
3. number3

<br>

<h2>
    <span class = "jjw_h2_style">6. 테이블   </span>
</h2>


아래와 같이 사용
~~~
| column1 | column2      | column2     |
|:--------|:-------------|:------------|
| a       | 1            | 3           |
| b       | 2            | 4           |
| c       | 3            | 5           |
|==========| ===========  |===========|
| total   | 6            | 12          |
~~~

| column1 | column2      | column2     |
|:--------|:-------------|:------------|
| a       | 1            | 3           |
| b       | 2            | 4           |
| c       | 3            | 5           |
|==========| ===========  |===========|
| total   | 6            | 12          |

<br><br>

<h2>
    <span class = "jjw_h2_style">7. 수평선   </span>
</h2>


`-` , `*`, `_`   3개 이상 작성

~~~
---
***
___
~~~

적용예)  <br>

---

***

___

잘은 안보이지만 생겼습니다


<h2>
    <span class = "jjw_h2_style">8. 이미지 삽입   </span>
</h2>



저는 assets/imgaes/폴더명 으로 폴더 하나를 생성해서 이미지를 관리하고 있습니다. 아래와 같이 입력하시면 이미지를 가져올 수 있습니다. <br>
`![Xixia](/assets/images/{폴더명}/{이미지이름}.png)`

![Xixia](/assets/images/preview-small.png)

<script>
    document.addEventListener("DOMContentLoaded", function() {
        // 모든 .markdown-cell 요소를 선택합니다.
        var cells = document.querySelectorAll('.markdown-cell');
        
        cells.forEach(function(cell) {
            // 각 셀의 내용을 마크다운으로 변환하고 HTML을 설정합니다.
            cell.innerHTML = marked(cell.innerText);
        });
    });
</script>