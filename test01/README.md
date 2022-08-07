# test01
## 添加头文件搜索路径
* `include_directories`，给项目中**所有目标**添加此搜索路径。
* `target_include_directories`，给项目中**指定目标**添加此搜索路径。

## 添加库搜索路径
* `link_directories`，给项目中**所有目标**添加此搜索路径，必须放到add_executable前面。
* `target_link_directories`，给项目中**指定目标**添加此搜索路径。