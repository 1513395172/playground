# 安装sublime text 3/package control/Markdown editing/Markdown Preview

摘要 本文主要介绍安装4种工具sublime text 3/package control/Markdown editing/Markdown Preview 步骤 

### 安装sublime text 3

Link https://www.sublimetext.com/3
Goal 安装sublime text 3
CML
- 下载OS X版本
Return
- 桌面打开

### 安装package control

Link https://packagecontrol.io/installation
Goal 安装package control
CML
- 用`control + ` `打开sublime text 3的console

- 复制粘贴
```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 
```

Return
- Package Control: No updated packages


### 安装markdown editing

Link https://packagecontrol.io/packages/MarkdownEditing#installation
Goal 安装Markdown Editing
CML
- Type `install package` and hit Return.
- Type `MarkdownEditing` and hit Return.
Return
```
[linkBlackboardTheme]: https://github.com/mdesantis/MarkdownEditing/blob/blackboard-theme/MarkdownEditor-Blackboard.tmTheme
  [mdesantis]: https://github.com/mdesantis
```

### 安装Markdown Preview 
Link https://packagecontrol.io/packages/Markdown%20Preview
Goal 使sublime text 3 有markdown预览功能
CML
- cmd + shift + p 
- Package Control : Install Package
- 找到Markdown Preview
- 安装
Return
```
Package Control Messages
========================

Markdown Preview
----------------

  Sublime Text 2/3 Markdown Preview
  =================================
```
Note
- 第1次使用该步骤安装失败
- 同样步骤尝试了第2次, 成功

Goal 使用Markdown Preview 预览
CML
- cmd + shift + p
- 输入mdp
- 选择markdown

### 使用markdown editing插入链接

Link
- https://github.com/SublimeText-Markdown/MarkdownEditing#key-bindings
- https://github.com/DebugUself/du4proto/issues/40
Goal 使用markdown editing插入链接
CML 
- 安装插件Markdown Editing
- 在Preference->Packages Settings->MarkdownEditing->keyBingding-Default中有：

    // inline image insertion
    { "keys": ["super+shift+k"], "command": "reference_new_inline_image", "context":
        [
            { "key": "selector", "operator": "equal", "operand": "text.html.markdown", "match_all": true }
        ]
    },
    // run paste as link command on selected text
    { "keys": ["ctrl+super+v"], "command": "reference_new_inline_link", "context":
        [
            { "key": "selector", "operator": "equal", "operand": "text.html.markdown", "match_all": true }
        ]
    },

  - 根据提示，可使用：
    + cmd + option + k 插入图片
    + cmd + option + v 插入链接
Return
- 输入`cmd + option + v`, 返回`[]()`

### Sublime text 3 其他编辑技巧
区域选中 
- cmd + shift + L
- cmd + shift + ↑
- cmd + shift + ↓
选中一行 cmd + L
选中部分 cmd + shift + →/←
跳到行头/行末尾 cmd + →/←

