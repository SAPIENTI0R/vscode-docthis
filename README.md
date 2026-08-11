# Document This

## Description

> This is a fork of [Document This](https://marketplace.visualstudio.com/items?itemName=oouo-diogo-perdigao.docthis) by Diogo Britto.  
> This fork adds support for HTML and NJK files to the extension, allowing you to generate JSDoc comments for JavaScript code inside `<script>` tags in .html and .njk files.

"Document This" is a Visual Studio Code extension that automatically generates detailed JSDoc comments for both TypeScript and JavaScript files.

![Demo showing the extension generating documentation on a class and the classes constructor method](images/demo.gif)

---

### Commands

#### Document at caret

Generates documentation for whatever the caret is on or inside of.

* Windows/Linux: `Ctrl+Alt+D` and again `Ctrl+Alt+D`
* MacOS: `Ctrl+Opt+D` and again `Ctrl+Opt+D`

#### Trace TypeScript syntax node

Prints info about the node ancestry at a given caret position.

* Windows/Linux: No default key binding
* MacOS: No default key binding

---

### Supported tags

Supports JSDoc and Closure Compiler tags: @class, @description, @enum, @export, @function, @implements, @interface, @param, @private, @returns or @return, @static, @template, @type, @memberOf and @date.

---

### Extension settings

| Setting | Description | Default |
|----|----|----|
| docthis.includeTypes | When enabled, type information is added to comment tags. | True |
| docthis.includeMemberOfOnClassMembers | When enabled, memberOf information is added to comment tags on class members. | True |
| docthis.includeMemberOfOnInterfaceMembers | When enabled, memberOf information is added to comment tags on interface members. | True |
| docthis.includeDescriptionTag | When enabled, JSDoc comments for functions and methods will include @description. | False |
| docthis.enableHungarianNotationEvaluation | When enabled, hungarian notation will be used as a type hint. | False |
| docthis.inferTypesFromNames | When enabled, will use names of params & methods as type hints. | False |
| docthis.includeAuthorTag | When enabled, will add the @author tag. | False |
| docthis.authorName | When docthis.includeAuthorTag is enabled, will add @author tag with this value. | None: Set the text for this tag by adding docthis.authorName to your settings file. |
| docthis.includeDateTag | When enabled, will add the @date tag in dd-mm-yyyy format. | False |
| docthis.returnsTag | Put @returns in place of @returns | False |

---

### List of all available formats for @date tag

| Mask | Description |
|----|----|
| `d` | Day of the month as digits; no leading zero for single-digit days. |
| `dd` | Day of the month as digits; leading zero for single-digit days. |
| `ddd` | Day of the week as a three-letter abbreviation. |
| `dddd` | Day of the week as its full name. |
| `m` | Month as digits; no leading zero for single-digit months. |
| `mm` | Month as digits; leading zero for single-digit months. |
| `mmm` | Month as a three-letter abbreviation. |
| `mmmm` | Month as its full name. |
| `yy` | Year as last two digits; leading zero for years less than 10. |
| `yyyy` | Year represented by four digits. |
| `h` | Hours; no leading zero for single-digit hours (12-hour clock). |
| `hh` | Hours; leading zero for single-digit hours (12-hour clock). |
| `H` | Hours; no leading zero for single-digit hours (24-hour clock). |
| `HH` | Hours; leading zero for single-digit hours (24-hour clock). |
| `M` | Minutes; no leading zero for single-digit minutes. |
| `MM` | Minutes; leading zero for single-digit minutes. |
| `N` | ISO 8601 numeric representation of the day of the week. |
| `o` | GMT/UTC timezone offset, e.g. -0500 or +0230. |
| `s` | Seconds; no leading zero for single-digit seconds. |
| `ss` | Seconds; leading zero for single-digit seconds. |
| `S` | The date's ordinal suffix (st, nd, rd, or th). Works well with `d`. |
| `l` | Milliseconds; gives 3 digits. |
| `L` | Milliseconds; gives 2 digits. |
| `t` | Lowercase, single-character time marker string: a or p. |
| `tt` | Lowercase, two-character time marker string: am or pm. |
| `T` | Uppercase, single-character time marker string: A or P. |
| `TT` | Uppercase, two-character time marker string: AM or PM. |
| `W` | ISO 8601 week number of the year, e.g. 42 |
| `Z` | US timezone abbreviation, e.g. EST or MDT. With non-US timezones or in the |
| `'...'`, `"..."` | Literal character sequence. Surrounding quotes are removed. |
| `UTC:` | Must be the first four characters of the mask. Converts the date from local time to UTC/GMT/Zulu time before applying the mask. The "UTC:" prefix is removed. |
