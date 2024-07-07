<<<<<<< HEAD
以下是一个详细的 Pelican 入门教程，帮助您从安装到创建并发布一个静态网站。

### 1. 安装 Pelican 和 相关依赖
首先，您需要安装 Pelican 和 Markdown（用于编写文章内容）。

```bash
pip install pelican markdown
```

### 2. 创建项目目录
创建一个新的目录用于存放您的 Pelican 项目。

```bash
mkdir my_blog
cd my_blog
```

### 3. 初始化 Pelican 项目
在项目目录中运行以下命令初始化 Pelican 项目。

```bash
pelican-quickstart
```

此命令会提示您输入一些配置信息，例如网站名称、作者名称、语言等。

### 4. 编写文章
在 `content` 目录中创建 Markdown 文件来编写您的文章。例如，创建一个名为 `first_post.md` 的文件：

```markdown
Title: 我的第一篇文章
Date: 2024-07-07
Category: 杂记
Tags: 初学者, 教程
Slug: my-first-post
Author: 您的名字
Summary: 这是我的第一篇文章的摘要。

这是文章的内容部分，可以使用 Markdown 语法来编写。
```

### 5. 生成静态网站
使用 Pelican 生成静态网站。

```bash
pelican content
```

此命令会在 `output` 目录中生成静态网站文件。

### 6. 预览网站
使用内置的 HTTP 服务器来预览您的网站。

```bash
pelican --listen
```

在浏览器中打开 [http://localhost:8000](http://localhost:8000) 来查看您的网站。

### 7. 自定义主题
您可以使用自定义主题来改变网站的外观。首先，下载您喜欢的主题（例如 Flex）：

```bash
git clone https://github.com/alexandrevicenzi/Flex.git themes/Flex
```

然后在 `pelicanconf.py` 文件中设置主题路径：

```python
THEME = 'themes/Flex'
```

### 8. 发布网站
您可以将生成的静态网站文件上传到任何静态网站托管服务，例如 GitHub Pages、Netlify 或 Vercel。以 GitHub Pages 为例：

1. 创建一个新的 GitHub 仓库。
2. 将 `output` 目录中的文件推送到 GitHub 仓库的 `gh-pages` 分支。

```bash
cd output
git init
git remote add origin <your-github-repo-url>
git add .
git commit -m "Initial commit"
git push -u origin master:gh-pages
```

您的网站将会在 `https://<your-username>.github.io/<your-repo>/` 上可访问。

### 9. 完整示例配置文件 (`pelicanconf.py`)

```python
AUTHOR = '您的名字'
SITENAME = '我的博客'
SITEURL = ''

PATH = 'content'

TIMEZONE = 'Asia/Shanghai'

DEFAULT_LANG = 'zh'

THEME = 'themes/Flex'

# Feed generation is usually not desired when developing
FEED_ALL_ATOM = None
CATEGORY_FEED_ATOM = None
TRANSLATION_FEED_ATOM = None
AUTHOR_FEED_ATOM = None
AUTHOR_FEED_RSS = None

# Blogroll
LINKS = (('Pelican', 'https://getpelican.com/'),
         ('Python.org', 'https://www.python.org/'),
         ('Jinja2', 'https://palletsprojects.com/p/jinja/'),)

# Social widget
SOCIAL = (('You can add links in your config file', '#'),
          ('Another social link', '#'),)

DEFAULT_PAGINATION = 10

# Uncomment following line if you want document-relative URLs when developing
# RELATIVE_URLS = True
```

### 10. 参考资源
- [Pelican 官方文档](https://docs.getpelican.com/)
- [Markdown 基础教程](https://www.markdownguide.org/basic-syntax/)

通过以上步骤，您应该能够创建并发布一个简单的 Pelican 静态网站。如果有任何问题或需要进一步的帮助，请随时提问！
=======
# walog.github.io
>>>>>>> f9d0f4178701df70853ca28eb4135e3f922546cd
