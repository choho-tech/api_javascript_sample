# 朝厚云服务JavaScript调用示例

请注意： 本份代码仅供在Node.js下的编程参考。不要将朝厚云服务API调用写入浏览器前端代码，除非您的网站只能从公司内部访问。否则您的API账号信息可以轻易被用户获取并用作其他用途，您将为这部分非法用途付费。

**生产环境上不应该使用示例代码中的轮询**判断任务完成部分，
而**应该通过回调**获取任务完成信息（即配置启动任务信息中的 `notification` 字段）

想要快速开始或者查看更多算法调用示例？建议先使用我们的Python样例了解http请求方法以及请求参数： https://gitee.com/chohotech/api_python_sample


## 使用步骤

直接在浏览器中访问`index.html`，填入相应信息与待切分的半颌三维模型即可启动分牙任务。

`index.html`中的`start_seg`函数也可以在Node.js中使用。

运行后网页将生成分牙结果`processed_mesh.stl`和`seg_labels.txt`并提供下载链接。

## 样例

- 本样例展示了
  1. 如何新建任务JSON
  2. 如何向服务器新建任务
  3. 如何向服务器查询任务状态并等待任务完成
  4. 如何获取任务结果
  5. 如何解析任务结果
- 请注意，这里我们展示了如何进行分牙任务，但是其他任务大同小异，用户经过简单的修改即可使用
- 本样例展示的是如何将一个STL半颌文件进行切分并将结果存为blob

## 代码许可

本仓库基于AGPL v3.0许可开源，如果您在项目中使用本仓库的代码，则您的项目必须向用户（包括SaaS用户）提供源代码。如果您是朝厚的付费用户，此份代码将根据我们的订阅用户协议向您授权，您没有遵守AGPL v3.0开源协议的义务。