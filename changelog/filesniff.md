filesniff.py

current version: 1.9

--------------------------------------------------------------------------------

## 1.9 | 2021-02-17

- [移除] stitch_path
- [移除] LKDB 和 lkdb
- [优化] 调整 _find_paths:args:fmt='dlist' 在无结果时的返回值
- [变更] 调整 suffix 和 fmt 的参数顺序
- [更新] 扩展 find_dirs:_filter, findall_dirs:_filter 对受保护文件的判断

## 1.8 | 2020-09-05

- [优化] _find_paths() 的 suffix 参数简化作用
- [变更] _find_paths() 返回格式调整为 fp-fn
- [变更] create_dirpath() 重命名为 force_create_dirpath()
- [更新] get_dirname() 增强稳定性
- [修复] __get_prj_dir() 的某些错误
- [修复] get_dirname() 对 './' 和 '../' 的错误处理
- [修复] find_subdirs(), findall_subdirs() 的过滤器错误
- [修复] _find_paths() 无结果时 `fmt='dlist'` 产生的报错
- [新增] ret_str() 装饰器
- [更新] 部分函数使用 pathlib.Path
- [变更] path_on_rel() & path_on_self() 重命名为 relpath()
- [优化] 简化 get_dirname() 函数

## 1.7 | 2020-08-22

- 创建 class FSPath

## 1.6 | 2020-08-02

- 重新设计 path getters
- 改善 LKDB 的初始值定义
- 新增 create_dirpath() 方法
- get_dirname() 新增支持 filepath

## 1.5 | 2019-12-18

- 查找文件/文件夹的方法提取出通用方法 _find_paths()
- 修复 _find_paths() 在 suffix 为数组时的过滤错误
- 优化 isfile() 方法
- 完善注释文档
- 调整 _get_prj_dir() 方法
- 调整私有方法命名
- 更正 isdir() 逻辑

## 1.4 | 2019-11-01

- 新增 stitch_path() 方法
- stitch_path() 新增 wrapper 参数
- find_files() 的 rtype 参数取消 int 类型支持
- dialog() 在找不到文件时予以报错
- 使用 filter 重构 find_files()
- find_files() suffix 参数增加支持 staticmethod 类型
- 移除 calc_relpath() 方法
- find_files() 调整参数顺序

## 1.3 | 2019-11-01

- file_sniffer.py 重命名为 filesniff.py
- 优化全部方法和代码逻辑
- 部分非常用方法转为内部方法
- 移除 get_lkdb_path()
- 新增 lkdb() 方法
- get_relpath() 重命名为 calc_relpath()
- lkdb() 增加支持 "{PRJ}" 关键字

## 1.2 | 2019-04-17

- get_filenames() 改为 get_filename 并简化方法
- 创建 getfile() 方法
- 创建 findall_files() 方法
- 简化 findall_subdirs() 方法
- 创建 get_dirname() 方法
- 改善尝试寻找 curr_project_dir 失败时的做法
- getfile() 重命名为 getpath()
- 优化 find_project_dir() 的方法和逻辑
- dialog() 不再免费提供 adir 参数的缺省值
- 简化 get_launch_path() 方法
- find_project_dir() 支持自定义工作路径
- 创建 get_relpath() 方法
- 简化导入的模块
- 创建 isfile() 方法
- 增加环境变量 (LKPATH 系列) 的简单获取方法
- 创建 isdir() 方法
- 提升 isdir() 判断效率
- get_filename() 参数 include_postfix 默认值改为 True
- findall_files() 增加支持更多返回类型
- 明确定义 findall_files() postfix 参数的作用
- find_subdirs() 和 findall_subdirs() 增加 except_protected_folder 参数
- 使用推导式重构 find_subdirs() 和 findall_subdirs()
- 移除 Locator
- findall_files() 增加 rtype='zip'
- findall_files() 部分返回值格式调整

## 1.1

- 将 easy_find_path.py 合并到此模块中
- Locator 增加快捷获取文件 (in.txt, out.txt 等)
- find_files() postfix 增加列表/元组类型的支持
- 创建 dialog() 方法
- 创建 find_subdirs() 方法
- 解决 get_curr_dir() 在 pyinstaller 导出后出错的问题
- 修复 dialog() 的打印层级错误
- 创建 findall_subdirs() 方法
- 删除 find_excels() 方法
- 创建 get_filenames() 方法
- dialog() 使用 print() 代替 lk.prt()
- 增强 find_files() 容错性

## 1.0

- 创建 file_sniffer.py
