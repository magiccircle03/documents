# 자바스크립트 chart 라이브러리

## 목차

### 무료 라이브러리

1. ChartJS
1. D3
1. Tui 차트
1. 구글차트
1. apexcharts

## 1. ChartJS

> 인기가 많은 Javascript Chart 라이브러리로, 사용법이 편리하고 예쁘다.
> https://www.chartjs.org/

### charts

- line
- bar
- radar
- doughnut and pie
- polar area
- bubble
- scatter

### Screenshots

#### \* line chart

<img src="https://user-images.githubusercontent.com/51072198/71459233-dc977c80-27e9-11ea-96fa-134c3a8b32b6.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71460112-d4d9d700-27ed-11ea-894c-1a27cef84eb3.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71463194-f1c7d780-27f8-11ea-9eb8-0dd7f5195b2a.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71463323-5420d800-27f9-11ea-84c9-de7fa58b83f2.png
" width="49%">

- 선과 점의 색상, 모양, 두께, 상호작용 시 스타일, 툴팁 등 커스터마이징 가능
- Stacked Area Chart로 설정할 수 있음
- line chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/line.html

#### \* bar chart

<img src="https://user-images.githubusercontent.com/51072198/71459232-dc977c80-27e9-11ea-9fe3-18dde590e820.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71460169-15395500-27ee-11ea-863c-48a4c6d8c3e1.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71460002-60069d00-27ed-11ea-903a-009c0f058580.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71463415-a104ae80-27f9-11ea-967e-eebec6e12adc.png" width="49%">

- 막대의 테두리 및 배경의 색, 테두리 너비, 툴팁 등 커스터마이징 가능
- 가로 막대나 Stacked bar로 설정할 수 있음
- bar chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/bar.html

#### \* radar chart

