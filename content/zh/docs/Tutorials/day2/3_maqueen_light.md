---
title: "小車聲光效果"
linkTitle: "聲光效果"
slug: maqueen-light
date: 2017-01-05
weight: 3
description: >
  控制小車上的七彩LED燈與蜂鳴器
---

# 控制聲光效果

## 蜂鳴器

簡易音樂盒

接到耳機或𡃤叭

## LED

LED 的發色原理簡介與小車 LED 元件使用前的注意事項

### RGB 調色原理

RGB 指的是紅色光（Red）、綠色光（Green）與藍色光（Blue）所組成的「三原色光模式」，透過將 RGB 三種單色光按照不同比例進行合成，就可以產出各種顏色的色光。

還記得小時後上自然課，老師用一個簡單的圖案解釋所有顏色的形成嗎 ？事實上，這就是 RGB 三色原理。RGB 原理裡面的三原色就是紅色（Red）、綠色（Green）、藍色（Blue）三種顏色。稱他們為三原色是因為只要用這三種顏色，我們就可以混合出其他各種顏色。舉例來說：等量的紅色和綠色加在一起就是黃色，而等量的紅色加上藍色就是紫紅色。若是將三種顏色等量的加在一起，那就是白色了。

![](https://i.imgur.com/A6Z1h4M.png)

正如上圖所展示的，三種原色加在一起，就可以混合出各種不同的顏色。在影像的概念裡，所有的顏色就是這樣”變”出來的。

參考資料：

<a href="https://www.w3schools.com/colors/colors_picker.asp" target="_blank">HTML Color Picker</a>

<a href="https://en.wikipedia.org/wiki/Web_colors" target="_blank">Web Colors (wiki) </a>

<a href="http://csscoke.com/2015/01/01/rgb-hsl-hex/" target="_blank">RGB、HSL、Hex 網頁色彩碼，看完這篇全懂了</a>

### 色相環

![](https://i.imgur.com/Dleh2DT.png)

### 安裝 NeoPixel 擴展

要能順利使用小車上的 LED，請加入 NeoPixel 擴展，小車控制 LED 的引腳在 `P15`，LED 數量共有 4 個。

![LED extension](https://i.imgur.com/oHKqdOs.jpg)

![NeoPixel blocks](https://i.imgur.com/VNN0Ewj.png)

## 實戰 LED

### 基本控制

### 霹靂燈

### 呼吸燈

實作呼吸燈前，我們需要知道怎麼透過 HSL 色彩表示式，來控制 LED 的顏色顯示

HSL(Hue, Saturation, Lightness)色彩寫法

HSL 色彩的寫法是 HSL(色相角度但不加單位 0~360, 色彩飽和度 0~100%, 色彩亮度 0~100%)，而在括號內的色相採用的是 0~360 度，正常所見的語法就像是這樣

<h1> HSL( 240,  100%,  50% ) </h1>

色相的 0 度為 R(紅)色，120 度為 G（綠）色，240 度為 B（藍）色，為了記憶方便，先讓我把角度 0 度設定為正上方(與 CSS3 漸層相同)大家記憶比較方便點，所以以順時針方向旋轉，他們之間的角度就如同下圖所示

![](https://i.imgur.com/Dleh2DT.png)
