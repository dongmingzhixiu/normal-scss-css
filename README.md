# normal-scss-css
常用的scss-css样式，对常用的样式进行组合优化，便于快速开发HTML5应用
使用时可以减少重复样式的多次适用，比如：
## 背景色 （提供 `白色 rgba(255,255,255)`, `黑色 rgba(0,0,0)`,`基本色 rgba(64, 158, 255)`,`成功色  rgba(103, 194, 58)`,`警告色  rgba(230, 162, 60)`,`危险色 rgba(245, 108, 108)`,`信息显示色 rgba(144, 147, 153)`,每种颜色提供 透明度 0.1-1 的样式，其中基本色示例如下
```html
<!-- 基本背景色 透明度为0.9 -->
<!-- 基本背景色 样式提供透明度从0.1-0.9，以适用不同情况， -->
<div class="primarybgcolor1"></div>
<div class="primarybgcolor2"></div>
<div class="primarybgcolor3"></div>
<div class="primarybgcolor4"></div>
<div class="primarybgcolor5"></div>
<div class="primarybgcolor6"></div>
<div class="primarybgcolor7"></div>
<div class="primarybgcolor8"></div>
<div class="primarybgcolor9"></div>
<!-- 基本背景色 透明度为1 -->
<div class="primarybgcolor"></div>
```
其他颜色同上（详情查看样式文件，阅读样式文件方便您更精确的使用），样式提供简写，便于节省页面所占空间 例如基本色提供：`b-p`,透明度需要追加数字以表示透明数,如`b-p1`,透明度为0.1
## 文字颜色 （提供 `白色 rgba(255,255,255)`, `黑色 rgba(0,0,0)`,`基本色 rgba(64, 158, 255)`,`成功色  rgba(103, 194, 58)`,`警告色  rgba(230, 162, 60)`,`危险色 rgba(245, 108, 108)`,`信息显示色 rgba(144, 147, 153)`,另外添加14种rgb色由黑变白的样式,样式原文如下：（其中 ...表示引用公用变量）
```css
/**	
* 文字信息 （其中 ...表示引用公用变量）
*/
.primarycolor ,.c-p{ 	color: ...}
.successcolor ,.c-s{	color: ...}
.dangercolor  ,.c-d{	color: ...}
.warningcolor ,.c-w{	color: ...}
.infocolor    ,.c-i{	color: ...}
.whitecolor   ,.c-f{	color: ...}
.blackcolor   ,.c-b{	color: ...}

/**
 * 文字颜色,由黑到白
 */
.color ,.c {color:  rgb(0,0,0);}
.color1 ,.c1 {color: rgb(20,20,20);}
.color2 ,.c2 {color: rgb(40,40,40);}
.color3 ,.c3{color: rgb(60,60,60);}
.color4 ,.c4{color: rgb(80,80,80);}
.color5 ,.c5{color: rgb(100,100,100);}
.color6 ,.c6{color: rgb(120,120,120);}
.color7 ,.c7{color: rgb(140,140,140);}
.color8 ,.c8{color: rgb(160,160,160);}
.color9 ,.c9{color: rgb(180,180,180);}
.color10,.c10{color:rgb(200,200,200);}
.color11,.c11{color:rgb(220,220,220);}
.color12,.c12{color:rgb(240,240,240);}
.color13,.c13{color:rgb(255,255,255);}

```

## 布局 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css

/**
 * 布局
 */
.flex-start-nowarp 	,.flex-start 	,.flex-s ,.f-s	{	display: flex;	justify-content: flex-start;}
.flex-end-nowarp 	,.flex-end 		,.flex-e ,.f-e	{	display: flex;	justify-content: flex-end;}
.flex-between-nowarp,.flex-between 	,.flex-b ,.f-b	{	display: flex;	justify-content: space-between;}
.flex-center-nowarp ,.flex-center 	,.flex-c ,.f-c 	{	display: flex;	justify-content: center;}


.flex-start-warp 	, .flex-s-w , .f-s-w{	display: flex;	justify-content: flex-start;		flex-wrap: wrap;}
.flex-end-warp 		, .flex-e-w , .f-e-w{	display: flex;	justify-content: flex-end;		flex-wrap: wrap;}
.flex-between-warp 	, .flex-b-w , .f-b-w{	display: flex;	justify-content: space-between;		flex-wrap: wrap;}
.flex-center-warp 	, .flex-c-w , .f-c-w{	display: flex;	justify-content: center;		flex-wrap: wrap;}

/**
 * 布局是否拆行 
 */
.flex-warp,.warp {	flex-wrap: wrap;}
.flex-nowarp,.nowarp {	flex-wrap: nowrap;}


