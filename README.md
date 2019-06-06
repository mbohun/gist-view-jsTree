# gist-view-jsTree
## [https://mbohun.github.io/gist-view-jsTree/](https://mbohun.github.io/gist-view-jsTree/)

#### dev notes
```BASH
./githubapi-get.sh $GITHUB_TOKEN /gists > my_gists.json
```
```BASH
cat my_gists.json \
    | jq '[ .[]|{"id":.id, "text":.description, "children":.files|keys, "state":{"opened":false,"disabled":false,"selected":false}}]' \
    > my_gists_jsTree.json
    
```
```JSON
[
  {
    "id": "81df9a27e90846ba913871b04d762c4f",
    "text": "Google API notes",
    "children": [
      "EXAMPLES.md",
      "HOWTO.md",
      "google_api_get_access_token.sh",
      "google_api_oauth2.0_authorization-00.png",
      "google_api_oauth2.0_authorization-01.png",
      "google_api_oauth2.0_authorization-02.png",
      "google_api_oauth2.0_authorization-03.png"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  },
  {
    "id": "23aab90d1af9069df22a60a03cfbfaa5",
    "text": "format issue",
    "children": [
      "issue.md"
    ],
    "state": {
      "opened": false,
      "disabled": false,
      "selected": false
    }
  }
]  
```
Copy my_gists_jsTree.json to gh-pages branch, git commit, git push.

#### REFERENCES:
- https://developer.github.com/v3/gists/#list-a-users-gists
- https://www.jstree.com/docs/json/
