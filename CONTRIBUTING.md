## Adding a new package

To add a package to this repository:

1. Create the custom package in 1Blocker on Mac.
2. Make sure the rule titles are short and on topic, starting with
`Block` or `Whitelist` and then the pattern. You can easily do this by
leaving the Title empty when you add or change the rule.
3. Add **one rule per host or script**. You can combine variations of
the same with regex, but without nested parenthesis. When you need to
do nesting split them into seperate rules. This is required to keep the
rules easy to understand.

Good:

```regex
//([\w\d]+\.)*(bad|evil)-corp\.net
/nightmare(\.min)?\.js
```

Bad:

```regex
(//([\w\d]+\.)*(bad|evil)-corp\.net|/nightmare(\.min)?\.js)
```

4. Export the custom package to file and run the contents through
CyberChef beatifier with _2 spaces_ indentation.
[Just use this one](https://snowplane.net/cyberchef.htm?recipe=%5B%7B%22op%22%3A%22JSON%20Beautify%22%2C%22args%22%3A%5B%22%20%20%22%5D%7D%5D)
5. Finally add the file ending in `.1blockpkg` to the repository and submit a Pull
Request.


## Updating a package

Just edit the file here in the repository and submit a Pull Request.
