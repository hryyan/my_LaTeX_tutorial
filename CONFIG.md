### LaTeX的配置
1. 首先安装texlive

```shell
sudo apt-get install texlive-full
```

2. 接着修改默认字体

```shell
sudo vim /usr/share/texlive/texmf-dist/tex/latex/ctex/fontset/ctex-xecjk-winfonts.def```

将ItalicFont中的楷体改为wqy-microhei.ttc，具体名称可以看
```shell
fc-list :lang=zh-cn
```

3. 将Fonts文件夹中的字体放在~/.fonts文件夹中

4. 在Sublime中安装LaTeXTools

5. 设置builder为xelatex

```shell
cd ~/.config/sublime-text-3/Packages/LaTeXTools/builders/
vim simpleBuilder.py
```

将41行中的pdflatex改为xelatex

6. 在sublime的package设置中，改build方式为simple
