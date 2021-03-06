```
╭──────┬─╮                       ╭─────╮
│        │                       │     │
│      ╭─╯╭───╮╭───╮ ╭──────╮    ├─────┤╭──────╮╭──────╮╭────┬─╮╭──────╮
│      ╰─╮├───┤│   │ │  ──  │    │     ││   ╭──╯│   ╭╮ ││      ││  ────┤
│      ╭─╯│   ││   │ │      │    │     ││   ╰──╮│   ││ ││   ╭╮ ││      │
│      │  │   ││   │ │  ────┤    │     ││      ││   ╰╯ ││   ││ │├────  │
╰──────╯  ╰───╯╰───╯ ╰──────╯    ╰─────╯╰──────╯╰──────╯╰───╯╰─╯╰──────╯
╭─╮ ╭─╮ ┬─╮    ╭─╮ ┬ ┬ ╭─╮   ╭─╮ ╭─╮ ╭─╮ ┬   ┬ ╭─╮ ╭─╮ ╭┬╮ ┬ ╭─╮ ╭╮╭ ╭─╮
├┤  │ │ ├┬╯    ├─╯ ├─┤ ├─╯   ├─┤ ├─╯ ├─╯ │   │ │   ├─┤  │  │ │ │ │││ ╰─╮
┴   ╰─╯ ┴╰─    ┴   ┴ ┴ ┴     ┴ ┴ ┴   ┴   ┴─╯ ┴ ╰─╯ ┴ ┴  ┴  ┴ ╰─╯ ╯╰╯ ╰─╯
```
> File specific icons for PHP. A port of Atom File-icons, https://github.com/file-icons/atom

<img alt="Icon previews" width="850" src="https://raw.githubusercontent.com/file-icons/atom/6714706f268e257100e03c9eb52819cb97ad570b/preview.png" />

## Install

1- Use `Composer` to install as follows, 

```bash
composer require websemantics/file-icons
```

## Getting Started

Create an instance of `FileIcons` class.

```php
use Websemantics\FileIcons\FileIcons;

$icons = new FileIcons();
```

Include `css` styles in the header of an html document. This will generate a `link` tag that points to the package stylesheet.

```php
FileIcons::includeCss();
```

Get the class name of the icon that represent a filename, for example `text-icon`.

```php
$filename = 'src/index.php';
$class_name = $icons->getClass($filename);
```

You can also get a class name of the associated icon color.

```php
$filename = 'README.md';
$class_name = $icons->getClassWithColor($filename);
```

Use the class name to generate html, for example

```php
echo "<a><i class='$class_name'></i>$filename</a>";
```

Check out - [Markdown Browser Plus](https://github.com/websemantics/markdown-browser-plus) to see implementation details.

## Resources

- [Atom File Icons](https://github.com/file-icons/atom), file specific icons for improved visual grepping.
- [Markdown Browser Plus](https://github.com/websemantics/markdown-browser-plus), Github flavoured, local file browser for viewing markdown documentation files.

## Support

Need help or have a question? post at [StackOverflow](https://stackoverflow.com/questions/tagged/file-icons+websemantics).

*Please don't use the issue trackers for support/questions.*

*Star if you find this project useful, to show support or simply for being awesome :)*

## Contribution

Contributions to this project are accepted in the form of feedback, bugs reports and even better - pull requests.

## License

[MIT license](http://opensource.org/licenses/mit-license.php) Copyright (c) Web Semantics, Inc.