![radar](https://user-images.githubusercontent.com/51072198/71459235-dd301300-27e9-11ea-8159-047eeef7cf05.png)

- radar chart는 두 개 이상의 다른 데이터 세트의 포인트를 비교하는 데 유용함
- 각 선과 점의 색상, 크기, 모양, 상호작용 시 스타일, 툴팁 등 커스터마이징 가능
- radar chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/radar.html

#### \* doughnut and pie chart

<img src="https://user-images.githubusercontent.com/51072198/71460274-8973f880-27ee-11ea-8167-aef93d30b404.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71459234-dc977c80-27e9-11ea-8097-1342430270de.png" width="49%">

- 각 호의 배경색, 호를 그릴 시작 각도, 테두리 굵기, 겹침 여부, 회전 애니메이션, 툴팁 등 커스터마이징 가능
- cutoutPercentage 설정 (중간에서 잘라낸 백분율, 50이면 도넛, 0이면 파이)
- doughnut and pie chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/doughnut.html

#### \* polar area chart

![polar-area](https://user-images.githubusercontent.com/51072198/71459624-bbd02680-27eb-11ea-94c0-02814238d904.png)

- pie chart와 유사하지만 값의 스케일도 표시할 수 있음
- 각 호의 배경색, 호를 그릴 시작 각도, 테두리 굵기, 겹침 여부, 회전 애니메이션, 툴팁 등 커스터마이징 가능
- polar area chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/polar.html

#### \* bubble chart

![bubble](https://user-images.githubusercontent.com/51072198/71459660-e02c0300-27eb-11ea-9187-91758483d0e0.png)

- bubble chart는 동시에 3차원 데이터를 표시하는 데 사용. 처음 두 치수로 위치가 정해지고 세번째 치수로 크기가 정해진다.
- 각 기포의 모양, 색, 테두리 두께, 회전 각도, 반경, 상호작용 시 스타일, 툴팁 등 커스터마이징 가능
- bubble chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/bubble.html

#### \* scatter chart

![scatter](https://user-images.githubusercontent.com/51072198/71459710-16698280-27ec-11ea-816c-308520e1e39a.png)

- x 축이 선형 축으로 변경된 꺾은 선형 차트를 기반으로 함.
- 꺾은 선형(line) 차트와 동일한 속성 지원 (동일한 방법으로 커스터 마이징)
- 꺾은 선형 차트(배열, 포인트 형식 모두 가능)와 달리 포인트 형식의 데이터만 허용
- scatter chart 커스터 마이징에 대한 자세한 옵션 : https://www.chartjs.org/docs/latest/charts/scatter.html

## 2. D3

> 특징 : 동적이고 interactive한 데이터 시각화를 구현하기 위한, 아주 다양한 차트를 제공
> https://d3js.org/

### charts

- line and area
- bar
- doughnut and pie chart
- calendar view
- interactive bubble chart
- maps
- wordcloud
- more charts

### Screenshots

#### \* line and area chart

<img src="https://user-images.githubusercontent.com/51072198/71465569-5b97af80-2800-11ea-9e32-ec69de5c0fb2.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71465572-5c304600-2800-11ea-84b5-6a697efb896c.jpeg" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71465714-b204ee00-2800-11ea-9ba1-dc0112af4939.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71465785-dbbe1500-2800-11ea-9d8a-407ad1bae2d4.png" width="49%">

#### \* bar chart

<img src="https://user-images.githubusercontent.com/51072198/71466084-d44b3b80-2801-11ea-8cc2-acb09e7f01da.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71466086-d4e3d200-2801-11ea-9878-3ab05bd6c212.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71466138-08bef780-2802-11ea-8679-e6d15834bd58.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71466142-09578e00-2802-11ea-96fe-5b0446679f36.png" width="49%">

#### \* doughnut and pie chart

<img src="https://user-images.githubusercontent.com/51072198/71466443-e7124000-2802-11ea-9372-73653dc76e42.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71466441-e7124000-2802-11ea-9068-804e56c718a7.png" width="49%">
<img src="https://user-images.githubusercontent.com/51072198/71466440-e679a980-2802-11ea-97b1-3a09ef8cdce6.png" width="49%">

#### \* calendar view

![calendar view](https://user-images.githubusercontent.com/51072198/71464816-18d4d800-27fe-11ea-9e18-a3d2532cc861.png)

#### \* interactive bubble chart

![interactive bubble chart](https://user-images.githubusercontent.com/51072198/71466692-aebf3180-2803-11ea-8fc1-ede956e06317.png)

#### \* maps

![maps](https://user-images.githubusercontent.com/51072198/71466775-f776ea80-2803-11ea-9761-b5e95774116c.png)

#### \* wordcloud

![스크린샷 2019-12-26 오후 5 27 57](https://user-images.githubusercontent.com/51072198/71467145-45402280-2805-11ea-902e-4dabf5c35ab8.png)

#### \* more charts

![etc1](https://user-images.githubusercontent.com/51072198/71467684-fdba9600-2806-11ea-87bf-e2711045853a.png)
![etc2](https://user-images.githubusercontent.com/51072198/71467068-f4c8c500-2804-11ea-8894-c182a89cffab.png)

- [링크](https://github.com/d3/d3/wiki/Gallery)

## 3. toast UI 차트

> nhn에서 제공하는 차트 라이브러리로, 디자인이 깔끔하며 다양한 옵션을 제공한다.

### charts

- Bar chart
- Column chart
- Line chart
- Area chart
- Bubble chart
- Pie chart
- Combo chart
- Map chart

#### \* bar chart

![bar차트1](https://image.toast.com/aaaadh/real/2018/techblog/bd47c0bc16a211e696229e1b6294fc39.png)
![bar차트2](https://image.toast.com/aaaadh/real/2018/techblog/11e47c1616a611e68d3393a3503368da.png)

#### \* Column chart

![Column](https://image.toast.com/aaaadh/real/2018/techblog/bd52486616a211e6894efc5fc07d2dfc.png)
![Column2](https://image.toast.com/aaaadh/real/2018/techblog/bd53545e16a211e6934056ef5fddb49a.png)

#### \* Line chart

![Line](https://image.toast.com/aaaadh/real/2018/techblog/bd6ea64616a211e69bf47ef1a0be24f3.png)

#### \* Area chart

![Area](https://image.toast.com/aaaadh/real/2018/techblog/bd40d91e16a211e68499cd2a77a862fb.png)

#### \* Bubble chart / pie chart

![Bubble](https://image.toast.com/aaaadh/real/2018/techblog/64c063b816ac11e69ebdb1152ee5e623.png)
![pie](https://image.toast.com/aaaadh/real/2018/techblog/64c9037e16ac11e689d7149a76c343dd.png)

#### \* Combo chart / Map chart

![Combo chart](https://image.toast.com/aaaadh/real/2018/techblog/64be95a616ac11e695d57ff9470c5eeb.png)
![Map chart](https://image.toast.com/aaaadh/real/2018/techblog/64bf03ce16ac11e688613fb4ccb11e4c.png)

### Customizing

#### 다양한 테마 적용 가능

테마를 직접 등록하고, 적용할 수 있다.

![theme](https://image.toast.com/aaaadh/real/2018/techblog/30cdc378106e11e688464a36f0bd6b63.png)

- 테마에 대한 더 자세한 사항 : https://github.com/nhn/tui.chart/wiki/theme

#### 옵션

- 데이터 포매팅  
   '1,000'(천 단위 표시), '0.00'(소수점 표시), '0001'(zero fill)과 같이 간단하게 적용할 수 있는 포맷팅 옵션 존재 (직접 포맷팅도 가능)
  ![theme](https://image.toast.com/aaaadh/real/2018/techblog/f0a7b8a8106311e69decfdec7d5f0f21.png)

- 영역을 넘어서는 가로축 라벨 개행 처리  
  회전된 글자로 인해 가독성이 좋지 못할 때, 개행 가능
  ![before](https://image.toast.com/aaaadh/real/2018/techblog/10c76150106511e69ed3260a74d40297.png)
  ![after](https://image.toast.com/aaaadh/real/2018/techblog/19132286106511e686088a59a54e900c.png)

- 다이버징(diverging) 옵션  
  diverging stacked bar chart 사용 시, 다른 차트 라이브러리와 달리 좌측 데이터를 음수처리하지 않아도 된다.

  ![인구분포](https://image.toast.com/aaaadh/real/2018/techblog/350pxUSpop2010.svg.png)

## 4. 구글차트

> 아주 많은 종류의 차트를 제공한다.
> https://developers.google.com/chart/

### charts

- Geo Chart
- Bar Chart
- Histogram
- Pie Chart
- Scatter Plot Chart
- Time Series Chart
- Combo Chart
- Area Chart
- Bubble Chart
- Timeline
- Gauge
- more charts ...

![google](https://user-images.githubusercontent.com/51072198/71467342-e4fdb080-2805-11ea-8cdc-549de3d67688.jpeg)

- 배경 색상, 투명도, 선의 굵기와 색상 등을 커스터마이징할 수 있다.
- 이 외에도 수많은 커스터마이징을 제공한다. 아래 문서에서 원하는 차트를 클릭하여 확인하자.  
  https://developers.google.com/chart/interactive/docs/gallery?hl=ko

## 5. apexcharts

> 특징 : 디자인이 깔끔하고, 인터렉티브한 차트를 만들 수 있다. 애니메이션 기능이 있으며 심플한 api로 생성, 설정할 수 있다.

### charts

- Line Chart
- Area Chart
- Column Chart
- Candlestick
- Heat Map Chart
- Pie / Donut
- Radar
- RadialBar

#### \* Line Chart

![스크린샷 2019-12-26 오후 6 27 48](https://user-images.githubusercontent.com/51072198/71469787-99e79b80-280d-11ea-89c2-09ae1c2d2e05.png)
![스크린샷 2019-12-26 오후 6 28 15](https://user-images.githubusercontent.com/51072198/71469788-99e79b80-280d-11ea-95a9-9f022e83fe02.png)

#### \* Area Chart

![Area Chart](https://user-images.githubusercontent.com/51072198/71470109-825ce280-280e-11ea-9608-42b3ef3076a9.jpeg)

#### \* Column Chart

![Column Chart](https://user-images.githubusercontent.com/51072198/71470217-cb149b80-280e-11ea-9eeb-55d96f44ce80.jpeg)

#### \* Candlestick

![Candlestick](https://user-images.githubusercontent.com/51072198/71470108-825ce280-280e-11ea-960d-00e1521fa139.jpeg)

#### \* Heat Map Chart

![Heat Map Chart](https://user-images.githubusercontent.com/51072198/71470112-82f57900-280e-11ea-918b-934cfda5684a.jpeg)

#### \* Pie / Donut

![Pie / Donut](https://user-images.githubusercontent.com/51072198/71470111-825ce280-280e-11ea-9404-cc1bb6ac32ac.jpeg)

#### \* Radar

![screencapture-apexcharts-javascript-chart-demos-radar-charts-2019-12-26-18_39_11 2](https://user-images.githubusercontent.com/51072198/71470372-49713d80-280f-11ea-9535-03a4a31ec0d2.jpeg)

#### \* RadialBar

![screencapture-apexcharts-javascript-chart-demos-radialbar-charts-2019-12-26-18_39_51 2](https://user-images.githubusercontent.com/51072198/71470371-49713d80-280f-11ea-8ed9-8cb79930dc69.jpeg)

### Customizing

- 그리드, 색상, 툴팁 등 디자인 및 테마 커스터마이징 가능
- 애니메이션, 이벤트 커스터마이징 가능
- 자세한 사항은 이곳에서 확인 : https://apexcharts.com/docs
