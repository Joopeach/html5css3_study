# <HTML5 + CSS3 웹 표준의 정석>

## 22.12.09

## Lesson 7 색상과 배경을 위한 스타일
--------------------------------------
### 07-1. 웹에서 색상 표현하기
1. 16진수 표기법 (ex.포토샵)
    - #ffffff 처럼 #과 함께 6자리의 16진수로 표시<br>
    - 앞에서부터 두자리씩 묶어 빨강, 초록, 파랑의 양
    - 하나도 섞이지 않을 때 = 0 <br> 가득 섞일 때 = ff
    - 000000 (검정) ~ ffffff (흰색)
    - 두자리씩 중복될 경우 줄여 사용
2. RGB/RGBA 표기법
    - color:rgb(0,0,0) 처럼 세자리의 숫자로 표시
    - 앞의 숫자부터 빨강, 초록, 파랑의 양
    - 하나도 섞이지 않을 때 = 0 <br> 가득 섞였을 때 = 255
    - 투명도를 조절할 때 color:rgba(255,0,0,.3) 처럼 마지막에 알파값 표시
    - 알파값은 불투명도를 나타내는 값으로 0~1 값 中 사용 <br> (1은 불투명 / 0은 완전 투명)
2. hsl/hsla 표기법
    - color:hsl(240, 100%, 50%) 처럼 세 자리의 숫자로 표시
    - 앞의 숫자부터 색상(hue), 채도, 밝기
    - 투명도를 조절할 때에는 hsla(240, 100%, 50%, 0.3)처럼 마지막에 알파값 표시<br> (RGBA랑 같음)
    - 알파값은 불투명도를 나타내는 값 <br> (RGBA랑 같음)
4. 색상 이름 표기법
    - 잘 알려진 색상 이름으로 표시
    - 기본 색상 16가지
    - 모든 브라우저에서 표현할 수 있는 색상 = 웹 안전 색상(web-safe color) <br> 기본 16 색상 포함해 256가지 있음
 --------------------------------------
### 07-2. 배경 색과 배경 이미지    
background-color : <색상>  <br>ex   
* background-color:#00ff00;
* background-color:rgb(0,255,0);
* background-color:green;

<br>

1. background-clip 속성 - 배경 적용 범위 조절
    - 속성값
        - border-box : 박스 모 델의 가장 외곽인 테두리까지 적용
        - padding-box : 박스 모델에서 테두리를 뺀 패딩 범위까지 적용
        - content-box : 박스 내용 부분에만 적용
2. background-image 속성 - 웹 요소에 배경 이미지 넣기
    - ex :  background-image : ul(파일경로)
3. background-repeat 속성 - 배경 이미지 반복 방법 지정
    - ex : background-repeat : repeat | repeat-x | repeat-y | no-repeat
    - 속성값
        - repeat : 브라우저 화면에 가득 찰 때까지 반복
        - repeat-x : 창 너비와 같아질 때까지 가로로 반복
        - repeat-y : 창 높이와 같아질 때까지 세로로 반복
        - no-repeat : 배경 이미지를 한 번만 표시하고 반복 X
4. background-position 속성 - 배경 이미지 위치 조절
    - ex : background-position: <수평위치> <수직 위치>; <br>
    수평위치 : left | center | right | <백분율> | <길이 값> <br>
    수직위치 : left | center | right | <백분율> | <길이 값>
        - 키워드 표시법
        - 백분율(%) 표시법
        - 길이(px) 표시법 
5. background-origin 속성 - 배경 이미지 배치할 기준 조절
    - ex : background-origin : border-box | bpadding-xog | content-box
    - 속성값
        - border-box : 박스 모델 가장 외곽 테두리가 기준
        - padding-box : 박스 모델에서 테두리를 뺀 패딩이 기준
        - content-box : 박스 모델에서 내용 부분이 기준
6. background-attachment 속성 - 배경 이미지 고정하기
    - ex) background-attachment : scroll | fixed
    - 속성 값
        - scroll : 화면 스크롤과 함께 배경이미지도 스크롤 (기본값)
        - fixed : 화면이 스크롤 되더라도 배경 이미지는 고정         
 --------------------------------------
### 07-3. 배경 색과 배경 이미지
1. 그라데이션과 브라우저 접두사
    - 그라데이션은 크기가 없는 배경 이미지이므로 background-image나 background 속성에서 사용
    - 속성은 표준화 됨
    - 하지만 구형 모던 브라우저에서는 브라우저 접두사 Need
        - ex)
        -webkit- 사파리 5.1~ 6.0 <br>
        -moz- 파이어폭스 3.6~15 <br>
        -o- 오페라 11.1~12.0
2. 선형 그러데이션
    - 수직 방향 or 수평방향으로, 혹은 대각선 방향으로 색상이 일정하게 변하는 것
    - 선형 그러데이션을 지정할 때는 방향, 색상이 Need
        - ex) linear-gradient( <각도> to <방향>, color-stop, [color-stop,..]);
    - 위 구문이 표준 구문. (브라우저 별 다름)
        * 방향
            * to top : 아래 → 위
            * to left : 오른쪽 → 왼쪽
            * to right : 왼쪽 → 오른쪽
            * to bottom : 위 → 아래로
        * 각도
            * 그러데이션이 끝나는 각도
            * 단위 = deg
        * 색상 중지 점 (color-stop)
            * 색상이 바뀌는 지점
            * 색상만 지정할 수도 있고 색상과 함께 중지 점의 위치도 지정 가능
3. 원형 그러데이션
    - 원이나 타원의 중심부터 동심원을 그리며 바깥 방향으로 색상이 바뀌는 그러데이션
    - 색상이 바뀌기 시작하는 원의 중심과 크기를 지정하고 그러데이션 모양을 지정해야 함.
    - ex) radial-gradient( <최종 모양> <크기> at <위치>, color-stop, [color-stop...])
    1. 모양
        - 원형 그러데이션에서 만들어지는 모양 : circle(원형), ellipse(타원형)
    2. 위치
        - 그러데이션이 시작하는 원의 중심 지정
        - [표준 구문] '모양'과 '크기' 속성 다음에 at 키워드와 함께 위치 값 지정
        - [접두사 구문] at 키워드 없이 구문의 맨 앞에 위치 값 지정
        - 사용할 수 있는 값 : 키워드(left, center, right 中 1, top, center, bottom 中 1)
    3. 크기 (그러데이션 원의 크기)
        - closet-side
        - closet-corner
        - farthest-side
        - farthest-corner
    4. 색상 중지점
        - 색상이 바뀌는 지점
        - 색상만 도 지정 가능, 함께 중지 점의 위치도 함께 지정 가능    