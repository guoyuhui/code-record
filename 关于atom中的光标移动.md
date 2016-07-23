# 关于atom中的光标移动

1. 呼出Command Palette
2. 输入init script
3. 贴代码

  SymbolRegex = /\s*[(){}<>[\]/'"]/
  atom.commands.add 'atom-text-editor', 'custom:jump-over-symbol': (event) ->
  editor = atom.workspace.getActiveTextEditor()
  cursorMoved = false
  for cursor in editor.getCursors()
    range = cursor.getCurrentWordBufferRange(wordRegex: SymbolRegex)
    unless range.isEmpty()
      cursor.setBufferPosition(range.end)
      cursorMoved = true
  event.abortKeyBinding() unless cursorMoved

4. 保存

5. 呼出Command Palette
6. 输入keymap
7. 贴代码

  ' atom-text-editor:not([mini]) ':
  'shift': ‘custom:jump-over-symbol'

8. 保存

9. 关闭atom
10. 重新打开就可以用了


这个方法只是一个一个的移动光标，

如果想让光标快速跳到行末，可以使用fn-➡️，或者command－➡️来执行命令；

如果想让光标从上一行的任何一个位置，直接跳到下一行，可以用command－return来执行命令。

       ps：来叔，在您的6月16日《基本开发环境设置》那篇文章里，在“安装atom”这个大标题下，引号中这段话：
       “关于 brew cask命令的说明，请参阅其官方网站：https://caskroom.io…… 学任何工具，第一件事情就是去把官方网站翻个遍，是必须的习惯。”

        网址是无效的，估计您少打了个Github。
        所以正确的网址应该是： https://caskroom.github.io
