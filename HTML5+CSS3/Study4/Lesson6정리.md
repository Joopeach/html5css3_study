<HTML5 + CSS3 웹 표준의 정석>

- 22.12.07

Lesson 6 텍스트 관련 스타일

06-1. 글꼴 관련 스타일
    font-family 속성 - 글꼴 지정하기)
        ● 웹 문서에서 사용할 글꼴
        ● <body> 태그, <p> 태그, <hn> 태그 => 텍스트를 사용하는 요소들에서 use
        ● 웹문서 內 둘 이상의 글꼴을 지정할 때는 쉼표 , use
        ● font-family 속성은 상속 O <body> 태그 內 한 번 정의 -> 문서 전체 적용
        ● 부모 요소와 diffrent 글꼴 사용하고 싶을 때 -> 태그 스타일이나 클래스 스타일을 use 다른글꼴 정의
    ex) 기본형 :: font-family:<글꼴 이름>[,<글꼴 이름>,<글꼴 이름>]
        p {font-family:굴림;}

    @font-face 속성
        ● 웹 폰트(Web font) : 웹 문서 內 글꼴 정보 함께 SAVE -> 사용자가 웹 문서 접속 시 글꼴 사용자 시스템으로 다운로드 시켜 사용
        ● 사용자 시스템에 없는 글꼴이더라도 웹 제작자가 의도한 대로 표시

    font-size 속성
        ● 글자 크기를 조절하는 속성
        ● 사용할 수 있는 값 : 절대크기, 상대크기, 숫자, 백분율
        ● 기본 값 = 상대크기 medium
        ● font-size는 상속 됨
    ex) 기본형 :; font-size: <절대크기>|<상대크기>|<크기>|<백분율>

    <크기>값에서 사용하는 단위
        em = 해당 글꼴의 대문자 M의 너비를 기준으로 크기 조절
        ex = x-height(엑스 하이트). 해당 글꼴의 소문자 x의 높이를 기준으로 크기를 조절
        px = 픽셀. 모니터에 따라 상대적 크기
        pt = 포인트. 일반 문서에서 많이 사용하는 단위

    font-weight 속성 - 글자 굵기 지정하기)
        normal =  일반적인 형태 기본 값 (400)
        bold|lighter|bolder = 굵게|원래 굵기보다 더 가늘게|원래 굵기보다 더 굵게
        100~900 사이의 수치 : 400 normal, 700 bold
    
    font-variant 속성 - 작은 대문자로 표시하기

    font-style 속성
        normal = 일반적인 형태
        italic = 이탤릭체로 표시 (기울어진 글꼴이 처음부터 디자인)
        oblique = 이탤릭체로 표시 (원래 글꼴을 기울어지게 표시)

    font 속성
        하나하나 소스 줄에 넣으면 길어지므로,,, font 속성을 이용하면 한꺼번에 묶을 수 있다!!!

06-2. 텍스트 스타일
    color 속성 : 글자색
        ● 글자 색 지정
        ● 16진수 값, rgb값, hsl 값 색상 이름 중에서 use
            ex) <style>
                    h1 {color:rgb(0,200,0);} /* rgb 값 사용 - 녹색 계열 */
                    h2 {color:blue;} /* 색상 이름 */
                    .accent {color:#ff0000;} /* 16진수 사용 - 빨강 */
                </style>
   
    text-decoration 속성 : 텍스트에 줄 표시/ 없애기 
        ex) 기본형 : text-decoration : none | underline | overline | line-through
        none - 밑을 표시 X
        underline - 밑줄
        overline - 영역 위로 줄
        line-through - 영역을 가로지르는 선 (취소 선) 
   
    text-transform 속성 : 텍스트 대. 소문자 변환
        ex) text-transform : none | capitalize | uppercase | lowercase | full-width
        none - 변환 X
        capitalize - 시작 첫 글자 대문자 변환
        uppercase - 모든 글자 대문자
        lowercase - 모든글자 소문자
        full-width - 가능한 모든 문자를 전각 문자로

    text-shadow 속성 : 텍스트에 그림자 효과

    white-space 속성 : 공백 처리

    letter-spacing & word-spacing 속성 : 텍스트 간격 조절
        ● letter-spacing : 글자 사이 간격
        ● word-spacing : 단어와 단어 사이 간격

06-3. 문단 스타일
    direction 속성 : 글자 쓰기 방향 지정
        ltr : 왼쪽에서 오른쪽으로 left-to-right
        rtl : 오른쪽에서 왼쪽으로 right-to-left

    text-align 속성 : 텍스트 정렬
        start : 현재 텍스트 줄의 시작 위치에 맞춰 문단정렬
        end : 현재 텍스트 끝 위치에 맞추어 문단 정렬
        left : 왼쪽에 맞춰 문단 정렬
        right : 오른쪽에 맞춤
        center : 가운데에 맞춤
        justify : 양쪽에 맞춤
        match-parent : 부모 요소에 따라 맞춤

    text-justify 속성 : 정렬 시 공백 조절
        auto : 웹 브라우저에서 자동 지정
        none : 정렬 x
        inter-word : 단어 사이의 공백을 조절해 정렬
        distribute 인접한 글자 사이의 공백을 똑같이 맞추어 정렬

    text-indent 속성 : 텍스트 들여쓰기
        <크기> : 단위와 함께 들여 쓸 크기 지정
        <백분율> : 부모 요소의 너비를 기준으로 상대적 크기를 지정

    line-height 속성 : 줄 간격 조절
        ex) line-height : normal | <숫자> | <크기> | <백분율> | inherit

    text-overflow 속성 : 넘치는 텍스트 표기하기
        clip : 넘치는 텍스트를 자른다
        ellipsis : 말 줄임표로 잘린 텍스트가 있다고 표시    

06-4. 목록 스타일
    list-style-type 속성 : 목록의 불릿과 번호 스타일 지정
    ex) list-sytle-type : none | <순서 없는 목록의 불릿> | <순서 목록의 번호>

    1) 순서 없는 목록에서 불릿 모양 바꾸기
        disc(●) : 채운 원
        circle(○) : 빈 원
        square(■) : 채운 사각형
        none : 불릿 X
    2) 순서 없는 목록에서 불릿 없애기
        ul { list-style-type:none;}
    3) 순서 목록에서 숫자 바꾸기
        decimal : 1로 시작하는 십진수                   1, 2, 3, 4 ...
        decimal-leading-zero : 앞에 0이 붙는 십진수     01, 02, 03, 04 ...
        lower-roman : 소문자 로마 숫자
        upper-roman : 대문자 로마 숫자
        lower-alpha , lower-latin : 소문자 알파벳
        upper-alpha , upper-latin : 대문자 알파벳
        armenian : 아르메니아 숫자
        georgian : 조지 왕조시대의 숫자
    4) list-tyle-image 속성 : 불릿 대신 이미지 넣기
        ex) list-style-image : <이미지> | none
            <이미지> = url (이미지 파일 경로)
    5) list-style-position 속성 : 목록에 들여쓰는 효과
    6) list-tyle 속성 : 목록 속성 한꺼번에 표시            
        


