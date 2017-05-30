## 查询统计非空文件夹

> find . -mindepth 1 -maxdepth 1 -type f | grep . | wc -l

find后边的参数用于指定路径, depth参数用于指定深度, 1为在当前路径下. -type用于制定文件类型, directory或者file等. grep是在返回的结果中做字符串查询. wc -l是进行统计.



## [The ps command](http://www.linfo.org/ps.html)

> ps -ef | grep adam

