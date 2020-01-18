# Css Flex

## 1. Container

### 1.1. Display

#### display: flex

    <div class="container1"></div>

    <div class="container2"></div>

> 각 div는 block형식으로 위에서 아래로 쌓임

#### display: inline-flex

    <div class="container2"></div>

    <div class="container2"></div>
    
> 각 div는 inline 형식으로 좌에서 우로 쌓임

### 1.2. Flex-flow

#### flex-direction: row

> container 안의 요소들을 수평으로 정렬

- main-axis는 가로축을 가짐

- cross-axis는 세로축을가짐

- main-start는 main-axis의 시작점

- main-end는 main-axis의 끝나는 부분

#### flex-direction: column
 
> container 안의 요소들을 수직으로 정렬

- main-axis는 세로축

- cross-axis는 가로축

- main-start는 main-axis의 시작점

- main-end는 main-axis의 끝나는 부분

### 1.3. flex-wrap

#### flex-wrap: norap (기본값)

> Items를 수평정렬. 요소가 container의 크기를 벗어날경우 자동으로 width가 조정되서 한줄로 나열됨

#### flex-wrap: wrap

> Items를 수직으로 정렬. 요소가 container의 크기를 벗어날 경우 자동으로 줄바꿈됨

### 1.4. justify-content

- #### container의 main-axis를 기준으로 items를 정렬

#### justify-content: space-around;

> container > items의 모든 여백값이 균등하게 배치

#### justify-content: center;

> container의 정중앙에 item을 배치. 이때 요소들 사이에 여백은 존재하지않음

#### justify-content: flex-start;

> item이 container의 main-start지점부터 시작하여 정렬. 요소들 사이에 여백은 존재하지않는 상태로 정렬

#### justify-content: flex-end;

> item이 container의 main-end지점부터 시작하여 정렬. 요소들 사이에 여백은 존재하지않는 상태로 정렬

#### justify-content: space-between;

> item이 container의 main-start와 main-end지점에 배치되고 그사이의 item은 균일한 여백값을 가지도록 배치

### 1.5. align-content

- #### container의 cross-axis를 기준으로 items를 정렬

- #### flex-wrap: wrap; 속성을 통해 items가 여러줄(2줄이상)이고 여백이 있을 경우에만 사용가능

- ##### 만약 wrap속성을 통해 items가 묶여있다면 align-content속성을 통해 items는 한묶음으로 제어가된다.

#### align-content: strech;

> cross-axis를 채우기위해 Items의 크기를 늘림.

#### align-content: flex-start;

#### align-content: flex-end;

#### align-content: center;

#### align-content: space-between;

#### align-content: space-around;

### 1.6. align-items

- #### cross-axis를 기준으로 items를 정렬

- #### flex-wrap: nowrap; 속성을 통해 items가 한줄일 경우에만 적용

- #### 

- 아래의 value들은 align-content와 동일하다.(baseline)

#### align-items: stretch;

#### align-items: flex-start;

#### align-items: flex-end;

#### align-items: center;

#### align-items: baseline;

> items를 문자 기준선에 맞추어 정렬

## 2. Items