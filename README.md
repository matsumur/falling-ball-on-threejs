# falling-ball-on-threejs

## このプロジェクトはなに？
立命館大学情報理工学部 実世界情報コースの講義、実世界情報実験3の球体落下実験のためのプロジェクトです。<a href="https://threejs.org">three.js</a>というJavascriptライブラリを利用して、物体落下のシミュレーションを行います。

## まずはどこをいじればいいの？
以下が球体の速度や位置を計算している部分です。ここをいじるとシミュレーション結果が変わります。
```
let animate = () =>  {
  delta = clock.getDelta();
  
  if(ball.position.y < 2.0 && ball_velocity.y <= 0) {
    ball_velocity.y = 0.0;
  }else{
    ball_velocity.x = 0.0;
    ball_velocity.y += GRAVITY * delta;
  }

  ball.position.x = ball.position.x;
  ball.position.y += ball_velocity.y * delta;

  requestAnimationFrame(animate);
 };
 ```

## わからないときに誰に質問したらいいの？
まずは自分でいろいろと試行錯誤して解決へのトライをしましょう。どうしてもわからなければ、作者である松村耕平か、TA/ESなどに聞いてください。

## バグがあったらどうすればいいの？
プルリクエストをお願いします。
