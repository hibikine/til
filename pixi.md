# 2018/11/5 Pixi.js の DisplayObject に Event の名前のプロパティにコールバックを代入すると動く

```js
const sprite = new PIXI.Sprite(PIXI.Texture.fromImage(somethingImage));
sprite.interactive = true;
sprite.pointerdown = () => console.log('hoge');
sprite.pointerup = () => console.log('fuga');
sprite.touchstart = () => console.log('hogehoge');
sprite.touchend = () => console.log('fugafuga');

const app = new PIXI.Application({width: 256, height: 256});
app.stage.addChild(sprite);
document.body.appendChild(sprite.view);
```
