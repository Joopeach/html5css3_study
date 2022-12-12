# <HTML5 + CSS3 웹 표준의 정석>

## 22.12.12 (주말 10일 분... )

## Lesson 8 CSS 박스 모델
--------------------------------------
### 08-1. CSS와 박스 모델
1. 블록 레벨 요소와 인라인 레벨 요소
    * 블록 레벨 요소
        + 요소를 삽입했을 때 혼자 한 줄을 차지하는 요소
        + 요소의 너비가 100%
    * 인라인 레벨 요소
        + 줄을 차지하는 요소
        + 화면에 표시되는 콘텐츠만큼만 영역을 차지하고 나머지 공간에는 다른 요소가 올 수 있음 ex) <img> ,  <strong> 등
2. 박스 모델(Box model) - 박스 형태의 콘텐츠
    * 실제 콘텐츠 영역, 패딩(padding), 박스의 테두리(border), 그리고 마진(margin) 등의 요소로 구성됨.
    * 개발자 도구에서 박스 모델 확인 가능
3. width, height 속성 - 콘텐츠 영역의 크기
    * 실제 콘텐츠 영역의 크기 지정
        +  기본형 :: <br> width : <크기> | <백분율> | auto <br>
                    height : <크기> | <백분율> | auto
        + 속성값 ::
            - <크기> : 너비,높이 값 → px(픽셀), cm(센티미터)단위 수치로 지정
            - <백분율> : 박스 모델 포함 → 부모 요소를 기준으로 너비, 높이 값을 백분율로 지정
            - auto : 박스 모델의 너비, 높이 값 = 양에 따라 자동으로 결정 (기본 값)
    * 실제 콘텐츠 너비 계산하기
        - at 모던 브라우저 :: <br>
                박스 모델의 전체 너비 = width 값 + 좌우 패딩 + 좌우 테두리
        - at 인터넷 익스플로러6 :: <br>
                width 값 = 콘텐츠 너비 + 좌우 패딩 + 좌우 테두리                
4. display 속성 - 화면 배치 방법 결정하기 <br>
    블록 레벨 요소를 인라인 레벨 요소로 바꾸거나 인라인 레벨 요소를 블록 레벨 요소로 바꿈 <br>
    기본형 :: <br>
    display : none | contents | block | inline | inline-block | table | table-cell
    1) display:block ::
        해당요소를 블록으로 지정 <br>
        <style>
            #block img {
                display:block;
                margin:10px;
            }
        </style>  
    2) display:inline ::
        블록 레벨 요소를 인라인 레벨로 지정
    3) display:inline-block :: 요소를 인라인 레벨로 배치하면서 내용에는 블록 레벨 속성을 지정
    4) display:none ::<br>해당 요소를 화면에 표시 X<br>
                    화면에서 공간 차지 X 
    5) 기타 display 값
        - inherit : 상위 요소 display 속성 상속받음
        - table : 블록 베레의 표로 만듬
        - inline-table : 인라인 레벨의 표로 만듬 (table 태그 사용한 듯)
        - table-row : 표의 행으로 made
        - table-row-group : 표의 행 그룹으로 made
        - table-geader-group : 표 제목영역 그룹으로 made
        - table-footer-group : 표 요약 영역 그룹 made
        - table-column : 표 열로 made
        - table-column-group : 표의 열 그룹 made
        - table-cell : 표의 1개 셀로 made
        - table-caption : 표의 캡션 made
        - list-item : 목록의 항목을 can 표시.. 기본적인 블록 박스와 표시자 박스 made
--------------------------------------
### 08-2. 테두리 관련 속성들
1. border-style :: 테두리 스타일
    * 기본 값 = none → 화면 테두리 표시안됨.
    * 테두리를 그리기 위해 맨 먼저 테두리 스타일부터 지정할 것
        - 속성 값
            - none : 기본값 / 테두리 X
            - hidden : 테두리 X <br> border-collapse:collapse 일 경우 다른 테두리도 X
            - dashed : 짧은 선(직선으로 된 점선) 표시
            - dotted : 점선 표시
            - double : 이중선
            - groove : 액자처럼 조각한 듯 표시
            - inset : 창에 박혀있는 것처럼 표시
            - outset : 창에서 튀어나온 것처럼 표시
            - ridge : outset과 같음
            - solid : 실선 표시
2. border-width :: 테두리 두께
    * 기본형 :: <br>
        border-top-width: <크기> | thin | medium | thick <br>
        border-right-width: <크기> | thin | medium | thick <br>
        border-bottom-width: <크기> | thin | medium | thick <br>
        border-left-width: <크기> | thin | medium | thick <br>
        border-width: <크기> | thin | medium | thick <br>
3. border-color :: 테두리 색상
    * 기본형 :: <br>
        border-top-color : <색상> <br>
        border-right-color : <색상> <br>
        border-bottom-color : <색상> <br>
        border-left-color : <색상> <br>
        border-color : <색상> <br>
4. border :: 테두리 스타일 묶어 지정
    * 테두리 스타일과 두께, 색상 등을 묶어 표기
5. border-radius :: 박스 모서리 둥글게
    * 기본형 :: <br>
        border-top-left-radius <br>
        border-top-right-radius <br>
        border-bottom-right-radius <br>
        border-bottom-left-radius <br>
        border-radius <br>
--------------------------------------
### 08-3. 여백을 조절하는 속성
1. margin :: 요소 주변 여백
    * 현재 요소의 주변 여백
    * 마진 이용 = 요소, 요소 사이의 간격 조절
    * 속성 값
        - <크기> : 너비, 높이 값 px, cm 단위로 함께 수치지정
        - <백분율>
2. 마진 중첩(margin overlap) 현상
3. padding
    * 콘텐츠 영역 N 테두리 사이의 여백