```
## 鼠标访问背景色（其中 ...表示引用公用变量）
```css
.primarybgcolor, .b-p {	background-color: ...!important;}
.primarybgcolor9,.b-p9 {	background-color: ...!important;}
.primarybgcolor8,.b-p8 {	background-color: ...!important;}
.primarybgcolor7,.b-p7 {	background-color: ...!important;}
.primarybgcolor6,.b-p6 {	background-color: ...!important;}
.primarybgcolor5,.b-p5 {	background-color: ...!important;}
.primarybgcolor4,.b-p4 {	background-color: ...!important;}
.primarybgcolor3,.b-p3 {	background-color: ...!important;}
.primarybgcolor2,.b-p2 {	background-color: ...!important;}
.primarybgcolor1,.b-p1 {	background-color: ...!important;}

```
## 鼠标访问字体色（其中 ...表示引用公用变量）

```css
.info-hover:hover 		,.c-h-i:hover {	color: ...;}
.danger-hover:hover 	,.c-h-d:hover	{	color: ...;}
.warning-hover:hover 	,.c-h-w:hover	{	color: ...;}
.success-hover:hover  	,.c-h-s:hover	{	color: ...;}
.primary-hover:hover 	,.c-h-p:hover	{	color: ...;}
.white-hover:hover 		,.c-h-f:hover	{	color: ...;}
.blackcolor-hover:hover ,.c-h-b:hover	{	color:...;}
```

## 内边距 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/**
 * 内边距
 */
.padding  	,.p {	padding: var(--padding);}
.padding0 	,.p0 {	padding: 0;}
.padding1 	,.p1 {	padding: var(--padding1);}
.padding2 	,.p2 {	padding: var(--padding2);}
.padding3 	,.p3 {	padding: var(--padding3);}
.padding4 	,.p4 {	padding: var(--padding4);}
.padding5 	,.p5 {	padding: var(--padding5);}
.padding6 	,.p6 {	padding: var(--padding6);}
.padding7 	,.p7 {	padding: var(--padding7);}
.padding8 	,.p8 {	padding: var(--padding8);}
.padding9 	,.p9 {	padding: var(--padding9);}
.padding10  ,.p10 {	padding: var(--padding10);}

/**
 * 访问边距内边距
 */
.padding-hover:hover  ,.p-h:hover {	padding: var(--padding);}
.padding1-hover:hover ,.p-h1:hover {	padding: var(--padding1);}
.padding2-hover:hover ,.p-h2:hover {	padding: var(--padding2);}
.padding3-hover:hover ,.p-h3:hover {	padding: var(--padding3);}
.padding4-hover:hover ,.p-h4:hover {	padding: var(--padding4);}
.padding5-hover:hover ,.p-h5:hover {	padding: var(--padding5);}
.padding6-hover:hover ,.p-h6:hover {	padding: var(--padding6);}
.padding7-hover:hover ,.p-h7:hover {	padding: var(--padding7);}
.padding8-hover:hover ,.p-h8:hover {	padding: var(--padding8);}
.padding9-hover:hover ,.p-h9:hover {	padding: var(--padding9);}
.padding10-hover:hover,.p-h10:hover  { padding: var(--padding10);}

/**
 * 内边距
 */
.padding-top  ,.p-t   {	padding-top: var(--padding);}
.padding-top0 ,.p-t0  {	padding-top:0;}.
.padding-top1 ,.p-t1  {	padding-top: var(--padding1);}
.padding-top2 ,.p-t2  {	padding-top: var(--padding2);}
.padding-top3 ,.p-t3  {	padding-top: var(--padding3);}
.padding-top4 ,.p-t4  {	padding-top: var(--padding4);}
.padding-top5 ,.p-t5  {	padding-top: var(--padding5);}
.padding-top6 ,.p-t6  {	padding-top: var(--padding6);}
.padding-top7 ,.p-t7  {	padding-top: var(--padding7);}
.padding-top8 ,.p-t8  {	padding-top: var(--padding8);}
.padding-top9 ,.p-t9  {	padding-top: var(--padding9);}
.padding-top10,.p-t10 {	padding-top: var(--padding10);}
				 
.padding-left  ,.p-l   {	padding-left: var(--padding);}
.padding-left0 ,.p-l0  {	padding-left:0;}.
.padding-left1 ,.p-l1  {	padding-left: var(--padding1);}
.padding-left2 ,.p-l2  {	padding-left: var(--padding2);}
.padding-left3 ,.p-l3  {	padding-left: var(--padding3);}
.padding-left4 ,.p-l4  {	padding-left: var(--padding4);}
.padding-left5 ,.p-l5  {	padding-left: var(--padding5);}
.padding-left6 ,.p-l6  {	padding-left: var(--padding6);}
.padding-left7 ,.p-l7  {	padding-left: var(--padding7);}
.padding-left8 ,.p-l8  {	padding-left: var(--padding8);}
.padding-left9 ,.p-l9  {	padding-left: var(--padding9);}
.padding-left10,.p-l10 {	padding-left: var(--padding10);}

.padding-right  ,.p-r   {	padding-right: var(--padding);}
.padding-right0 ,.p-r0  {	padding-right:0;}.
.padding-right1 ,.p-r1  {	padding-right: var(--padding1);}
.padding-right2 ,.p-r2  {	padding-right: var(--padding2);}
.padding-right3 ,.p-r3  {	padding-right: var(--padding3);}
.padding-right4 ,.p-r4  {	padding-right: var(--padding4);}
.padding-right5 ,.p-r5  {	padding-right: var(--padding5);}
.padding-right6 ,.p-r6  {	padding-right: var(--padding6);}
.padding-right7 ,.p-r7  {	padding-right: var(--padding7);}
.padding-right8 ,.p-r8  {	padding-right: var(--padding8);}
.padding-right9 ,.p-r9  {	padding-right: var(--padding9);}
.padding-right10,.p-r10 {	padding-right: var(--padding10);}

.padding-bottom  ,.p-b   {	padding-bottom: var(--padding);}
.padding-bottom0 ,.p-b0  {	padding-bottom:0;}.
.padding-bottom1 ,.p-b1  {	padding-bottom: var(--padding1);}
.padding-bottom2 ,.p-b2  {	padding-bottom: var(--padding2);}
.padding-bottom3 ,.p-b3  {	padding-bottom: var(--padding3);}
.padding-bottom4 ,.p-b4  {	padding-bottom: var(--padding4);}
.padding-bottom5 ,.p-b5  {	padding-bottom: var(--padding5);}
.padding-bottom6 ,.p-b6  {	padding-bottom: var(--padding6);}
.padding-bottom7 ,.p-b7  {	padding-bottom: var(--padding7);}
.padding-bottom8 ,.p-b8  {	padding-bottom: var(--padding8);}
.padding-bottom9 ,.p-b9  {	padding-bottom: var(--padding9);}
.padding-bottom10,.p-b10 {	padding-bottom: var(--padding10);}


/**
 * 两个内边距为0
 */

.padding-top-left0    ,.p-tl0{		padding-top: 0;		padding-left: 0;}
.padding-top-right0   ,.p-tr0{		padding-top: 0;		padding-right: 0;}
.padding-top-bottom0  ,.p-tb0{		padding-top: 0;		padding-bottom: 0;}
.padding-left-right0  ,.p-lr0{		padding-left: 0;	padding-right: 0;}
.padding-left-bottom0 ,.p-lb0{	padding-left: 0;	padding-bottom: 0;}
.padding-bottom-right0,.p-br0{	padding-right: 0;	padding-bottom: 0;}
/**
 * 三个内边距为0
 */

.padding-top-bottom-left0   ,.p-tbl0{	padding-top: 0;	padding-bottom: 0;	padding-left: 0;}
.padding-top-bottom-right0  ,.p-tbr0{	padding-top: 0;	padding-bottom: 0;	padding-right: 0;}
.padding-left-right-top0    ,.p-lrt0{	padding-top: 0;	padding-right: 0;	padding-left: 0;}
.padding-left-right-bottom0 ,.p-lrb0{	padding-bottom: 0;	padding-right: 0;padding-left: 0;}

```

