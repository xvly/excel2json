# excel2json

详细帮助文档请见：[https://neil3d.github.io/coding/excel2json.html](https://neil3d.github.io/coding/excel2json.html)

## 命令行参数

* -e, –excel Required. 输入的Excel文件路径.
* -j, –json 指定输出的json文件路径.
* -h, –header Required. 表格中有几行是表头.
* -c, –encoding (Default: utf8-nobom) 指定编码的名称.
* -l, –lowcase (Default: false) 自动把字段名称转换成小写格式.
* -a 序列化成数组
* -d, --date:指定日期格式化字符串，例如：dd / MM / yyy hh: mm:ss
* -s 序列化时强制带上sheet name，即使只有一个sheet
* -exclude_prefix： 导出时，排除掉包含指定前缀的表单和列，例如：-exclude_prefix #
* -cell_json：自动识别单元格中的Json对象和Json数组，Default：false

## 问题记录
* nuget 库下载

    * 方案一：直接更新（实测无效，修改 nuget 程序源也一样无效）
    * 方案二：通过 https://www.nuget.org/packages 下载相关包，然后通过设置 nuget 程序源更新，能解决大部分 nuget 更新问题。但是有一个 NewtonSoft.Json 依然无法更新，该文件最终通过 PM>Install-Package Newtonsoft.Json -Version 12.0.3 指令进行进行更新（注：提示已拥有 Microsoft.CSharp 定义的依赖库，直接更新 nuget 即可）。

## 示例
![Excel](./Docs/excel.png)  
![GUI](./Docs/gui.png)  
![CMd](./Docs/cmd.png)  


