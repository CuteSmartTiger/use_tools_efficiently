数字模式
chmod u=rx scriptfile.sh
直到现在为止，我们使用了叫做“符号”的模式来用 chmod 指定权限的改变。然而，指定权限还有
一种普遍使用的方法 — 使用 4 位八进制数。使用叫做数字权限语法的语法，每一位代表一个权限
三元组。例如，在 1777 中，777 设置本章我们所讨论的“owner”、“group”和“other”
标志。1 用来设置专门的权限位，我们将在本章的结束部分讲到。这个图表说明了怎样解释第二到
四位（777）：
模式 数字
rwx 7
rw- 6 
r-x 5
r-- 4
-wx 3
-w- 2
--x 1
--- 0