## 外边距 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/**
 * 外边距
 */
.margin  ,.m   {	margin: var(--margin);}
.margin0 ,.m0  {	margin:0;}
.margin1 ,.m1  {	margin: var(--margin1);}
.margin2 ,.m2  {	margin: var(--margin2);}
.margin3 ,.m3  {	margin: var(--margin3);}
.margin4 ,.m4  {	margin: var(--margin4);}
.margin5 ,.m5  {	margin: var(--margin5);}
.margin6 ,.m6  {	margin: var(--margin6);}
.margin7 ,.m7  {	margin: var(--margin7);}
.margin8 ,.m8  {	margin: var(--margin8);}
.margin9 ,.m9  {	margin: var(--margin9);}
.margin10,.m10 {    margin: var(--margin10);}


/**
 * 外边距
 */
.margin-left  ,.m-l   {	margin-left: var(--margin);}
.margin-left0 ,.m-l0  {	margin-left:0;}
.margin-left1 ,.m-l1  {	margin-left: var(--margin1);}
.margin-left2 ,.m-l2  {	margin-left: var(--margin2);}
.margin-left3 ,.m-l3  {	margin-left: var(--margin3);}
.margin-left4 ,.m-l4  {	margin-left: var(--margin4);}
.margin-left5 ,.m-l5  {	margin-left: var(--margin5);}
.margin-left6 ,.m-l6  {	margin-left: var(--margin6);}
.margin-left7 ,.m-l7  {	margin-left: var(--margin7);}
.margin-left8 ,.m-l8  {	margin-left: var(--margin8);}
.margin-left9 ,.m-l9  {	margin-left: var(--margin9);}
.margin-left10,.m-l10 {  margin-left: var(--margin10);}

