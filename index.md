## 面试问题

You can use the [editor on GitHub](https://github.com/GStarmin/GStarmin.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

## OS

### 操作系统调度原则
- 如果运行的程序发生I/O事件请求，CPU使用率会降低，因为此时进程在等待硬盘数据的返回。所以为了提高CPU运行效率，在由于I/O导致CPU空闲时，调度程序需要从就绪队列中选择一个进程运行。
- 有的程序执行时间较长，一直占有CPU，系统吞吐量（单位时间内CPU完成的进程数量）降低。所以为了提高系统吞吐量，调度程序需要权衡长任务和短任务的完成数量。
- 进程的周转时间包含运行时间和阻塞等待时间。进程的周转时间越小越好，调度程序需要保证周转时间尽可能的小
- 调度程序需要让就绪队列中的等待时间尽可能的短
- 对于交互式比较强的应用，比如键盘、鼠标，调度程序要考虑程序的响应时间尽可能快。

总上所述，调度程序主要从以下几个系统参数来考虑：
- CPU利用率：调度程序尽可能的让CPU繁忙，提高调度程序的利用率
- 系统吞吐量：吞吐量是单位时间内CPU完成的进程数，长作业会降低吞吐量，短作业提高吞吐量
- 周转时间：周转时间是运行时间和阻塞时间的总和，一个进程的调度时间越小越好
- 等待时间：进程在就绪队列中等待时间尽可能的短
- 响应时间：在交互式较强的系统，调度算法需要尽可能的降低响应时间

### 读者写者问题的应用
1. 独木桥问题
- 一次只能上一辆车
- 一次可以上多辆车
2. Linux的IPX路由代码使用了读-写锁，读路由表的情况比更新路由表的情况多得多。

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/GStarmin/GStarmin.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
