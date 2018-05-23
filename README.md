# PythonLearn
记录一些学习Python的语法知识和心得，并且利用Python实现的网络爬虫



## 爬取网络上的文章

- [ ] 爬取“[梦远书城](http://www.my285.com/xdmj/index.htm)”中的「[现代文学]((http://www.my285.com/xdmj/index.htm))」、「[言情小说](http://www.my285.com/yq/index.htm)」、「[武侠小说](http://www.my285.com/wuxia/index.htm)」，获取每个作者信息和对应的url
- [ ] 解析每个作者的Url和爬取作者名下文章



### 获取链接：

通过配置:

> ```
> wuxia/index.htm "body td.bg > a[href]"
> yq/index.htm   "body td.t3 > a[href]"
> xdmj/index.htm "body td[bgcolor="#FFFFFF"] > a[href]"
> ```





```java
Stack<Integer> stack1 = new Stack<Integer>();
Stack<Integer> stack2 = new Stack<Integer>();

public void push(int node) {
    stack2.add(node);
}

public int pop() {
    if (stack1.isEmpty()) {
        if (!stack2.isEmpty()) {
            while (!stack2.isEmpty()) {
                stack1.add(stack2.pop());
            }
        }
    }
    return stack1.pop();
}
```