.margin-right  ,.m-r   {	margin-right: var(--margin);}
.margin-right0 ,.m-r0  {	margin-right:0;}
.margin-right1 ,.m-r1  {	margin-right: var(--margin1);}
.margin-right2 ,.m-r2  {	margin-right: var(--margin2);}
.margin-right3 ,.m-r3  {	margin-right: var(--margin3);}
.margin-right4 ,.m-r4  {	margin-right: var(--margin4);}
.margin-right5 ,.m-r5  {	margin-right: var(--margin5);}
.margin-right6 ,.m-r6  {	margin-right: var(--margin6);}
.margin-right7 ,.m-r7  {	margin-right: var(--margin7);}
.margin-right8 ,.m-r8  {	margin-right: var(--margin8);}
.margin-right9 ,.m-r9  {	margin-right: var(--margin9);}
.margin-right10,.m-r10 { margin-right: var(--margin10);}

.margin-top  ,.m-t   {	margin-top: var(--margin);}
.margin-top0 ,.m-t0  {	margin-top:0;}
.margin-top1 ,.m-t1  {	margin-top: var(--margin1);}
.margin-top2 ,.m-t2  {	margin-top: var(--margin2);}
.margin-top3 ,.m-t3  {	margin-top: var(--margin3);}
.margin-top4 ,.m-t4  {	margin-top: var(--margin4);}
.margin-top5 ,.m-t5  {	margin-top: var(--margin5);}
.margin-top6 ,.m-t6  {	margin-top: var(--margin6);}
.margin-top7 ,.m-t7  {	margin-top: var(--margin7);}
.margin-top8 ,.m-t8  {	margin-top: var(--margin8);}
.margin-top9 ,.m-t9  {	margin-top: var(--margin9);}
.margin-top10,.m-t10 {	margin-top: var(--margin10);}

.margin-bottom  ,.m-b   {	margin-bottom: var(--margin);}
.margin-bottom0 ,.m-b0  {	margin-bottom:0;}
.margin-bottom1 ,.m-b1  {	margin-bottom: var(--margin1);}
.margin-bottom2 ,.m-b2  {	margin-bottom: var(--margin2);}
.margin-bottom3 ,.m-b3  {	margin-bottom: var(--margin3);}
.margin-bottom4 ,.m-b4  {	margin-bottom: var(--margin4);}
.margin-bottom5 ,.m-b5  {	margin-bottom: var(--margin5);}
.margin-bottom6 ,.m-b6  {	margin-bottom: var(--margin6);}
.margin-bottom7 ,.m-b7  {	margin-bottom: var(--margin7);}
.margin-bottom8 ,.m-b8  {	margin-bottom: var(--margin8);}
.margin-bottom9 ,.m-b9  {	margin-bottom: var(--margin9);}
.margin-bottom10,.m-b10 {	margin-bottom: var(--margin10);}


/**
 * 两个外边距为0
 */

.margin-top-left0    ,.m-tl0{		margin-top: 0;		margin-left: 0;}
.margin-top-right0   ,.m-tr0{		margin-top: 0;		margin-right: 0;}
.margin-top-bottom0  ,.m-tb0{		margin-top: 0;		margin-bottom: 0;}
.margin-left-right0  ,.m-lr0{		margin-left: 0;		margin-right: 0;}
.margin-left-bottom0 ,.m-lb0{		margin-left: 0;		margin-bottom: 0;}
.margin-bottom-right0,.m-br0{	margin-right: 0;	margin-bottom: 0;}
/**
 * 三个外边距为0
 */

.margin-top-bottom-left0  ,.m-tbl0{	margin-top: 0;		margin-bottom: 0;	margin-left: 0;}
.margin-top-bottom-right0 ,.m-tbr0{	margin-top: 0;		margin-bottom: 0;	margin-right: 0;}
.margin-left-right-top0   ,.m-lrt0{	margin-top: 0;		margin-right: 0;	margin-left: 0;}
.margin-left-right-bottom0,.m-lrb0{	margin-bottom: 0;	margin-right: 0;	margin-left: 0;}

