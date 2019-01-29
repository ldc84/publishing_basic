# 레이아웃 구성

## 목차
> 1. 기본구조
> 2. position
> 3. float
> 4. etc (table, flex, grid)

## 1. 기본구조

``` html
<!-- wrap -->
<div id="wrap">

  <!-- header -->
  <header>해더</header>
  <!-- //header -->

  <!-- container -->
  <div id="container">

    <!-- lnb -->
    <aside id="lnb">
      LNB
    </aside>
    <!-- //lnb -->

    <!-- contents -->
    <section id="contents">
      Contents..
    </section>
    <!-- //contents -->

  </div>
  <!-- //container -->

  <!-- footer -->
  <footer>푸터</footer>
  <!-- //footer -->

</div>
<!-- //wrap -->
```


## 2. position
``` css
#wrap {
  border:1px solid #c1c1c1;
}
header, 
footer {
  height:60px;
  background-color:yellow;
}
#container {
  position:relative;
  height:400px;
  background-color:gray;
}
#lnb {
  position:absolute;
  top:0;
  left:0;
  width:100px;
  height:100%;
  background-color:pink;
}
#contents {
  padding:0 0 0 100px;
  background-color:green;
}
```


## 3. float
``` css
#wrap {
  border:1px solid #c1c1c1;
}
header, 
footer {
  height:60px;
  background-color:yellow;
}
#container {
  height:400px;
  background-color:gray;
  overflow:hidden;
}
#lnb {
  float:left;
  width:100px;
  height:400px;
  background-color:pink;
}
#contents {
  float:left;
  width:400px;
  padding:0 0 0 100px;
  background-color:green;
}
```


## 4. etc (table, flex, grid)

### 4.1 table
table 속성과 동일하게 들어감
``` css
.parent {display:table;}
.child {display:table-cell;}
```

### 4.2 flex
요즘 가장 핫하고 쓰임새가 좋은 속성
``` css
.flex {
  display:flex;
  flex-direction:row; /* 주축 : row(default) / row-reserse / column / column-reverse */
  flex-wrap:nowrap; /* 영역지정 : nowrap(default) / wrap */
  align-items:stretch; /* 열 정렬 : stretch(default) / flex-start / flex-end / center */
  justify-content:flex-start; /* 행 정렬 : stretch(default) / flex-start / flex-end / center / space-around / space-between / space-evenly */
}
```

### 4.3 grid
정식으로 나온지 얼마 되지 않은 속성이지만 다양한 기능
``` css
.grid {
  display:grid;
  grid-template-columns: 20px repeat(6, 1fr) 20px;
  grid-auto-rows: 200px;
  grid-column-gap:30px;
  grid-row-gap: 50px;
}
.grid > div {
  border:1px dotted #999;
}

```