# API

<!-- MarkdownTOC -->

- [测试类](#测试类)
    - [整数求和](#整数求和)
    - [整数求积](#整数求积)
    - [文件上传](#文件上传)
- [定位类](#定位类)
    - [获取店铺坐标（developing）](#获取店铺坐标（developing）)
    - [三角定位](#三角定位)

<!-- /MarkdownTOC -->

**注**：坐标系原点位于左下角，x 轴向右为正方向，y 轴向上为正方向。

<a name="测试类"></a>
## 测试类

<a name="整数求和"></a>
### 整数求和

Request URI:

```
GET /api/sum
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|x|第一个整数|int|
|y|第二个整数|int|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|ans|两个整数的和|int|

Response Example:

```json
{
    "ans": 100
}
```

<a name="整数求积"></a>
### 整数求积

Request URI:

```
POST /api/product
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|x|第一个整数|int|
|y|第二个整数|int|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|ans|两个整数的积|int|

Response Example:

```json
{
    "ans": 144
}
```

<a name="文件上传"></a>
### 文件上传

Request URI:

```
POST /api/upload
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|file|文件内容（可以重复此参数从而上传多个文件）|binary|
|ext (optional)|上传文件的扩展名|string|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|files|所有上传成功的文件的 URI|json array|

Response Example:

```json
{
    "files": ["/uploaded_files/1f3758119fa34aa09afeed337b8e317c.jpeg"]
}
```

<a name="定位类"></a>
## 定位类

<a name="获取店铺坐标（developing）"></a>
### 获取店铺坐标（developing）

Request URI:

```
POST /api/shop-location
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|img|店铺照片（JPEG 格式）|JPEG image|

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|x|店铺位置横坐标|float|
|y|店铺位置纵坐标|float|

Response Example:

```json
{
    "x": 10.5,
    "y": 20.5
}
```

<a name="三角定位"></a>
### 三角定位

Request URI:

```
GET /api/positioning
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|alpha|alpha 角度值|float|
|beta|beta 角度值|float|
|x1|第一个参照物的横坐标|float|
|y1|第一个参照物的纵坐标|float|
|x2|第二个参照物的横坐标|float|
|y2|第二个参照物的纵坐标|float|
|x3|第三个参照物的横坐标|float|
|y3|第三个参照物的纵坐标|float|

[参数含义](https://github.com/GetYourLocation/Dashboard/blob/master/doc/%E5%AE%9A%E4%BD%8D%E7%AE%97%E6%B3%95%E6%B5%8B%E8%AF%95%E7%BB%93%E6%9E%9C%E6%8A%A5%E5%91%8A.md#测试)

Response Properties:

| Property | Description | Type |
|----------|-------------|------|
|x|用户位置横坐标|float|
|y|用户位置纵坐标|float|

Response Example:

```json
{
    "x": 136.35,
    "y": 230.55
}
```