```

## 圆角 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/**
 * 圆角
 */
.radius  ,.r{	border-radius: 50%;}
.radius0 ,.r0{	border-radius: 0;}
.radius1 ,.r1{	border-radius: var(--radius1);}
.radius2 ,.r2{	border-radius: var(--radius2);}
.radius3 ,.r3{	border-radius: var(--radius3);}
.radius4 ,.r4{	border-radius: var(--radius4);}
.radius5 ,.r5{	border-radius: var(--radius5);}
.radius6 ,.r6{	border-radius: var(--radius6);}
.radius7 ,.r7{	border-radius: var(--radius7);}
.radius8 ,.r8{	border-radius: var(--radius8);}
.radius9 ,.r9{	border-radius: var(--radius9);}
.radius10,.r10{	border-radius: var(--radius10);}

```

## 宽度和高度 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/**
 * 宽度 可视宽度比例
 */

.width-vw ,.w-vw    {	width: 100vw;}
.width-vw0 ,.w-vw0  {	width: 10vw;}
.width-vw1 ,.w-vw1  {	width: 10vw;}
.width-vw2 ,.w-vw2  {	width: 20vw;}
.width-vw3 ,.w-vw3  {	width: 30vw;}
.width-vw4 ,.w-vw4  {	width: 40vw;}
.width-vw5 ,.w-vw5  {	width: 50vw;}
.width-vw6 ,.w-vw6  {	width: 60vw;}
.width-vw7 ,.w-vw7  {	width: 70vw;}
.width-vw8 ,.w-vw8  {	width: 80vw;}
.width-vw9 ,.w-vw9  {	width: 90vw;}
.width-vw10,.w-vw10 {	width: 100vw;}


/**宽度百分比*/
.width  ,.w   { width: 100%;}
.width0 ,.w0  {	width: 0;}
.width1 ,.w1  {	width: 10%;}
.width2 ,.w2  {	width: 20%;}
.width3 ,.w3  {	width: 30%;}
.width4 ,.w4  {	width: 40%;}
.width5 ,.w5  {	width: 50%;}
.width6 ,.w6  {	width: 60%;}
.width7 ,.w7  {	width: 70%;}
.width8 ,.w8  {	width: 80%;}
.width9 ,.w9  {	width: 90%;}

/**
 * 常用宽度值
 */
.width10 ,.w-10  {  width: var(--size10 );}
.width20 ,.w-20  {  width: var(--size20 );}
.width40 ,.w-40  {	width: var(--size40 );}
.width60 ,.w-60  {	width: var(--size60 );}
.width80 ,.w-80  {	width: var(--size80 );}
.width100,.w-100 {	width: var(--size100);}
.width120,.w-120 {	width: var(--size120);}
.width140,.w-140 {	width: var(--size140);}
.width160,.w-160 {	width: var(--size160);}
.width180,.w-180 {	width: var(--size180);}
.width200,.w-200 {	width: var(--size200);}
.width220,.w-220 {	width: var(--size220);}
.width240,.w-240 {	width: var(--size240);}
.width260,.w-260 {	width: var(--size260);}
.width280,.w-280 {	width: var(--size280);}
.width300,.w-300 {	width: var(--size300);}



/**
 * 高度 可视比例
 */

.height-vh  ,.h-vh   {	height: 100vh;}
.height-vh0 ,.h-vh0  {	height: 10vh;}
.height-vh1 ,.h-vh1  {	height: 10vh;}
.height-vh2 ,.h-vh2  {	height: 20vh;}
.height-vh3 ,.h-vh3  {	height: 30vh;}
.height-vh4 ,.h-vh4  {	height: 40vh;}
.height-vh5 ,.h-vh5  {	height: 50vh;}
.height-vh6 ,.h-vh6  {	height: 60vh;}
.height-vh7 ,.h-vh7  {	height: 70vh;}
.height-vh8 ,.h-vh8  {	height: 80vh;}
.height-vh9 ,.h-vh9  {	height: 90vh;}
.height-vh10,.h-vh10 {	height: 100vh;}


/**高度百分比*/
.height  ,.h   { 	height: 100%;}
.height0 ,.h0  {	height: 0;}
.height1 ,.h1  {	height: 10%;}
.height2 ,.h2  {	height: 20%;}
.height3 ,.h3  {	height: 30%;}
.height4 ,.h4  {	height: 40%;}
.height5 ,.h5  {	height: 50%;}
.height6 ,.h6  {	height: 60%;}
.height7 ,.h7  {	height: 70%;}
.height8 ,.h8  {	height: 80%;}
.height9 ,.h9  {	height: 90%;}



/**
 * 常用高度值
 */
