## 首页不要页码 
1. 在begin命令或者newpage命令之后，马上调用pagenumbering{gobble}，这个可以消掉该页页码
2. 然后在下一页（通常是newpage命令之后），调用pagenumbering{arabic}，重新开始显示页码


