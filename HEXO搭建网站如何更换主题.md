* 进入hexo

1. $ cd public/guoyuhui.github.io
2. $ git clone https://github.com/iissnan/hexo-theme-next themes/next
3. 当 克隆/下载 完成后，打开 站点配置文件（在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml。
   其中，一份位于站点根目录下，主要包含Hexo本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。为了描述方便，在以下说明中，将前者称为 站点配置文件， 后者称为 主题配置文件。）， 找到 theme 字段，并将其值更改为 next。
   
   启用 NexT 主题
   
   theme: next
4. 用$ hexo clean 来清除 Hexo 的缓存
5. $ hexo s --debug，前往4000站点，查看是否成功。
6. 如果成功，用hexo-g,hexo-d两个命令生成，就可以到网址上看到主题变化了。
