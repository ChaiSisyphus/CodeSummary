## 记录编程的机会 经验 新学到的知识
# 记录新学会的java编程知识
  map.getOrDefault(key， defaultValue)方法
  从map中根据键key获得对应的值，若没有键值对，则返回一个设置的默认值
![image](https://user-images.githubusercontent.com/60838780/112316131-c8d90f80-8ce5-11eb-8d04-5947dc2df2f0.png)

# 刷题获得的知识
![image](https://user-images.githubusercontent.com/60838780/112316267-e6a67480-8ce5-11eb-9e93-88f22135c6cc.png)
答案是只创建一次对象，因为String类型在java中被设定为一旦创建就不可改变类型，对String类型的改变，都是创建新的String类型。
既然String类型的量是不能改变的，因此可以在进行编译的时候就将其放入字符串常量池中。题目中，三个已经确定的字符串在进行编译的时候就被合并并放入了常量池中，因此只创建一个对象。

![image](https://user-images.githubusercontent.com/60838780/112832262-a3724a00-90c7-11eb-937a-005040c8b6cf.png)
【1】引用数据类型必须进行初始化才有值，不进行初始化就对其进行索引会报错。一旦适用构造方法对其进行初始化，就算构造方法内部没有对该对象进行赋值，java也会给这个对象赋予一个默认的值（基本数据类型和引用数据类型的初始默认值）

# 有关字符串（String）的心得
【1】任何对字符串进行操作的题一般都要将字符串转换为字符数组，然后按照对数组的操作对字符串进行操作
【2】java中Sting自带的API非常强大，其中有非常多可以使用的方法，比如说toCharArray()——将字符串转换为字符数组；split(regex)——对字符串数组进行分裂，返回字符串数组；replace(oldString, newString)和replaceAll(regex, newString)可将将字符串中的元素进行替换；contact(stirng)——将新字符串连接在被操作字符串后边；charAt(index)——返回字符串索引处的char值；indexof(var)——返回字符串第一次出现目标值时的索引；String.valueOf(var)——返回该变量的字符串形式；

![image](https://user-images.githubusercontent.com/60838780/112985203-79398e80-9192-11eb-98ae-8e8439e0f261.png)
【1】使用split方法对上边的字符串进行分割时，会产生8个字符串数组，分以下几种情况：（1）字符串开始之前每有一个空格，便产生一个空的字符串（2）在字符串中间时，每有n个空格就会产生（n-1）个空的字符串（3）在字符串末尾时，无论有多少个空格都不再产生新的空字符串。【2】使用spilt(" ")方法分离子数组中分为两类:完全不含空格和完全不含有效字符。完全不含有效字符的数组可以对其长度进行判断以此来进行判别。【3】replaceFirst方法，可以替换掉遍历到的第一次复合条件的值，因此不会像replace方法一样，一次性将所有符合条件的值全部替换【4】indexOf——返回字符串中第一次出现目标字符串的索引。
