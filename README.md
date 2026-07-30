# curl to fetch

Paste a curl command and get JavaScript fetch and Python requests code, generated entirely in your browser.

**Live demo:** https://0xelitesystem.github.io/curl-to-fetch/

## Use

1. Open the page (or the live demo above).
2. Paste a curl command into the box. Multi-line commands with backslash, caret, or backtick line continuations are fine.
3. Read the generated code in the two tabs: JavaScript (fetch) and Python (requests).
4. Click Copy to put either snippet on your clipboard.

The converter understands the common curl options: the URL, `-X/--request`, `-H/--header`, `-d/--data`, `--data-raw`, `--data-binary`, `--data-urlencode`, `--json`, `-F/--form`, `-u/--user`, `-b/--cookie`, `-A/--user-agent`, `-e/--referer`, `-G/--get`, `-I/--head`, `-k/--insecure`, and `--url`. It infers the HTTP method (a body means POST unless you set the method yourself), picks the right Content-Type, parses JSON and form bodies into idiomatic structures, and shows a note when something cannot be represented (for example, a body read from a local file).

## Why this exists

Most "curl to code" sites send the command you paste to a server. A curl command often carries bearer tokens, cookies, and API keys, so that is exactly the kind of thing you do not want to upload. This tool is a single HTML file with no backend, no analytics, and no third-party scripts. The conversion runs as plain JavaScript on your own machine. It is MIT licensed, so you can read every line, fork it, or host your own copy.

## Privacy

Everything runs in your browser. Nothing you paste is sent anywhere. There are no network requests, no cookies, no analytics, and no external fonts or libraries. You can confirm this by opening your browser dev tools network tab while you use the page, or by loading the file with your network disconnected.

## Run locally

```
git clone https://github.com/0xelitesystem/curl-to-fetch.git
cd curl-to-fetch
```

Then open `index.html` in any browser by double-clicking it, or serve the folder:

```
python -m http.server
```

and visit http://localhost:8000.

## Build

There is no build step and there are no dependencies. The whole tool is one `index.html` file with inline CSS and JavaScript. Edit it and reload.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. See [LICENSE](LICENSE).

## Related

- https://github.com/0xelitesystem/jwt-inspector
- https://github.com/0xelitesystem/eeat-signals-reference
