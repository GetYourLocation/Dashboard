# API

<!-- MarkdownTOC -->

- [测试类](#测试类)
    - [整数求和](#整数求和)
    - [整数求积](#整数求积)
    - [文件上传](#文件上传)
    - [三角定位](#三角定位)
- [定位类](#定位类)

<!-- /MarkdownTOC -->

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
    "ans": 100
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

<a name="三角定位"></a>
### 三角定位

Request URI:

```
GET /api/localize
```

Request Parameters:

| Param | Description | Type |
|-------|-------------|------|
|alpha|alpha 值|float|
|beta|beta 值|float|
|x1|第一个参照物的横坐标|float|
|y1|第一个参照物的纵坐标|float|
|x2|第二个参照物的横坐标|float|
|y2|第二个参照物的纵坐标|float|
|x3|第三个参照物的横坐标|float|
|y3|第三个参照物的纵坐标|float|

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

<a name="定位类"></a>
## 定位类

