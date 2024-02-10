# myexvim
### how to install exvim
1) cp .vim* ~/ -rf
2) sudo apt install id-utils gawk ctags vim
3) sudo apt install tmux
myexvim + tmux : tmux是基于多终端开发，与myexvim 结合使用，解决了myexvim的窗口占用问题，还有可以解决在myexvim 中,
复制粘贴的问题, tmux + myexvim 可以更方便在多终端，多工程，多窗口下快速切换和开发.

### how to use exvim
0) base on exvim, :Update --> update tags and ID.
1) :GS {tag}  : global search tags
2) ctrl+] or \+] : jump to seltect tags defines
3) \\ : search call functions
4) gg :jump to head , shit+g : go to end.
  ctrl + d: fast down , ctrl + u： fast up.
  ctrl + h/l : swtich file buffer:minibuffer
### Note
历数当前的编辑器的优缺点:
1) source insight : 查看代码利器,无太大的缺点, nodepad++ 适合编辑少量文件
2) vim 编辑器：全命令式编辑器，缺点是集成度不够高，没有基于project的概念去开发，也就意味着：并不适合做工程开发
  即便添加一些插件也解决不了缺少project的缺点
3) exvim 基于project的原理开发，插件也做了相应的调整，确保了插件稳定性. 
  本工程基于exvim 下在ubuntu 16-ubuntu22.04 都可以正常跑。其中修改如下:
  a. 修改了filebuffer ： 使用minibuffer 更加简单直接, 只需要ctrl + h/l  就可以切换，多了的filebuffer 可以使用在选中buffer后d删除.
  b. 修改了默认的工程配置，做到了开箱即用的特点,默认不显示侧边栏文件结构，因为不适用.
  c. id-lang.map 里面添加了识别ID 的语言, 
     下面添加ctags默认识别语言:
-    let ctags_optioins = '--fields=+iaS --extra=+q'
+    let ctags_optioins = '--c++-kinds=+px --langmap=c++:+.ino  --langmap=python:+.be   --fields=+aiKSz --extra=+q'
4) myexvim的优点: 集成了exvim的优点，并且从中做了简化,适合做工程开发，命令行开发全程可以无需鼠标，减少注意力的分散点，做到了所想即所得。与source insight
有同样的基于project开发的理念,区别在于：一个是代码的所见即所得，一个是代码的所想即所得。

