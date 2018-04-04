杂记，回头再整理
步步为坑，那就稳扎稳打，步步为营
## 需求：把 https://github.com/pingcap/docs-cn 转成 pdf 电子书
###需求分解
 1. Single markdown page-pdf：a piece of cake... 
 2. Multiple markdown pages - one big PDF: list the file of the md names in the command
 3. 中文，需要额外的编码和字体支持
 
 ## 系统： ubuntu 16.04
 
 ## 工具
 1. Pandoc: $ sudo apt-get install pandoc
 2. Texlive: $ sudo apt-get install texlive-xetex texlive-latex-recommended texlive-latex-extra
 3. Fonts: Font manager： 查看并安装中文字体 （字体来源：从windows系统里面拷过来）
 ## 命令：
 
 $ pandoc -N -s --toc --smart --latex-engine=xelatex -V CJKmainfont='微软雅黑' -V mainfont='Segoe UI' -V geometry:margin=1in README.md op-guide/recommendation.md  op-guide/binary-deployment.md op-guide/docker-deployment.md op-guide/configuration.md op-guide/monitor-overview.md op-guide/monitor.md op-guide/pd-control.md sql/README.md op-guide/mysql-compatibility.md faq.md trouble-shooting.md op-guide/migration.md op-guide/tune-TiKV.md op-guide/history-read.md -o output.pdf
## Known issues
 图片显示
 命令行太长
 
 
 ## 致谢
 http://www.ituring.com.cn/article/828
 http://www.cnblogs.com/airbird/p/6160223.html
 
