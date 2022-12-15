# <HTML5 + CSS3 웹 표준의 정석>

## 22.12.13 (주말 11일 분... )

## Lesson 9 CSS 레이아웃
--------------------------------------
### 09-1. CSS 포지셔닝과 주요 속성들
1. CSS 포지셔닝이란?
   * CSS = 웹 문서 요소를 적절히 배치하는 것

2. box-sizing 속성
    * 박스 모델 너비 값의 기준을 지정 <br>
    box-sizing : content-box | border-box
    * 속성 값 <br>
      * content-box : width 속성 값을 콘텐츠 영역 너비 값으로 사용합니다. (기본값)
      * border-box : width 속성 값을 콘텐츠 영역에 테두리까지 포함한 박스 모델 전체 너비 값으로 사용
  
3. float 속성 
   * 왼쪽 or 오른쪽으로 배치하기
   * float : left | right | none
  
4. clear 속성
    * float 속성을 무효화 시키는 속성
  
5. position 속성
   * 웹 문서 안에 요소들을 배치하기 위한 속성
   * position : static | relative | absolute | fixed
   * 속성 값 <br>
     * static : 요소를 문서의 흐름에 맞추어 배치
     * relative : 이전 요소에 자연스럽게 연결해 배치하되 위치를 지정할 수 있음
       * 자연스럽게 배치
       * 고정되어 있지 X / 다른 요소에 의해 바뀔 수 O
       * 상대적 위치 사용 / 다른요소와 조화로움
       * left or top 속성 이용 : 요소의 위치를 옮길 수 있음
     * absolute : 원하는 위치를 지정해 비치
       * 문서의 흐름과 상관X 원하는 위치에 요소 위치
       * 요소의 위치 = 가장 가까운 부모 요소 or 조상 요소 중 positon:relative인 요소
       * left, top, right, bottom 속성을 사용 = 네 모서리에서 얼마나 떨어져 있는지 지정
     * fixed : 지정한 위치에 고정해 배치 (화면에서 잘릴 수 있음)
       * 문서의 흐름 상관X 원하는 위치에 요소를 배치
       * 부모 요소가 아닌 브라우저 창 기준 <br> → 브라우저 창 왼쪽 위 꼭지점(0,0) 기준으로 좌표 계산 함
       * 브라우저 창 화면을 스크롤 하더라도 계속 같은 위치에 지정
  
6. visibility 속성
   * 요소를 보이게 하거나 보이지 않게 함
   * visibility : bisible | hidden | collapse
   * 속성 값 <br>
     * visible : 화면에 요소 표시 (기본 값)
     * hidden : 화면에서 요소 표시 X (하지만 크기는 그대로 유지, 배치에 영향을 미침)
     * collapse : 표의 행, 열, 행 그룹, 열 그룹 등에서 지정 → 서로 겹치도록 조절 <br> 그 외의 영역에서 사용 시 'hidden'처럼 됨
  
7. z-index 속성
    * 요소 쌓는 순서 정하기
    * z-index 값이 크면 값이 작은 요소보다 위에 쌓임
    * z-index 값을 명시 X = 1 부터 시작 1씩 커짐
--------------------------------------
### 09-2. 다단으로 편집하기
1. column-width : 단의 너비 고정, 다단 구성
   * column-width : <크기> | auto
   * 단의 너비를 고정해 놓고 화면 분할
   * 화면이 커지면 단의 개수가 多

2. column-count : 단의 개수 고정, 다단 구성
    * column-count : <숫자> | auto
    * 단의 개수를 먼저 정한 후 화면분할
    * 화면이 커질수록 단의 너비가 넓어짐

3. column-gap : 단과 단 사이 여백 지정

4. break-before, break-after : 특정 요소의 앞 or 뒤 에 다단 위치 지정
    * break-after : column | avoid-column
    * break-before : column | avoid-column
    * break-inside : column | avoid-column

5. column-span : 여러 단을 하나로 합
   * column-span : 1 | all
   * 속성 값 <br>
    1 = 단을 하나만 합치는 것 = 합치지 않는 것 (기본값) <br>
    all = 전체 단을 하나로 합침 (단의 일부만은 불가능)
--------------------------------------
### 09-3. 표 스타일
1. caption-side : 표 제목 위치
   * 캡션(설명글)은 기본으로 표 위쪽에 표시
   * 이 속성을 이용해 아래쪽에 표시 가능
   * catpion-side : top | bottom

2. border : 표 테두리 스타일 결정
   * 표의 바깥 테두리와 셀 테두리 모두 지정

3. border-collapse : 테두리 통합, 분리하기
   * 표 테두리와 셀 테두리를 합칠 것인지 설정
   * 속성 값 <br>
    collapse : 테두리를 하나로 합쳐 표시 <br>
    separate : 테두리를 따로 표시 (기본값)

4. border-spacing : 
    * border-collapse:separate를 사용해 셀들을 분리했을 경우, 인접한 셀 테두리 사이의 거리를 지정
    * 값이 1개 : 수평거리 & 수직 거리를 같게
    * 값이 2개 : 첫번째 값은 수평 거리, 두번째 값은 수직 거리
    * border-spacing : <크기>
5. empty-cell
   * border-collapse:separate를 사용해 셀들을 분리했을 경우, 내용이 없는 빈 셀들의 표시 여부를 지정
   * empty-calls : show | hide

6. width, height
   * 너비나 높이를 지정하지 않음 셀 안의 내용이 표시될 만큼만 표시된다.
   * width 값을 지정할 경우 padding 속성을 이용해 여백을 넣어주면 보기 좋게 꾸밀 수 있다.

7. table-layout
   * 셀 안의 내용 양에 따라 셀 너비를 변하게 할지, 고정시킬지 결정
   * table-layout : fixed | auto
   * 속성 값<br>
  fixed : 셀 너비 고정 / 셀 내용에 따라 셀의 너비가 달라지지 않음 <br>
  auto : 셀 내용에 따라 셀 의 너비 변경(기본 값)

8. text-align
   * 셀 안에서의 수평 정렬 방법
   * text-align : left | right | center

9. vertical-align
   * 셀 안에서의 수직 정렬 방법
   * vertical-align : top | bottom | middle
   * 속성값 <br>
   top : 위쪽 패딩 가장자리에 내용의 뒷부분 맞춤 <br>
   bottom : 아래쪽 패딩 가장자리에 내용이ㅡ 아랫부분 맞춤 <br>
   middle : 패딩의 중앙에 내용의 중앙을 맞춤      