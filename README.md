# pcbless.com Redirect

极简静态站，唯一职责：把属于供应商的所有流量永久重定向到主站。

```
pcbless.com/*       ->  https://www.pcb-less.com/*   [301]
www.pcbless.com/*   ->  https://www.pcb-less.com/*   [301]
```

由 Netlify 托管，重定向规则写在根目录下的 `_redirects`，`:splat` 会保留原路径与查询参数。
`index.html` 只是兜底页（规则未命中时显示），带 meta refresh 且 `canonical` 指向主域。

主站仓库：[Semiment/pcb-less-website](https://github.com/Semiment/pcb-less-website)