.height10 ,.h-10  { height: var(--size10 );}
.height20 ,.h-20  { height: var(--size20 );}
.height40 ,.h-40  {	height: var(--size40 );}
.height60 ,.h-60  {	height: var(--size60 );}
.height80 ,.h-80  {	height: var(--size80 );}
.height100,.h-100 {	height: var(--size100);}
.height120,.h-120 {	height: var(--size120);}
.height140,.h-140 {	height: var(--size140);}
.height160,.h-160 {	height: var(--size160);}
.height180,.h-180 {	height: var(--size180);}
.height200,.h-200 {	height: var(--size200);}
.height220,.h-220 {	height: var(--size220);}
.height240,.h-240 {	height: var(--size240);}
.height260,.h-260 {	height: var(--size260);}
.height280,.h-280 {	height: var(--size280);}
.height300,.h-300 {	height: var(--size300);}

```

## 文字超出省略 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/****超出省略号(ellipsis)****/
.ellipsis  ,.els  {overflow: hidden;	text-overflow: ellipsis;	white-space: nowrap}
.ellipsis_2,.els2 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 2;}
.ellipsis_3,.els3 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 3;}
.ellipsis_4,.els4 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 4;}
.ellipsis_5,.els5 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 5;}
.ellipsis_6,.els6 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 6;}
.ellipsis_7,.els7 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 7;}
.ellipsis_8,.els8 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 8;}
.ellipsis_9,.els9 {	overflow: hidden;	text-overflow: ellipsis;	display: -webkit-box;	-webkit-box-orient: vertical;	-webkit-line-clamp: 9;}

```

## 字体 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
.font-size 	,.fs 	{	font-size: var(--font-size);}
.font-size14,.fs14 	{	font-size: var(--font-size14);}
.font-size15,.fs15  {	font-size: var(--font-size15);}
.font-size16,.fs16  {	font-size: var(--font-size16);}
.font-size18,.fs18  {	font-size: var(--font-size18);}
.font-size20,.fs20  {	font-size: var(--font-size20);}
.font-size22,.fs22 	{	font-size: var(--font-size22);}
.font-size24,.fs24 	{	font-size: var(--font-size24);}
.font-size26,.fs26 	{	font-size: var(--font-size26);}
.font-size28,.fs28 	{	font-size: var(--font-size28);}
.font-size30,.fs30 	{	font-size: var(--font-size30);}
.font-size32,.fs32 	{	font-size: var(--font-size32);}
.font-size36,.fs36 	{	font-size: var(--font-size36);}
.font-size38,.fs38 	{	font-size: var(--font-size38);}
.font-size40,.fs40 	{	font-size: var(--font-size40);}
.font-size52,.fs52 	{	font-size: var(--font-size52);}


.font-weigth-bold,.fs-w-b{	font-weight: bold;}
.font-weigth-normal,.fs-w-n{	font-weight: normal;}

```

## 文字位置 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
/**
 * 文字位置
 */
.text-left 		,.t-l {	text-align: left!important;}
.text-right 	,.t-r {	text-align: right!important;}
.text-center 	,.t-c {	text-align: center!important;}

```

## 文字引用提示标签 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css

.success-tip,.tip-s {	border-left: var(--size10)  solid var(--successcolor)!important;	text-align: left;	padding: var(--size10) ;}
.primary-tip,.tip-p {	border-left: var(--size10)  solid var(--primarycolor)!important;	text-align: left;	padding: var(--size10) ;}
.warning-tip,.tip-w {	border-left: var(--size10)  solid var(--warningcolor)!important;	text-align: left;	padding: var(--size10) ;}
.info-tip   ,.tip-i {	border-left: var(--size10)  solid var(--infocolor)!important;	text-align: left;	padding: var(--size10) ;}
.danger-tip ,.tip-d {	border-left: var(--size10)  solid var(--dangercolor)!important;	text-align: left;	padding: var(--size10) ;}
```

## box-sizing调整模型布局 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css
.border-box,.box-b {	box-sizing: border-box;}
/*为元素指定的任何内边距和边框都将在已设定的宽度和高度内进行绘制*/
.content-box,.box-c {	box-sizing: content-box;}
/*//规定应从父元素继承 box-sizing 属性的值。*/
.inherit-box,.box-i {	box-sizing: inherit;}
```

## 边框 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css

