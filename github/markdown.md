## Headings

To create a heading, add one to six <kbd>#</kbd> symbols before your heading text. The number of <kbd>#</kbd> you use will determine the size of the heading.

```markdown
# The largest heading
## The second largest heading
###### The smallest heading
```

![Rendered H1, H2, and H6 headings](https://docs.github.com/assets/cb-8119/images/help/writing/headings-rendered.png)

When you use two or more headings, GitHub automatically generates a table of contents which you can access by clicking the unordered list icon within the file header. Each heading title is listed in the table of contents and you can click a title to navigate to the selected section. 

![Screenshot highlighting the table of contents icon](https://docs.github.com/assets/cb-47415/images/help/repository/headings_toc.png)


## Styling text

You can indicate emphasis with bold, italic, or strikethrough text in comment fields and `.md` files.  

| Style | Syntax | Keyboard shortcut | Example | Output |
| --- | --- | --- | --- | --- |
| Bold | `** **` or `__ __`| <kbd>Command</kbd>+<kbd>B</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>B</kbd> (Windows/Linux) | `**This is bold text**` | **This is bold text** |
| Italic | `* *` or `_ _`     | <kbd>Command</kbd>+<kbd>I</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>I</kbd> (Windows/Linux) | `*This text is italicized*` | *This text is italicized* |
| Strikethrough | `~~ ~~` | | `~~This was mistaken text~~` | ~~This was mistaken text~~ |
| Bold and nested italic | `** **` and `_ _` | | `**This text is _extremely_ important**` | **This text is _extremely_ important** |
| All bold and italic | `*** ***` | | `***All this text is important***` | ***All this text is important*** |

## Quoting text

You can quote text with a <kbd>></kbd>.

```markdown
Text that is not a quote

> Text that is a quote
```

![Rendered quoted text](https://docs.github.com/assets/cb-12181/images/help/writing/quoted-text-rendered.png)


**Tip:** When viewing a conversation, you can automatically quote text in a comment by highlighting the text, then typing <kbd>R</kbd>. For more information about keyboard shortcuts, see "[Keyboard shortcuts](/articles/keyboard-shortcuts/)."

## Quoting code

You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted.{% ifversion fpt or ghae or ghes > 3.1 or ghec %} You can also press the <kbd>Command</kbd>+<kbd>E</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>E</kbd> (Windows/Linux) keyboard shortcut to insert the backticks for a code block within a line of Markdown.

```markdown
Use `git status` to list all new or modified files that haven't yet been committed.
```

![Rendered inline code block](https://docs.github.com/assets/cb-4680/images/help/writing/inline-code-rendered.png)

To format code or text into its own distinct block, use triple backticks.

<pre>
Some basic Git commands are:
```
git status
git add
git commit
```
</pre>

![Rendered code block](https://docs.github.com/assets/cb-4274/images/help/writing/code-block-rendered.png)

For more information, see "[Creating and highlighting code blocks](/articles/creating-and-highlighting-code-blocks)."

{% data reusables.user-settings.enabling-fixed-width-fonts %}

## Links

You can create an inline link by wrapping link text in brackets `[ ]`, and then wrapping the URL in parentheses `( )`. {% ifversion fpt or ghae or ghes > 3.1 or ghec %}You can also use the keyboard shortcut <kbd>Command</kbd>+<kbd>K</kbd> to create a link.{% endif %}{% ifversion fpt or ghae-issue-5434 or ghes > 3.3 or ghec %} When you have text selected, you can paste a URL from your clipboard to automatically create a link from the selection.{% endif %}

`This site was built using [GitHub Pages](https://pages.github.com/).`

![Rendered link](https://docs.github.com/assets/cb-4329/images/help/writing/link-rendered.png)

{% tip %}

**Tip:** {% data variables.product.product_name %} automatically creates links when valid URLs are written in a comment. For more information, see "[Autolinked references and URLs](/articles/autolinked-references-and-urls)."

{% endtip %}

## Section links

{% data reusables.repositories.section-links %}

## Relative links

{% data reusables.repositories.relative-links %}

## Images

You can display an image by adding <kbd>!</kbd> and wrapping the alt text in `[ ]`. Then wrap the link for the image in parentheses `()`.

`![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)`

![Rendered Image](https://docs.github.com/assets/cb-25655/images/help/repository/readme-links.png)

{% data variables.product.product_name %} supports embedding images into your issues, pull requests{% ifversion fpt or ghec %}, discussions{% endif %}, comments  and `.md` files. You can display an image from your repository, add a link to an online image, or upload an image. For more information, see "[Uploading assets](#uploading-assets)."

{% tip %}

**Tip:** When you want to display an image which is in your repository, you should use relative links instead of absolute links.

{% endtip %}

Here are some examples for using relative links to display an image.
 
| Context | Relative Link |
| ------ | -------- |
| In a `.md` file on the same branch | `/assets/images/electrocat.png` |
| In a `.md` file on another branch | `/../main/assets/images/electrocat.png` |
| In issues, pull requests and comments of the repository | `../blob/main/assets/images/electrocat.png` |
| In a `.md` file in another repository | `/../../../../github/docs/blob/main/assets/images/electrocat.png` |
| In issues, pull requests and comments of another repository | `../../../github/docs/blob/main/assets/images/electrocat.png?raw=true` |

{% note %}

**Note**: The last two relative links in the table above will work for images in a private repository only if the viewer has at least read access to the private repository which contains these images.

{% endnote %}

For more information, see "[Relative Links](#relative-links)."

{% ifversion fpt or ghec or ghes > 3.3 or ghae-issue-5559 %}
### Specifying the theme an image is shown to

You can specify the theme an image is displayed to by appending `#gh-dark-mode-only` or `#gh-light-mode-only` to the end of an image URL, in Markdown.

We distinguish between light and dark color modes, so there are two options available. You can use these options to display images optimized for dark or light backgrounds. This is particularly helpful for transparent PNG images.

| Context | URL |
|--------|--------|
| Dark Theme | `![GitHub Light](https://github.com/github-light.png#gh-dark-mode-only)` |
| Light Theme | `![GitHub Dark](https://github.com/github-dark.png#gh-light-mode-only)` |
{% endif %}

## Lists

You can make an unordered list by preceding one or more lines of text with <kbd>-</kbd> or <kbd>*</kbd>.

```markdown
- George Washington
- John Adams
- Thomas Jefferson
```

![Rendered unordered list](https://user-images.githubusercontent.com/61284764/156911636-f2ac46b0-7fcb-4b57-afdf-77ba446dd30a.png)

To order your list, precede each line with a number.

```markdown
1. James Madison
2. James Monroe
3. John Quincy Adams
```

![Rendered ordered list](https://docs.github.com/assets/cb-3403/images/help/writing/ordered-list-rendered.png)

### Nested Lists

You can create a nested list by indenting one or more list items below another item.

To create a nested list using the web editor on {% data variables.product.product_name %} or a text editor that uses a monospaced font, like [Atom](https://atom.io/), you can align your list visually. Type space characters in front of your nested list item, until the list marker character (<kbd>-</kbd> or <kbd>*</kbd>) lies directly below the first character of the text in the item above it.

```markdown
1. First list item
   - First nested list item
     - Second nested list item
```
![Nested list with alignment highlighted](https://user-images.githubusercontent.com/61284764/156911645-6cdaeed2-5e30-473e-8051-ef23e81b34ed.png)

![List with two levels of nested items](https://user-images.githubusercontent.com/61284764/156911649-b94af5a0-32f4-410e-8365-e669837ff53e.png)

To create a nested list in the comment editor on {% data variables.product.product_name %}, which doesn't use a monospaced font, you can look at the list item immediately above the nested list and count the number of characters that appear before the content of the item. Then type that number of space characters in front of the nested list item.

In this example, you could add a nested list item under the list item `100. First list item` by indenting the nested list item a minimum of five spaces, since there are five characters (`100. `) before `First list item`.

```markdown
100. First list item
     - First nested list item
```

![List with a nested list item](https://user-images.githubusercontent.com/61284764/156911651-5f515968-69c8-432a-9374-b73874f666af.png)  

You can create multiple levels of nested lists using the same method. For example, because the first nested list item has seven characters (`␣␣␣␣␣-␣`) before the nested list content `First nested list item`, you would need to indent the second nested list item by seven spaces.

```markdown
100. First list item
     - First nested list item
       - Second nested list item
```

![List with two levels of nested items](https://docs.github.com/assets/cb-3655/images/help/writing/nested-list-example-2.png)    

For more examples, see the [GitHub Flavored Markdown Spec](https://github.github.com/gfm/#example-265).

## Task lists

{% data reusables.repositories.task-list-markdown %}

If a task list item description begins with a parenthesis, you'll need to escape it with <kbd>\\</kbd>:

`- [ ] \(Optional) Open a followup issue`

For more information, see "[About task lists](/articles/about-task-lists)."

## Mentioning people and teams

You can mention a person or [team](/articles/setting-up-teams/) on {% data variables.product.product_name %} by typing <kbd>@</kbd> plus their username or team name. This will trigger a notification and bring their attention to the conversation. People will also receive a notification if you edit a comment to mention their username or team name. For more information about notifications, see {% ifversion fpt or ghes or ghae or ghec %}"[About notifications](/github/managing-subscriptions-and-notifications-on-github/about-notifications){% else %}"[About notifications](/github/receiving-notifications-about-activity-on-github/about-notifications){% endif %}."

`@github/support What do you think about these updates?`

![Rendered @mention](![image](https://user-images.githubusercontent.com/61284764/156911755-aca63dfd-5b79-4e74-9748-c5c7888edfb5.png)

When you mention a parent team, members of its child teams also receive notifications, simplifying communication with multiple groups of people. For more information, see "[About teams](/articles/about-teams)."

Typing an <kbd>@</kbd> symbol will bring up a list of people or teams on a project. The list filters as you type, so once you find the name of the person or team you are looking for, you can use the arrow keys to select it and press either tab or enter to complete the name. For teams, enter the @organization/team-name and all members of that team will get subscribed to the conversation.

The autocomplete results are restricted to repository collaborators and any other participants on the thread.

## Referencing issues and pull requests

You can bring up a list of suggested issues and pull requests within the repository by typing <kbd>#</kbd>. Type the issue or pull request number or title to filter the list, and then press either tab or enter to complete the highlighted result.

For more information, see "[Autolinked references and URLs](/articles/autolinked-references-and-urls)."

## Referencing external resources

{% data reusables.repositories.autolink-references %}

{% ifversion ghes < 3.4 %}
## Content attachments

Some {% data variables.product.prodname_github_apps %} provide information in {% data variables.product.product_name %} for URLs that link to their registered domains. {% data variables.product.product_name %} renders the information provided by the app under the URL in the body or comment of an issue or pull request.

![Content attachment](/assets/images/github-apps/content_reference_attachment.png)

To see content attachments, you must have a {% data variables.product.prodname_github_app %} that uses the Content Attachments API installed on the repository.{% ifversion fpt or ghec %} For more information, see "[Installing an app in your personal account](/articles/installing-an-app-in-your-personal-account)" and "[Installing an app in your organization](/articles/installing-an-app-in-your-organization)."{% endif %}

Content attachments will not be displayed for URLs that are part of a markdown link.

For more information about building a {% data variables.product.prodname_github_app %} that uses content attachments, see "[Using Content Attachments](/apps/using-content-attachments)."{% endif %}

## Uploading assets

You can upload assets like images by dragging and dropping, selecting from a file browser, or pasting. You can upload assets to issues, pull requests, comments, and `.md` files in your repository.

## Using emoji

You can add emoji to your writing by typing `:EMOJICODE:`.

`@octocat :+1: This PR looks great - it's ready to merge! :shipit:`

![Rendered emoji](/assets/images/help/writing/emoji-rendered.png)

Typing <kbd>:</kbd> will bring up a list of suggested emoji. The list will filter as you type, so once you find the emoji you're looking for, press **Tab** or **Enter** to complete the highlighted result.

For a full list of available emoji and codes, check out [the Emoji-Cheat-Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

## Paragraphs

You can create a new paragraph by leaving a blank line between lines of text.

{% ifversion fpt or ghae-issue-5180 or ghes > 3.2 or ghec %}
## Footnotes

You can add footnotes to your content by using this bracket syntax:

```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.
```

The footnote will render like this:

![Rendered footnote](![image](https://user-images.githubusercontent.com/61284764/156911775-29c3fe32-594e-4861-b77b-522a5c6f9c7a.png)
)

{% tip %}

**Note**: The position of a footnote in your Markdown does not influence where the footnote will be rendered. You can write a footnote right after your reference to the footnote, and the footnote will still render at the bottom of the Markdown.

{% endtip %}
{% endif %}

## Hiding content with comments

You can tell {% data variables.product.product_name %} to hide content from the rendered Markdown by placing the content in an HTML comment.

<pre>
&lt;!-- This content will not appear in the rendered Markdown --&gt;
</pre>

## Ignoring Markdown formatting

You can tell {% data variables.product.product_name %} to ignore (or escape) Markdown formatting by using <kbd>\\</kbd> before the Markdown character.

`Let's rename \*our-new-project\* to \*our-old-project\*.`

![Rendered escaped character](https://docs.github.com/assets/cb-2978/images/help/writing/escaped-character-rendered.png)

For more information, see Daring Fireball's "[Markdown Syntax](https://daringfireball.net/projects/markdown/syntax#backslash)."

{% ifversion fpt or ghes > 3.2 or ghae-issue-5232 or ghec %}

## Disabling Markdown rendering

{% data reusables.repositories.disabling-markdown-rendering %}

{% endif %}
