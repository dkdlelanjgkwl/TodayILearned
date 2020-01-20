# Float Layout

## float tips

### [float 작동원리 link](https://youtu.be/xara4Z1b18I)

1. float으로 인해 부모요소 크기가 적용되지않을때

    - 부모요소에 overflow: hidden or auto

        부모요소에 크기는 할당가능 하나 옳바르지않은 방법

    - 형제 요소에 비어있는 div를 주고 css속성으로 clear: both

        요소의 개수가많을 경우 일일이 비어있는 div태그를주고 css 속성을 적용해야하는 문제점
    
    - 부모요소에 가상요소 선택자를 이용해서 clear: both

        요소가 많을 경우 전부 가상요소선택자로 속성을 줘야하는 문제점

    - .clearfix::after라는 css module을 만들고 부모요소             클래스에 clearfix 모듈 적용(추천)

        예시

            .clearfix::after {
                clear: both;
            }

2. 요소사이의 간격 and 요소를 감싸는 wrapper 사이 공간설정

    2.1. 예시

            html

            <main class="parent clearfix">
                <div class="child group1></div>
                <div class="child group2></div>
                ...
            </main>
            
            css
            /* parent요소 가운데정렬과 크기잡아주기 */
            .parent {
                box-sizing: border-box;
                width: 값;
                margin: 0 auto;
            }
            /* float적용된 자식요소들 만큼의 크기를 가지도록 부모요소 크기 잡아주기 실제 css에선 module화 해서 따로 빼준다 */
            .clearfix::after {
                display: block;
                content: "";
                clear: both;
            }
            /*margin과 padding으로 부모요소와 자식요소의 간격잡아주기, 부모요소의 width와 view port크기에 따라 가변 */
            .parent {
                padding: 50px 25px;
            }
            .child {
                float: left;
                height: 60vh;
                margin: 0 25px; 
            }