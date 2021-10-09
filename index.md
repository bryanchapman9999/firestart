## Welcome to Bryan's Pages

You can use the [editor on GitHub](https://github.com/bryanchapman9999/firestart/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Links
[Outlook](https://outlook.live.com/owa/)


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

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/bryanchapman9999/firestart/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

### Notepad

data: text/html,
<html>
    <head>
        <title>Notepad</title>
        <link rel="icon" type="image/png" href="http://icons.iconarchive.com/icons/hopstarter/sleek-xp-software/256/Notepad-icon.png">
        <script src="http://code.jquery.com/jquery-2.0.3.min.js"></script>
        <script type="text/javascript">
            $(document).ready(function() {
                $('#text').bind('keyup', function() {
                    var content = $(this).val();
                    setTitle(content);
                    setLineNumber(content);
                });

                $('#text').bind('focus click', function() {
                    var content = $(this).val();
                    setLineNumber(content);
                });
            });

            function setTitle(content) {
                var lines = content.split('\n');

                for (i = 0; i < lines.length; i++) {
                    if (lines[i].trim().length > 0) {
                        document.title = lines[i];
                        return 0;
                    }
                }

                document.title = "Notepad";
            }

            function setLineNumber(content) {
                var lineNumber = content.substr(0, $('#text').prop('selectionStart')).split("\n").length;
                $('#lineNumber').html(lineNumber);
            }
        </script>
        <style type="text/css">
            #text {
                position: absolute;
                font-family: Menlo;
                font-size: 12px;
                width: 100%;
                height: 100%;
                border: none;
                outline: none;
                padding: 15px;
                padding-bottom: 35px;
                background: #EEEEEE;
            }

            #ruler {
                position: absolute;
                left: 925px;
                width: 2px;
                height: 100%;
                border-right: 1px solid lightgray;
            }

            #statusBar {
                background-image: -ms-linear-gradient(top, #C7C7C7 0%, #8C8E8F 100%);
                background-image: -moz-linear-gradient(top, #C7C7C7 0%, #8C8E8F 100%);
                background-image: -o-linear-gradient(top, #C7C7C7 0%, #8C8E8F 100%);
                background-image: -webkit-gradient(linear, left top, left bottom, color-stop(0, #C7C7C7), color-stop(1, #8C8E8F));
                background-image: -webkit-linear-gradient(top, #C7C7C7 0%, #8C8E8F 100%);
                background-image: linear-gradient(to bottom, #C7C7C7 0%, #8C8E8F 100%);

                /*background: #C7C7C7;*/
                position: absolute;
                left: 0;
                bottom: 0;
                width: 100%;
                height: 23px;
                border-top: 1px solid #656565;
            }

            #statusBarText {
                font-family: 'Lucida Grande';
                font-size: 12px;
                font-weight: bold;
                color: #393C3E;
                text-shadow: 1px 1px #CBCBCB;
                margin-left: 6px;
                margin-top: 3px;
            }
        </style>
    </head>
    <body style="margin: 0;">
        <textarea id="text" autofocus spellcheck="false"></textarea>
        <div id="ruler"></div>
        <div id="statusBar">
            <div id="statusBarText">Line <span id="lineNumber">1</span></div>
        </div>
    </body>
</html>
