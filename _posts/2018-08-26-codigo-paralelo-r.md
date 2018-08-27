---
layout: post
title: "Implementando códigos paralelos em R..."
subtitle: "... não é tão complicado"
image: /img/nate-grant-346782-unsplash.jpg
tags: [R, paralelo, foreach, doMC]
---

Não é tão complicado....

```r
library(foreach)
library(doMC)
registerDoMC(4)
resultado = foreach(i=1:10, .combine=c) %dopar% {
  i^2
}
```

Teste....
