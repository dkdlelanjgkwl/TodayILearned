# Css Flex

>1. Container

## Display

### display: flex

    <div class="container1"></div>

    <div class="container2"></div>

각 div는 block형식으로 위에서 아래로 쌓임

### display: inline-flex

    <div class="container2"></div>

    <div class="container2"></div>
    
각 div는 inline 형식으로 좌에서 우로 쌓임

>2. Items

## Flex-flow

### flex-direction: row

container 안의 요소들을 수평으로 정렬

main-axis는 가로축을 가짐

cross-axis는 세로축을가짐

main-start는 main-axis의 시작점

main-end는 main-axis의 끝나는 부분

### flex-direction: column

container 안의 요소들을 수직으로 정렬