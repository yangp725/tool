https://www.sublimetext.com/3

### 常规设置
\Sublime Text3\Data\Packages\User\Preferences.sublime-settings  
设置如下：
```
{
"color_scheme": "Packages/Color Scheme - Default/Monokai Bright.tmTheme",
//"font_face": "courier New bold",
//"font_face": "Consolas",
//"font_face": "DejaVu Sans Mono",
"font_face": "Ubuntu Mono",
"font_size": 14,
//"font_weight": "bold",
"highlight_line": true,
"rulers":[80],
"save_on_focus_lost": true,
"show_encoding": true,
"show_line_endings": true,
"tab_size": 4,
"translate_tabs_to_spaces": true,
"trim_trailing_white_space_on_save": true
}
```
### 支持中文
https://segmentfault.com/a/1190000002461891  
1.在Sublime Text里，按ctrl+`，打开Console，一次性输入如下代码：

```
import urllib.request,os;pf = 'Package Control.sublime-package';ipp = sublime.installed_packages_path();urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) );open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```
2.重启Sublime Text  
3.在Sublime Text中，按Ctrl+Shift+P打开命令行模式，输入Install Package关键字，然后点击自动出现的下拉菜单里的第一项：Package Control: Install Package  
4.此时你会看到左下角有个=号来回动，稍等一会，会再次在命令行下弹出一个下拉菜单。输入“ConvertToUTF8”或者“GBK Encoding Support”，选择匹配项

### Connect Server
Install Package -> SFTP
选择一个文件夹打开,然后同步到服务器
