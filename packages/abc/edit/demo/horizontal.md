---
order: 1
title: 水平排列
---

一行一列表单。

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-demo',
  template: `
  <form nz-form #f="ngForm" na-edit-wrap="1" labelWidth="150">
    <na-edit label="App Key" error="请填写" optional="(选填)" optionalHelp="通过控制台-查看KEY获取" extra="额外提示信息">
      <input type="text" nz-input [(ngModel)]="i.ak" name="ak" required>
    </na-edit>
    <na-edit label="App Secret" error="请填写，最多32位">
      <input type="text" nz-input [(ngModel)]="i.sk" name="sk" required maxlength="32">
    </na-edit>
    <na-edit>
      <button nz-button nzType="primary" [disabled]="f.invalid">Save</button>
    </na-edit>
  </form>`,
})
export class DemoComponent {
  i: any = {};
}
```