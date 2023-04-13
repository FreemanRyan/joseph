## Personal Page of Joseph

- 版权申明

> ------
>
> 除非在项目文件中特别注明，此项目文件内容使用 [署名-非商业性使用-相同方式共享 4.0 国际](https://creativecommons.org/licenses/by-nc-sa/4.0/) 授权发布。任何人可以自由阅读、复制、发行，或通过信息网络传播本作品，或创作演绎作品，但**必须保留作者署名（FreemanRyan）**，以及指向（https://github.com/FreemanRyan/joseph.git/）的链接 ，并**不可用于商业用途** ；若在该作品基础上进行演绎，则**必须使用相同的协议（[署名-非商业性使用-相同方式共享 4.0 国际](https://creativecommons.org/licenses/by-nc-sa/4.0/)）**进行发布。

- 每日一句API接口文档
  - 鸣谢：此接口为木头开发，其主页连接为`https://v2c.tech`; 如有侵权，请联系215147283@qq.com删除。

```Json
API 接口
我们提供了一个 API 接口，可以通过接口获得指定数量和返回值格式的内容。接口的使用方式如下所示：
基本使用：
GET https://api.lovelive.tools/api/SweetNothings
使用此方法将会返回纯文本的一句随机的内容。
高级使用：
GET https://api.lovelive.tools/api/SweetNothings/:count/Serialization/:serializationType?genderType=:genderType
GET https://api.lovelive.tools/api/SweetNothings/Serialization/:serializationType/:count?genderType=:genderType
GET https://api.lovelive.tools/api/SweetNothings/Serialization/:serializationType?genderType=:genderType
GET https://api.lovelive.tools/api/SweetNothings/:count?genderType=:genderType

Url 变量说明：
serializationType：返回内容的格式，可以选择 Text 或 Json 格式。Text 格式会根据 count 的值以换行为分隔返回内容，Json 格式会在 returnObj 中包含返回一个 Array<string>。
count：要获取的数量。如果不在 Url 中使用这个参数 ，将默认获取 1 个句子。

Query 变量说明：
genderType：内容的身份分类，可以选择 M 或 F 。M 为 “渣男”，F 为 “绿茶”。

Json 格式返回值的示例：
GET https://api.lovelive.tools/api/SweetNothings/2/Serialization/Json?genderType=M
{
  code: 200,
  message: "",
  returnObj: [
    "她再也没有对我说过晚安，我的失眠也再没好过。",
    "从遇见你的那一天起，我所走的每一步都是为了更接近你。"
  ]
}



Text 格式返回值的示例：
GET https://api.lovelive.tools/api/SweetNothings/2/Serialization/Text?genderType=F
{
  code: 200,
  message: "",
  returnObj: [
    "她再也没有对我说过晚安，我的失眠也再没好过。",
    "从遇见你的那一天起，我所走的每一步都是为了更接近你。"
  ]
}

```

