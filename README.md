# gist-view-jsTree
## [https://mbohun.github.io/gist-view-jsTree/](https://mbohun.github.io/gist-view-jsTree/)

#### dev notes
This is fully dynamic version:
- No need to pre-generate JSON input for the jsTree
- It uses the [fetch() API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) to access the GitHub REST API from the javascript inside index.html
- Simply copy index.html to `gh-pages` branch (or merge `master` to `gh-pages`), then git commit & git push `gh-pages`.

#### REFERENCES:
- https://developer.github.com/v3/gists/#list-a-users-gists
- https://www.jstree.com/docs/json/