.border-efefef  ,.bor-ef{	border:var(--size1) solid #efefef!important;}
.border-ffffff  ,.bor-ff{	border:var(--size1) solid #ffffff!important;}
.border-success ,.bor-s{	border:var(--size1) solid var(--successcolor)!important;}
.border-danger  ,.bor-d{	border:var(--size1) solid var(--dangercolor)!important;}
.border-primary ,.bor-p{	border:var(--size1) solid var(--primarycolor)!important;}
.border-warning ,.bor-w{	border:var(--size1) solid var(--warningcolor)!important;}
.border-info    ,.bor-i{	border:var(--size1) solid var(--infocolor)!important;}

/**
 * 边框
 */


.border-width0 			,.bor-0 	{ 				border-top-width:0 !important ;	border-bottom-width:0 !important ;	border-left-width:0 !important ;	border-right-width:0 !important ;}
.border-top-width0 		,.bor-t0 	{	border: 0;	border-top-width:0 !important ;}
.border-bottom-width0 	,.bor-b0 	{	border: 0;	border-bottom-width:0 !important ;}
.border-left-width0 	,.bor-l0 	{	border: 0;	border-left-width:0 !important ;}
.border-right-width0 	,.bor-r0 	{	border: 0;	border-right-width:0 !important ;}

.border-width 			,.bor-1		{  				border-top-width:var(--size1) !important ;	border-bottom-width:var(--size1) !important ;border-left-width:var(--size1) !important ;	border-right-width:var(--size1)  !important ;}
.border-top-width 		,.bor-t1 	{	border: 0;	border-top-width:var(--size1)  	!important	;}
.border-bottom-width 	,.bor-b1 	{	border: 0;	border-bottom-width:var(--size1)!important ;}
.border-left-width 		,.bor-l1 	{	border: 0;	border-left-width:var(--size1)  !important	;}
.border-right-width 	,.bor-r1 	{	border: 0;	border-right-width:var(--size1) !important;}

.border-width2 			,.bor-2		{ 	border-top-width:var(--size2) !important;	border-bottom-width:var(--size2) !important;	border-left-width:var(--size2)  !important;	border-right-width:var(--size2) !important ;}
.border-top-width2 		,.bor-t2 	{	border: 0;	border-top-width:var(--size2)  !important;}
.border-bottom-width2 	,.bor-b2 	{	border: 0;	border-bottom-width:var(--size2) !important ;}
.border-left-width2 	,.bor-l2 	{	border: 0;	border-left-width:var(--size2) !important ;}
.border-right-width2 	,.bor-r2 	{	border: 0;	border-right-width:var(--size2) !important ;}

.border-width3 			,.bor-3		{ 	border-top-width:var(--size3) !important;	border-bottom-width:var(--size3) !important ;	border-left-width:var(--size3)  !important;	border-right-width:var(--size3)  !important;}
.border-top-width3 		,.bor-t3 	{	border: 0;	border-top-width:var(--size3) !important ;}
.border-bottom-width3 	,.bor-b3 	{	border: 0;	border-bottom-width:var(--size3) !important ;}
.border-left-width3 	,.bor-l3 	{	border: 0;	border-left-width:var(--size3)  !important;}
.border-right-width3 	,.bor-r3 	{	border: 0;	border-right-width:var(--size3) !important ;}

.border-width4 			,.bor-4		{ 	border-top-width:var(--size4) !important;	border-bottom-width:var(--size4)  !important;	border-left-width:var(--size4) !important ;	border-right-width:var(--size4) !important ;}
.border-top-width4 		,.bor-t4 	{	border: 0;	border-top-width:var(--size4) !important ;}
.border-bottom-width4 	,.bor-b4 	{	border: 0;	border-bottom-width:var(--size4) !important ;}
.border-left-width4 	,.bor-l4 	{	border: 0;	border-left-width:var(--size4) !important ;}
.border-right-width4 	,.bor-r4 	{	border: 0;	border-right-width:var(--size4) !important ;}

.border-width5 			,.bor-5		{ 	border-top-width:var(--size5) !important;	border-bottom-width:var(--size5)  !important;	border-left-width:var(--size5) !important ;	border-right-width:var(--size5) !important ;}
.border-top-width5 		,.bor-t5 	{	border: 0;	border-top-width:var(--size5) !important ;}
.border-bottom-width5 	,.bor-b5 	{	border: 0;	border-bottom-width:var(--size5) !important ;}
.border-left-width5 	,.bor-l5 	{	border: 0;	border-left-width:var(--size5) !important ;}
.border-right-width5 	,.bor-r5 	{	border: 0;	border-right-width:var(--size5) !important ;}

/**
 * 边框颜色
 */
.border-color-primary 			,.bor-c-p 		{	border-color: 		var(--primarycolor)!important ;}
.border-color-top-primary		,.bor-c-t-p 	{	border-top-color: 	var(--primarycolor)!important  ;}
.border-color-bottom-primary	,.bor-c-b-p 	{	border-bottom-color:var(--primarycolor)!important  ;}
.border-color-left-primary		,.bor-c-l-p 	{	border-left-color: 	var(--primarycolor)!important  ;}
.border-color-right-primary		,.bor-c-r-p 	{	border-right-color: var(--primarycolor)!important  ;}
.border-color-success 			,.bor-c-s 	 	{	border-color: 		var(--successcolor)!important  ;}
.border-color-top-success		,.bor-c-t-s  	{	border-top-color: 	var(--successcolor)!important  ;}
.border-color-bottom-success	,.bor-c-b-s  	{	border-bottom-color:var(--successcolor)!important  ;}
.border-color-left-success		,.bor-c-l-s  	{	border-left-color: 	var(--successcolor)!important  ;}
.border-color-right-success		,.bor-c-r-s  	{	border-right-color: var(--successcolor)!important  ;}
.border-color-warning 			,.bor-c-w 	 	{	border-color: 		var(--warningcolor)!important  ;}
.border-color-top-warning		,.bor-c-t-w  	{	border-top-color: 	var(--warningcolor)!important  ;}
.border-color-bottom-warning	,.bor-c-b-w  	{	border-bottom-color:var(--warningcolor)!important  ;}
.border-color-left-warning		,.bor-c-l-w  	{	border-left-color: 	var(--warningcolor)!important  ;}
.border-color-right-warning		,.bor-c-r-w  	{	border-right-color: var(--warningcolor)!important  ;}
.border-color-info 				,.bor-c-i 	 	{	border-color: 		var(--infocolor)!important  ;}
.border-color-top-info			,.bor-c-t-i  	{	border-top-color: 	var(--infocolor)!important  ;}
.border-color-bottom-info		,.bor-c-b-i  	{	border-bottom-color:var(--infocolor)!important  ;}
.border-color-left-info			,.bor-c-l-i  	{	border-left-color: 	var(--infocolor)!important  ;}
.border-color-right-info		,.bor-c-r-i  	{	border-right-color: var(--infocolor)!important  ;}
.border-color-danger			,.bor-c-d 	 	{	border-color: 		var(--dangercolor)!important  ;}
.border-color-top-danger		,.bor-c-t-d  	{	border-top-color: 	var(--dangercolor)!important  ;}
.border-color-bottom-danger		,.bor-c-b-d  	{	border-bottom-color:var(--dangercolor)!important  ;}
.border-color-left-danger		,.bor-c-l-d  	{	border-left-color: 	var(--dangercolor)!important  ;}
.border-color-right-danger		,.bor-c-r-d  	{	border-right-color: var(--dangercolor)!important  ;}
.border-color-efefef			,.bor-c-ef 		{	border-color: 		 #efefef!important ;}
.border-color-top-efefef		,.bor-c-t-ef  	{	border-top-color: 	 #efefef!important ;}
.border-color-bottom-efefef		,.bor-c-b-ef  	{	border-bottom-color: #efefef!important ;}
.border-color-left-efefef		,.bor-c-l-ef  	{	border-left-color: 	 #efefef!important ;}
.border-color-right-efefef		,.bor-c-r-ef  	{	border-right-color:  #efefef!important ;}
.border-color-ffffff			,.bor-c-ff 		{	border-color: 		 #ffffff!important ;}
.border-color-top-ffffff		,.bor-c-t-ff  	{	border-top-color: 	 #ffffff!important ;}
.border-color-bottom-ffffff		,.bor-c-b-ff  	{	border-bottom-color: #ffffff!important ;}
.border-color-left-ffffff		,.bor-c-l-ff  	{	border-left-color: 	 #ffffff!important ;}
.border-color-right-ffffff		,.bor-c-r-ff  	{	border-right-color:  #ffffff!important ;}



.border-style 			,.bor-s-sol 	{border-style: solid;}
.border-style-none 		,.bor-s-non		{border-style:none;}
.border-style-hidden 	,.bor-s-hid		{border-style:hidden;}
.border-style-dotted 	,.bor-s-dot		{border-style:dotted;}
.border-style-dashed 	,.bor-s-das		{border-style:dashed;}
.border-style-solid 	,.bor-s-sol		{border-style:solid;}
.border-style-double 	,.bor-s-dou		{border-style:double;}
.border-style-groove 	,.bor-s-gro		{border-style:groove;}
.border-style-ridge 	,.bor-s-rid		{border-style:ridge;}
.border-style-inset 	,.bor-s-ins		{border-style:inset;}
.border-style-outset 	,.bor-s-out		{border-style:outset;}
.border-style-inherit 	,.bor-s-inh		{border-style:inherit;}

```

## 内容溢出处理 [ 其中`var(...)`在不同文件中有不同的表现形式，在css中表现为`var(...)`，在scss中表现为`$...`   ]
```css

/*内容溢出处理*/
.overflow-hidden 	,.over-h 	{	overflow: hidden;}
.overflow-hidden-y 	,.over-h-y 	{	overflow-y: hidden;}
.overflow-hidden-x 	,.over-h-x 	{	overflow-x: hidden;}
.overflow-auto 		,.over-a 	{	overflow: auto;}
.overflow-auto-y 	,.over-a-y 	{	overflow-y: auto;}
.overflow-auto-x 	,.over-a-x 	{	overflow-x: auto;}

```
## 其他样式，
以上内容具体参考样式文件为准







