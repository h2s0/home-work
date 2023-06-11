# mission-03 과제 
### trasnsition 속성의 활용법을 복습하며 이해도를 확인하기 위한 과제물입니다.
---

<br>

- ### 완성예시와 완성본 비교
<br>

<div>완성예시</div>
<div class="left">완성본</div>

<video src="./%EC%99%84%EC%84%B1%EC%98%88%EC%8B%9C.mp4" controls title="완성예시" class="complete" autoplay muted></video>
<video src="./%EC%99%84%EC%84%B1%EB%B3%B8.mp4" controls title="완성본" class="complete" autoplay muted></video>


<style>
    .complete{
        width: 250px;
        display:inline-block;
    }

    div{
        display:inline-block;
    }

    .left{
        margin-left:200px;
    }

</style>

- ### Markup 작성

```
body > main

    > section.about-wrapper

        > h2.site-text

        > div.site-list-wrapper
            > ul.site-list
                - li>a
                - li>a
                - li>a
                - li>a
                - li>a
```
<br>

- ### transition 을 활용하여 구현해야 할 움직임 <br><br>
    1. 흰색 창의 세로값이 길어지며 리스트 목록이 보임
    2. 리스트가 아래로 내려감
    3. 마우스를 떼고 난 뒤, 흰색 창의 세로값과 제로베이스 글자가 원상태로 돌아옴

    <br>
- ### transition 속성값 활용방법 <br><br>

1. 흰색 창의 높이 값을 조절
```css
/* 흰색 창 초기값 */
.site-list-wrapper{
    width: 166px;
    background: #fff;
    border: 1px solid #A3A3A3;
    border-radius: 5px;
    overflow: hidden;
    height: 29px;
    transition: height, 800ms;
}
/* 흰색 창 hover 결과값 */
.site-list-wrapper:hover{
    height: 171px;
}
```
<br>
    2. padding-top 으로 리스트 위치 조절
<br>

```CSS
/* 리스트 목록 초기값 */
.site-list{
    overflow: hidden;
    transition: padding-top 350ms 700ms ease-in-out;
}

/* 리스트 목록 결과값 */
.site-list:hover{
    padding-top: 13px;
}
```
<br>

3. 흰색 창의 효과가 끝나기 직전 리스트 효과가 나타나기 위해 `transition-delay` 속성값 활용
<br><br>
마우스를 뗀 뒤에도 같은 효과를 주기 위해 `ease-in-out` 속성값 활용
