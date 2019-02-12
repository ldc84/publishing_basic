# CSS

## 목차
> 1. CSS 란 ?
> 2. CSS 적용방법
> 3. CSS 선택자
> 4. 많이 쓰는 속성
> 5. CSS 상속
> 6. 미디어쿼리(반응형)
> 7. CSS3

## 1. css 란 ?

``` bash
Cascading Style Sheet
```  
웹에 대한 표현


## 2. CSS 적용방법
외부 스타일
``` html
<!-- html head 에 추가 -->
<link rel="stylesheet" href="style.css">
```

내부 스타일
``` html
<!-- html head 에 추가 -->
<style type="text/css">

</style>
```

인라인 스타일
``` html
<!-- html 태그에 직접 입력 -->
<div style="display:block; color:#666; font-size:20px;">

</div>
```


## 3. CSS 선택자
``` css
/* id */
#id {}

/* class */

.class {}

/* 태그 */
div {}

/* 가상선택자 */
a:hover {}
a:focus {}
a:active {}
a:visited {}
div:before {}
div:after {}
div:first-child {}
div:last-child {}
div:nth-child(n) {}
div:nth-child(even) {}
div:nth-child(odd) {}
div:nth-of-type(n) {}
div:not() {}
...
```


## 4. 많이 쓰는 속성
``` css
/* 기본타입 */
.selector {
  propertie:value;
}

/* 영역 */
.layout {
  display:block; /* inline / line-block / block / table / flex / grid */
  position:relative; /* relative / absolute / fixed / sticky / static(default) */
  float:left; /* left / right / none / inherit */
}

/* 여백 or 간격 */
.padding-margin {
  margin:10px;
  margin:0 auto;
  margin:0 auto 10px;
  padding:20px;
  padding-left:10px;
}

/* 컬러 */
.color {
  /* Hex */
  color:#fff;
  border-color:#111;
  background-color:#222;
  /* RGB */
  color:rgb(0,0,0);
  color:rgba(0,0,0,0.3);
}

/* 폰트 */
.font {
  font-family:'gulim', 'dotum';
  font-size:20px;
  font-weight:300;
  line-height:20px;
  letter-spacing:-1px;
  word-spacing:-1px;
  word-wrap:keep-all;
}

/* 정렬 */
.align {
  text-align:center;
  vertical-align:middle;
}

/* 다중 */
.multi {
  border:1px solid #ddd;
  background:#333 url('/images/bg.jpg') no-repeat 0 center;
  font:italic bold 12px/20px arial, sans-serif; /* 비추 */
}
```


## 5. CSS 상속
``` css
.class div {}
li li {}
```

## 6. 미디어쿼리
``` css
/* 0 ~ 767px 넓이만 적용 */
@media screen and (max-width:767px) {
  
}

/* 768px ~ 1199px 넓이만 적용 */
@media screen and (min-width:768px) and (max-width:1199px) {
  
}

/* 1200px 이상 넓이만 적용 */
@media screen and (min-width:1200px) {
  
}

/* 폰을 눕혔을때도 가능 */
@media screen and (orientation: landscape) {
  
}
```

## 7. CSS3 일부 기능
> - cross browsing issue 가 있음. 표준브라우저에선 이상없지만 ie10이하에선 일부 적용 안되는 경우가 있음.
> - transform : 회전 및 애니메이션 하기 위한 속성
> - transition 에 의한 애니메이션
> - animation : @keyframes
> - background 효과 : image / clip / attachment / blend-mode
> - etc ...