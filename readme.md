##README  
yukiokamura  
2015.12.11  
©2015 yukiokamura All Rights Reserved.   


sample view is HERE  
http://yukiokamura.tokyo/playground/#boid  

---


webページに背景として挿入したい場合は以下のコードをbody内で宣言してください。


```
<canvas id="canvas"></canvas>
```

その後自動で全画面表示になりますので、cssの方で以下のコード  

```
#canvas{
	position: absolute;
	top:0;
	left:0;
}
```

を入力します。  
ボールの色を変更したい場合は、  

```
function drawCircle(x,y){
  context.beginPath();
  context.strokeStyle = "#fff";
  context.arc(x,y,radius,0,Math.PI*2,false);
  context.stroke();
}
```

の部分のstrokeStyleで色を変更してください。  
ぬりつぶすなら上のコードを

```
function drawCircle(x,y){
  context.beginPath();
  context.fillStyle = "#fff";
  context.arc(x,y,radius,0,Math.PI*2,false);
  context.fill();
}
```

以下のように書き換えてください。