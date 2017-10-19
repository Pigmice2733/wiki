# Contributing to This Wiki

First off, thanks for your interest in helping the wiki grow.

## Editing a page
If you want to edit a page that already exists, you can go to that page and click on the "Suggest an edit to this page" button. Then you can make your changes. Make sure you select the "create a new branch" option. Name your branch with your initials, followed by a description of your changes.

Example: `cee/add-programming-guide`

![Committing on GitHub](/images/commit-on-github.png)

## Creating a new page

First, [create a file on the GitHub repo](https://github.com/Pigmice2733/wiki/new/master). The file's name will turn into the URL of the page. You **must** use the `.md` extension.

Examples:
- `contributing-to-wiki.md`
- `programming/getting-started.md`
- `programming/deploying-code.md`
- `design/using-cad.md`

![Naming a file](/images/naming-file.png)

Then fill in the contents of your file. The wiki is formatted using [Markdown](https://en.wikipedia.org/wiki/Markdown). You should read through [GitHub's guide to Markdown](https://guides.github.com/features/mastering-markdown/).

Your page must have a top-level heading, which is the title of the page.

Example:
```md
# Title of the article

Article contents here
```

When you include images, put them in the [`images` folder](https://github.com/Pigmice2733/wiki/tree/master/images), and include them like this:
```md
![image description here](/images/path-to-image.png)
```

If you need code examples in your page, you can use backticks for code samples that look like
`` `this` `` 🡪 `this`

If you want full code examples that aren't part of a sentence, use triple backticks:

````md
```
code here
```
````
You can put a language after the first backticks if you want the code to be colored:

````
```python
def foo:
  4 + 5 - number
```
````
Turns into:
```python
def foo:
  4 + 5 - number
```

Then, as shown above, commit your changes to a branch.
