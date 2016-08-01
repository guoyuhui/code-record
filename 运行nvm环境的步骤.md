# 一：运行nvm环境的步骤

    (1).curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.2/install.sh | bash

curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.2/install.sh | NVM_DIR="path/to/nvm" bash

git clone https://github.com/creationix/nvm.git ~/.nvm && cd ~/.nvm && git checkout `git describe --abbrev=0 —tags`

. ~/.nvm/nvm.sh

~/.zshrc

2. export NVM_DIR="$HOME/.nvm"

[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm

3. nvm install 5.0

     (4).nvm use 5.0

10. $ npm install -g hexo-cli

      (11).$ cd ~/Public
      
    git clone https://github.com/guoyuhui/guoyuhui.github.io.git(如果hexo出问题，只用重装hexo,不用走clone这一步，直接从第11步调到第13步)

12. $ hexo init guoyuhui.github.io

13. $ cd guoyuhui.github.io

     (14).$ npm install hexo-deployer-git --save
     
15.$ hexo generate

16.$ hexo server

# 二：在atom中如何调出username文件

1.atom中

Atom 就会打开 yourname.github.io 这个文件夹…… 在计算机世界里，. 是个特殊字符，代表“所有的”（以后你会越来越了解的），所以，atom . 的意思相当于“用 Atom 这个程序打开当前目录内的所有文件”……
在 Atom 的左侧面板中，选择 _config.yml 文件，找到 deploy 哪一部分，改成：

deploy:

  type: git
  
  repo: https://github.com/guoyuhui/guoyuhui.github.io.git
  
  >每个冒号后面都麻痹要加空格！！！

repo:git@github.com:guoyuhui/guoyuhui.github.io.git

2.username:aliceguo2016reborn@gmail.com
  username:guoyuhui
  password:G..1.........-.F
  

3.teminal中依次输入

hexo deploy

(open guoyuhui.github.io)

open https://guoyuhui.github.io

(open . 打开atom相关文件夹guoyuhui.github.io)


# 三：run npm command gives error "/usr/bin/env: node: No such file or directory”


1.输入：ln -s /usr/bin/nodejs /usr/bin/node

2.ln: /usr/bin/node: Operation not permitted怎么办？

# 四－在atom里调用terminal面板

输入：apm install platformio-ide-terminal
