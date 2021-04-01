---
layout: post
title: "markdown测试"
categories: 
- blog
tags: 
- test
---

## 代码

```csharp
public class Appraisal {
  private ICollectible collectible { get; set; }
  private IGrader collectableGrader { get; set; }

  public Appraisal(ICollectable collectible, IGrader collectableGrader) {
    this.collectible = collectible;
    this.collectableGrader = collectableGrader;
  }

  public Money ComputePrice() {
    var percentageModifier = collectableGrader.Grade(collectible.condition);
    return collectible.ListPrice * percentageModifier;
  }
}
```

---

## 样式

*斜体*

**加粗**

[baidu](https://www.baidu.com)
[baidu](www.baidu.com)


---

$$
        \begin{pmatrix}
        1 & a_1 & a_1^2 & \cdots & a_1^n \\
        1 & a_2 & a_2^2 & \cdots & a_2^n \\
        \vdots & \vdots & \vdots & \ddots & \vdots \\
        1 & a_m & a_m^2 & \cdots & a_m^n \\
        \end{pmatrix}
$$

![daily](/static/daily-ui-1.png)

 It's basically ["The Personal MBA"][mba] 

[mba]: http://mdswanson.com/writeup/2012/07/25/the-personal-mba.html
