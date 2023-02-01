# APEX Chart





## 설치하기&#x20;

```shell
//npm
npm install --save react-apexcharts apexcharts
//yarn
yarn add apexchart 
```



```javascript
import ApexCharts from "react-apexcharts";
```

## 사용하기

```javascript

    <ApexCharts
      type="pie"
      height={"250em"}
      series={rankdata}
      options={{
        chart: {
          width: "100%",
          toolbar: {
            show: false,
          },
          background: "transparent",
          zoom: {
            enabled: false,
          },
        },
        plotOptions: {
          pie: {
            expandOnClick: true,
          },
        },
        labels: ranklabel,
        dataLabels: {
          enabled: true,
          formatter: function (val, opt) {
            if (typeof val === "string") {
              val = parseInt(val);
            }
            val = Math.round(val as number);
            return val + "%";
          },
        },
        legend: {
          labels: {
            colors: ["#fff"],
          },
        },
        title: {
          text: "검색랭킹",
          align: "center",
          style: {
            color: "#fff",
          },
        },
      }}
    />
```

쓰는 순서는 상관없지만, 가독성이 좋게 순서를 맞출려고 노력했다,

1\) 우선 타입지정을 해줘야 한다, 대표적으로  bar , pie, donut, 등이 있다.&#x20;

2\) height 과 width로  사이즈를 지정해주고, &#x20;

3\) series 는 해당 데이터가 들어가는 부분인데 , 'rankdata'  해당코드는 조회수를 배열에있는 변수다&#x20;

* pie/donut chart는 data 와 label를 넣어주는게 다른 차트들과 다른다.

```javascript
//바 차트 방법 1 
series= {[
    {
    name: "검색수"
    x : 꽃// xaxis
    y : 120// yaxis 
    }
]}
//바 차트 방법 2
const value = {x : 꽃 , y : 120} 
series= {[
    {
    name: "검색수"
    data: value }]}
//pie chart
series= {rankdata}//조화수가 들어있는 배열
label = ranklabel //이름들이 들어있는 배열 
```

4\) 그다음  option 부분인데 내용이 너무 많아 공식 문서를 참고하는게 좋다, 공식문서를 보고도 헷갈렸던 부분들만 기록

legend : ![](.gitbook/assets/image.png) graph 표시 되는 각 요소들을 보여준다&#x20;

responsive: 자체적으로 반응형을 지원하기 때문에 breakpoint 만 잘활용하면 설정하기 쉽다&#x20;

```javascript
responsive:{
    breakpoint: 1200,
    option:{
        x-axis:{},
        y-axis:{},
        }}
```

datalabel: 해당 차트에 data값을 직접 표시해준다  직접 표시되는걸 변경할수있는데 ,  pie chart 경우 직접 퍼센트로 바꿔줘서 소수점을 잘봐야하는데 , 여기서  type 오류가 많이 생겼다, 그래서 억지로 타입 지정해주었다 .

<pre class="language-javascript"><code class="lang-javascript"><strong>datalabel:{
</strong><strong>  enabled: true,//활성화
</strong>  formatter: function (val, opt) {
            if (typeof val === "string") {
              val = parseInt(val);}
            val = Math.round(val as number);
            return val + "%";
}
</code></pre>

plotoption: 차트안에 요소 plot에 대한 옵션을 해주는 부분인데 여기서 "distributed: true " 를 못찾아서 엄청난 삽질을 했다,  bar 차트에서  저 옵션을 true로 해야 각 바 마다 스타일, 색깔을 지정해줄수있다.&#x20;

```javascript
 plotOptions: {
          bar: {
            horizontal: false,
            borderRadius: 4,
            columnWidth: " 50",
            barHeight: "100%",
            distributed: true,
          },
        },
```



## 마무리

처음으로 차트를 사용해보았는데, 라이브러리를 활용하니까 확실히 편했다, 다른 차트 라이브러리 후보들로  airbnb의 visx, chart.js 등있었는데 다음 기회에 추가해보고 활용할수있으면 좋게다. 끝! &#x20;
