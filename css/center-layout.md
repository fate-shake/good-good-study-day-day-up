# 居中布局的N种方式
### 水平居中
+ 行内元素的话，设置 text-align: center; 即可
+ 块级元素的话，设置 margin：0 auto; 即可
+ 使用flex布局：justify-content：center; 即可
+ 子绝父相，transform：translate(-50%,0)即可
+ 子绝父相，left：50%;magin-left: width/2;即可
+ 子绝父相，left: 0;right: 0;margin: 0 auto;即可

### 上下居中
+ 行内元素上下居中：line-height 设置为父元素高度即可
+ 行内块级元素：vertical-align：middle；配合伪类元素
+ flex布局：align-items: center;

### 水平垂直居中
+ 行内元素：{ text-align: center; line-height: 父元素高度 }
+ flex布局：{ display: flex; justify-content: center; align-items: center; }
+ transform布局： 
   + 宽高不定：子绝父相+ child{ left: 50%;top: 50%; transform: translate(-50%,-50%) }
   + 已知宽高：子绝父相+ child{ left: 50%,top: 50%; transform: translate( -宽/2，-高/2 ) }
+ 负margin布局：子绝父相+ child{ left: 50%;top: 50%; margin-left: -宽/2，-高/2 }
+ margin布局：子绝父相+ child{ left: 0;top: 0; right: 0; bottom: 0;margin: auto; }

### 其他
还可以通过grid布局、calc计算属性布局

felx与grid 将展专门开一个文档记录

calc因性能问题用的少，只做了解

> 2019/4/30