---
description: 咒语讲解
---

# Prompt 咒语

### 正向提示词 Prompt

正向提示词是对需要绘画的对象的描述。

优秀的咒语描述常常能带来不错的绘画效果，后面我也会讲解咒语的模版。

### 反向提示词 Negative Prompt

反向提示词是可以筛选掉不需要的画风、元素、以及错误的绘画结果。反向提示词在特定条件中非常有用。

例如在22-3月的版本，AI不太会画手和一些面部的细节，可以通过增加反向提示词将绘画错误的手以及数量不正确的手臂以及腿进行纠正。

## 提示词基本语法

### 内容性提示词

#### 人物及主题特征

* 服饰穿搭
* 发型发色
* 五官特点
* 面部表情
* 肢体动作

#### 场景特征

* 室内、室外
* 大场景
* 小细节

#### 环境光照

* 白天黑夜
* 特定时间
* 光环境
* 天空

#### 画幅视角

* 距离
* 人物比例
* 观察视角
* 镜头属性

dynamic angle 动态角度\
from above\
from below\
wide shot 广角镜头\
Aerial View 鸟瞰图&#x20;

full body shot（全身） \
cowboy shot （半身） \
close-up shot （接近）

### 标准化提示词

#### 画质提示词

* 通用高画质 best quality, ultra-detailed, masterpiece , 8K
* 特定分辨率类型（推荐） extremely detailed CG unity 8K wallpaper, unreal engine rendered

#### 画风提示词

* 插画风 illustration, painting, paintbrush
* 二次元 anime, comic, game, CG&#x20;
* 写实系 photorealistic, realistic, photograph

### 着重强调提示词

#### 括号加数字

在需要加倍强调的提示词加上括号，同时后面填写需要增加多少倍。

for instance, (white flower:1.5) 为白花的权重为原来的1.5倍（增强）。

同时也可以减弱。

#### 提升特定元素质量的方法

```Plain
extremely detailed /* 某些单词 /
beautiful detailed / 某种单词 */
```

### 反向提示词

#### 质量类型

可以在反向提示词中添加杜绝低质量的提示词，用来提升其画面的质量。

{% code overflow="wrap" %}
```
(worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality
```
{% endcode %}

#### 反单色和灰度

((monochrome), ((grayscale))

当然如果画面会变得非常灰的话，可以使用外挂VAE模型(vae-ft-mse-840000-ema-pruned)来提升亮度

#### 身体比例

bad proportions&#x20;

表示身体畸形的比例，同时该关键词可以用特定的身材比例来进行替代。

#### 错误数量和畸形的四肢

{% code overflow="wrap" %}
```
(missing arms:1.331), (extra legs:1.331), (fused fingers:1.61051), (too many fingers:1.61051), (unclear eyes:1.331), lowers, bad hands, missing fingers, extra digit,bad hands, missing fingers, (((extra arms and legs))),
```
{% endcode %}

## 模版

### 通用模版

#### 正向提示词

1. 描述人物
2. 描述场景
3. 描述环境（时间，光照）
4. 描述画幅视角
5. 其他画面元素
6. 高品质标准化
7. 画风标准化
8. 其他特殊要求、氛围装饰等

#### 反向提示词

{% code overflow="wrap" %}
```
NSFW, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((grayscale)), skin spots, acnes, skin blemishes, age spot, (ugly:1.331), (duplicate:1.331), (morbid:1.21), (mutilated:1.21), (tranny:1.331), mutated hands, (poorly drawn hands:1.5), blurry, (bad anatomy:1.21), (bad proportions:1.331), extra limbs, (disfigured:1.331), (missing arms:1.331), (extra legs:1.331), (fused fingers:1.61051), (too many fingers:1.61051), (unclear eyes:1.331), lowers, bad hands, missing fingers, extra digit,bad hands, missing fingers, (((extra arms and legs))),
```
{% endcode %}

## 常用 prompt 推荐

### 正向提示词：

| prompt               | 用途                                        |
| -------------------- | ----------------------------------------- |
| HDR, UHD, 64K        | (HDR、UHD、4K、8K和64K)这样的质量词可以带来巨大的差异提升照片的质量 |
| Highly detailed      | 画出更多详细的细节                                 |
| Studio lighting      | 添加演播室的灯光，可以为图像添加一些漂亮的纹理                   |
| Professional         | 加入该词可以大大改善图像的色彩对比和细节                      |
| Vivid Colors         | 给图片添加鲜艳的色彩，可以为你的图像增添活力                    |
| Bokeh                | 虚化模糊了背景，突出了主体，像iPhone的人像模式                |
| High resolution scan | 让你的照片具有老照片的样子赋予年代感                        |
| Sketch               | 素描                                        |
| Painting             | 绘画                                        |

### 反向提示词：

| prompt                    | 描述      |
| ------------------------- | ------- |
| mutated hands and fingers | 变异的手和手指 |
| deformed                  | 畸形的     |
| bad anatomy               | 解剖不良    |
| disfigured                | 毁容      |
| poorly drawn face         | 脸部画得不好  |
| mutated                   | 变异的     |
| extra limb                | 多余的肢体   |
| ugly                      | 丑陋      |
| poorly drawn hands        | 手部画得很差  |
| missing limb              | 缺少的肢体   |
| floating limbs            | 漂浮的四肢   |
| disconnected limbs        | 肢体不连贯   |
| malformed hands           | 畸形的手    |
| out of focus              | 脱离焦点    |
| long neck                 | 长颈      |
| long body                 | 身体长     |

### 常用艺术风格：

| 艺术风格                           | 艺术家                                                                      | 说明             |
| ------------------------------ | ------------------------------------------------------------------------ | -------------- |
| Portraits                      | Derek Gores, Miles Aldridge, Jean Baptiste-Carpeaux, Anne-Louis Girodet  | 肖像画            |
| Landscape                      | Alejandro Bursido, Jacques-Laurent Agasse, Andreas Achenbach, Cuno Amiet | 风景画            |
| Horror                         | H.R.Giger, Tim Burton, Andy Fairhurst, Zdzislaw Beksinski                | 恐怖画            |
| Anime                          | Makoto Shinkai, Katsuhiro Otomo, Masashi Kishimoto, Kentaro Miura        | 动漫画            |
| Sci-fi                         | Chesley Bonestell, Karel Thole, Jim Burns, Enki Bilal                    | 科幻画            |
| Photography                    | Ansel Adams, Ray Earnes, Peter Kemp, Ruth Bernhard                       | 摄影             |
| （Concept artists (video game)) | Emerson Tung, Shaddy Safadi, Kentaro Miura                               | 概念艺术           |
| Digital painting               | \\                                                                       | 数字艺术风格         |
| Concept art                    | \\                                                                       | 2d插画风格         |
| Ultra realistic illustration   |                                                                          | 画风真实和逼真，用于生成人物 |
