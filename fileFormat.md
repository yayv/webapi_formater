这个格式说明文件，用 raw 模式看效果更好。

# 接口文件格式说明

## 文件格式

```
  # 文件说明
  # 其他内容
	~~test~~
  ## MENU 
  * MENU标题行之下,到另一个标题之前均为菜单内容。菜单内的模块用加粗行表示 *
  *用户*
  - [ ] User01: 用户登录
  *功能*
  - [ ] Func01: 功能A
  
  # Interface Start 
  *从上一行开始为接口描述的内容*

  ## 模块编码1:模块名1

  ### 接口编号1:接口名1
  
  ### 接口编号2:接口名2
  
  ### 接口编号3:接口名3

  ## 模块编码2:模块名2

  ### 接口编号5:接口名5
  
  ### 接口编号6:接口名6
  
  ### 接口编号7:接口名7
  ```
  CODE: 同标题的<接口编号>
  NAME: 同标题的<接口名>
  URL: 必写
  METHOD: POST/GET...
  FORMAT: JSON/FORM
  NOTE:
  TODO:
  REQUEST: 统一用json格式表示, 必须有,值可以为空白
  RESPONSE: 必须有内容
  STATUS:
  LASTMODIFY: 最后修改日期,用于判断本接口是否有更新
  ```
  
```

说明:
其中, REQUEST 和 RESPONSE 的内容均需要用接口参数格式进行描述。如果 METHOD 为 GET 方法, 则 URL 里允许出现参数表的占位符, 如: {params}. 或者, 用 {key} {value} 的方式表示具体的 URL 拼接方式, 具体参数表的描述依然使用 REQUEST 部分的年日哦给你进行描述。

接口描述格式中, URL,REQUEST,RESPONSE 3项为必填项; NO 和 NAME 项必须与标题行的内容一致。
