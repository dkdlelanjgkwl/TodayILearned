# Flex Layout

## 1. body 태그안의 native code정렬을 위해 container만들기

### 1.1. native code 수직정렬 예시

    html

    <div class="container">
        <header>...</header>
        <main>...</main>
        <footer>....</footer>
    </div>

    css

    *, ::before, ::after {
    box-sizing: border-box;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: "값";
    }

## 2. section을 나누고 싶은 구역에 flex적용하고 정렬하기

### 2.1. main 태그안에 요소들에 적용예시(수평정렬)
        
        html
        <main class="main">
            <div class="group1"></div>
            <div class="group2"></div>
            <div class="group3"></div>
        </main>

        css
        *, ::before, ::after {
        box-sizing: border-box;
        }   
        .main {
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            /* 
            단축속성
            flex: row wrap;
             */
            justify-content: space-evenly; /* padding 값에 맞춰서 알아서 요소들 사이간격 설정 */
            height: 60vh; /* .main 요소의 크기와상관없이 크기를 가지기위해 높이값 설정 */
            padding: 30px 15px;
        }

### 2.2. 수평정렬된 요소순서 컨트롤하기(order 속성)

    html
    <main class="main">
        <div class="group1"></div>
        <div class="group2"></div>
        <div class="group3"></div>
    </main>
    
    css
    *, ::before, ::after {
    box-sizing: border-box;
    }

    .group1 {
        /* 
        기본 order값은 초기값을 기준
        order: 0; (초기값)
         */
    }
    .group2 {
        order: -1;
    }
    .group3 {
        order: 1;
    }

> ### 결과 : group2 -> group1 -> group3 순서로 요소배치