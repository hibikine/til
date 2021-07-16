# optionのdisabled selected hiddenテクニック

CSSのselectで使うoptionに

* disabled - 選択できない
* selected - 初期選択
* hidden - 選択肢が見えない

と付けとくと、「選択してください。」みたいなやつを簡単に出せる

```tsx
const Hoge = () => (
  <select>
    <option disabled selected hidden>
      Please select
    </option>
    <option>Apple</option>
    <option>Orange</option>
    <option>Grape</option>
  </select>
);
```
		