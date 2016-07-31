* 进入hexo

1. $ cd public/guoyuhui.github.io
2. $ git clone https://github.com/iissnan/hexo-theme-next themes/next
3. 当 克隆/下载 完成后，打开 站点配置文件（*a哪个是站点配置文件--guoyuhui下的是站点配置文件，哪个是主题配置文件--theme下的是主题配置文件？*）， 找到 theme 字段，并将其值更改为 next。
   启用 NexT 主题
   
   theme: next
4. 用$ hexo clean 来清除 Hexo 的缓存
5. $ hexo s --debug，前往4000站点，查看是否成功。
6. 如果成功，用hexo-g,hexo-d两个命令生成，就可以到网址上看到主题变化了。
