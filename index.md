## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Sludge-Factory/nguidlechat/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="https://cdn.socket.io/socket.io-3.0.1.min.js"></script>
</head>
<body>
    
    <input type="text" class="message">
    <button onclick="sendMessage()">Send</button>
    <h1></h1>
    <script>

        const socket = io('http://localhost:3005')

        socket.on('connection')

        socket.on('message', (data) => {
            document.querySelector('h1').innerHTML = data
        })
        const sendMessage = () => {
            const usertext = document.querySelector('.message')
            const message = usertext.value
            socket.emit('message', message)
        }
    </script>


</body>
</html>


For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Sludge-Factory/nguidlechat/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we???ll help you sort it out.
