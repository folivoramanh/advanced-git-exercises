PS C:\Users\LENOVO> cd "C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises"                                   PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> curl https://api.github.com/users/nnja


StatusCode        : 200
StatusDescription : OK
Content           : {"login":"nnja","id":2030983,"
                    node_id":"MDQ6VXNlcjIwMzA5ODM=
                    ","avatar_url":"https://avatar
                    s.githubusercontent.com/u/2030
                    983?v=4","gravatar_id":"","url
                    ":"https://api.github.com/user
                    s/nnja","html_url":"...
RawContent        : HTTP/1.1 200 OK
                    Vary: Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With
                    X-GitHub-Media-Type:
                    github.v3; format=json
                    x-github-api-version-selected:
                     2022-11-28
                    Access-Control-Expose-Headers:
                     ETag, L...
Forms             : {}
Headers           : {[Vary, Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With],
                    [X-GitHub-Media-Type,                              github.v3; format=json], [x-gi                     thub-api-version-selected,                         2022-11-28], [Access-Control-E                     xpose-Headers, ETag, Link,                         Location, Retry-After,
                    X-GitHub-OTP,
                    X-RateLimit-Limit,
                    X-RateLimit-Remaining,
                    X-RateLimit-Used,
                    X-RateLimit-Resource,
                    X-RateLimit-Reset,
                    X-OAuth-Scopes,
                    X-Accepted-OAuth-Scopes,
                    X-Poll-Interval,
                    X-GitHub-Media-Type,
                    X-GitHub-SSO,
                    X-GitHub-Request-Id,
                    Deprecation, Sunset]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 1218



PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> Invoke-WebRequest -URI https://api.github.com/users/nnja


StatusCode        : 200
StatusDescription : OK
Content           : {"login":"nnja","id":2030983,"
                    node_id":"MDQ6VXNlcjIwMzA5ODM=
                    ","avatar_url":"https://avatar
                    s.githubusercontent.com/u/2030
                    983?v=4","gravatar_id":"","url
                    ":"https://api.github.com/user
                    s/nnja","html_url":"...
RawContent        : HTTP/1.1 200 OK
                    Vary: Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With
                    X-GitHub-Media-Type:
                    github.v3; format=json
                    x-github-api-version-selected:
                     2022-11-28
                    Access-Control-Expose-Headers:
                     ETag, L...
Forms             : {}
Headers           : {[Vary, Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With],
                    [X-GitHub-Media-Type,
                    github.v3; format=json], [x-gi                     thub-api-version-selected,                         2022-11-28], [Access-Control-E                     xpose-Headers, ETag, Link,                         Location, Retry-After,
                    X-GitHub-OTP,
                    X-RateLimit-Limit,
                    X-RateLimit-Remaining,
                    X-RateLimit-Used,
                    X-RateLimit-Resource,
                    X-RateLimit-Reset,
                    X-OAuth-Scopes,
                    X-Accepted-OAuth-Scopes,
                    X-Poll-Interval,
                    X-GitHub-Media-Type,
                    X-GitHub-SSO,
                    X-GitHub-Request-Id,
                    Deprecation, Sunset]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 1218



PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> Invoke-WebRequest -URI "https://api.github.com/search/repositories?q=user:nnja&sort=stars&per_page=1" | Select-String "stargazers_count"

{"total_count":49,"incomplete_results":false,"item
s":[{"id":105804084,"node_id":"MDEwOlJlcG9zaXRvcnk
xMDU4MDQwODQ=","name":"advanced-git","full_name":"
nnja/advanced-git","private":false,"owner":{"login
":"nnja","id":2030983,"node_id":"MDQ6VXNlcjIwMzA5O
DM=","avatar_url":"https://avatars.githubuserconte
nt.com/u/2030983?v=4","gravatar_id":"","url":"http
s://api.github.com/users/nnja","html_url":"https:/
/github.com/nnja","followers_url":"https://api.git
hub.com/users/nnja/followers","following_url":"htt
ps://api.github.com/users/nnja/following{/other_us
er}","gists_url":"https://api.github.com/users/nnj
a/gists{/gist_id}","starred_url":"https://api.gith
ub.com/users/nnja/starred{/owner}{/repo}","subscri
ptions_url":"https://api.github.com/users/nnja/sub
scriptions","organizations_url":"https://api.githu
b.com/users/nnja/orgs","repos_url":"https://api.gi
thub.com/users/nnja/repos","events_url":"https://a
pi.github.com/users/nnja/events{/privacy}","receiv
ed_events_url":"https://api.github.com/users/nnja/
received_events","type":"User","site_admin":false}
,"html_url":"https://github.com/nnja/advanced-git"
,"description":"Frontend Masters Advanced Git -
by Nina Zakharenko","fork":false,"url":"https://ap
i.github.com/repos/nnja/advanced-git","forks_url":
"https://api.github.com/repos/nnja/advanced-git/fo
rks","keys_url":"https://api.github.com/repos/nnja
/advanced-git/keys{/key_id}","collaborators_url":"
https://api.github.com/repos/nnja/advanced-git/col
laborators{/collaborator}","teams_url":"https://ap
i.github.com/repos/nnja/advanced-git/teams","hooks
_url":"https://api.github.com/repos/nnja/advanced-
git/hooks","issue_events_url":"https://api.github.
com/repos/nnja/advanced-git/issues/events{/number}
","events_url":"https://api.github.com/repos/nnja/
advanced-git/events","assignees_url":"https://api.
github.com/repos/nnja/advanced-git/assignees{/user
}","branches_url":"https://api.github.com/repos/nn
ja/advanced-git/branches{/branch}","tags_url":"htt
ps://api.github.com/repos/nnja/advanced-git/tags",
"blobs_url":"https://api.github.com/repos/nnja/adv
anced-git/git/blobs{/sha}","git_tags_url":"https:/
/api.github.com/repos/nnja/advanced-git/git/tags{/
sha}","git_refs_url":"https://api.github.com/repos
/nnja/advanced-git/git/refs{/sha}","trees_url":"ht
tps://api.github.com/repos/nnja/advanced-git/git/t
rees{/sha}","statuses_url":"https://api.github.com
/repos/nnja/advanced-git/statuses/{sha}","language
s_url":"https://api.github.com/repos/nnja/advanced
-git/languages","stargazers_url":"https://api.gith
ub.com/repos/nnja/advanced-git/stargazers","contri
butors_url":"https://api.github.com/repos/nnja/adv
anced-git/contributors","subscribers_url":"https:/
/api.github.com/repos/nnja/advanced-git/subscriber
s","subscription_url":"https://api.github.com/repo
s/nnja/advanced-git/subscription","commits_url":"h
ttps://api.github.com/repos/nnja/advanced-git/comm
its{/sha}","git_commits_url":"https://api.github.c
om/repos/nnja/advanced-git/git/commits{/sha}","com
ments_url":"https://api.github.com/repos/nnja/adva
nced-git/comments{/number}","issue_comment_url":"h
ttps://api.github.com/repos/nnja/advanced-git/issu
es/comments{/number}","contents_url":"https://api.
github.com/repos/nnja/advanced-git/contents/{+path
}","compare_url":"https://api.github.com/repos/nnj
a/advanced-git/compare/{base}...{head}","merges_ur
l":"https://api.github.com/repos/nnja/advanced-git
/merges","archive_url":"https://api.github.com/rep
os/nnja/advanced-git/{archive_format}{/ref}","down
loads_url":"https://api.github.com/repos/nnja/adva
nced-git/downloads","issues_url":"https://api.gith
ub.com/repos/nnja/advanced-git/issues{/number}","p
ulls_url":"https://api.github.com/repos/nnja/advan
ced-git/pulls{/number}","milestones_url":"https://
api.github.com/repos/nnja/advanced-git/milestones{
/number}","notifications_url":"https://api.github. com/repos/nnja/advanced-git/notifications{?since,a ll,participating}","labels_url":"https://api.githu b.com/repos/nnja/advanced-git/labels{/name}","rele ases_url":"https://api.github.com/repos/nnja/advan ced-git/releases{/id}","deployments_url":"https://
api.github.com/repos/nnja/advanced-git/deployments
","created_at":"2017-10-04T18:35:50Z","updated_at"
:"2023-08-08T18:18:14Z","pushed_at":"2021-08-29T14
:51:15Z","git_url":"git://github.com/nnja/advanced
-git.git","ssh_url":"git@github.com:nnja/advanced-
git.git","clone_url":"https://github.com/nnja/adva
nced-git.git","svn_url":"https://github.com/nnja/a
dvanced-git","homepage":"http://frontendmasters.co
m/workshops/git-indepth/","size":9709,"stargazers_
count":726,"watchers_count":726,"language":null,"h
as_issues":true,"has_projects":true,"has_downloads
":true,"has_wiki":true,"has_pages":false,"has_disc
ussions":false,"forks_count":540,"mirror_url":null
,"archived":false,"disabled":false,"open_issues_co
unt":1,"license":null,"allow_forking":true,"is_tem
plate":false,"web_commit_signoff_required":false,"
topics":[],"visibility":"public","forks":540,"open
_issues":1,"watchers":726,"default_branch":"master
","score":1.0}]}


PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> curl "https://api.github.com/repos/nodejs/node/languages"


StatusCode        : 200
StatusDescription : OK
Content           : {"JavaScript":13282342,"C++":4
                    766766,"Python":2353499,"C":61
                    3336,"HTML":163390,"Shell":992
                    27,"Makefile":53723,"Batchfile
                    ":41870,"Emacs Lisp":14363,"Pe
                    rl":11715,"R":8037,"TypeScript
                    ":702,"Assembly":157...
RawContent        : HTTP/1.1 200 OK
                    Vary: Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With
                    X-GitHub-Media-Type:
                    github.v3; format=json
                    x-github-api-version-selected:
                     2022-11-28
                    Access-Control-Expose-Headers:
                     ETag, L...
Forms             : {}
Headers           : {[Vary, Accept,
                    Accept-Encoding, Accept,
                    X-Requested-With],
                    [X-GitHub-Media-Type,
                    github.v3; format=json], [x-gi
                    thub-api-version-selected,
                    2022-11-28], [Access-Control-E
                    xpose-Headers, ETag, Link,
                    Location, Retry-After,
                    X-GitHub-OTP,
                    X-RateLimit-Limit,
                    X-RateLimit-Remaining,
                    X-RateLimit-Used,
                    X-RateLimit-Resource,
                    X-RateLimit-Reset,
                    X-OAuth-Scopes,
                    X-Accepted-OAuth-Scopes,
                    X-Poll-Interval,
                    X-GitHub-Media-Type,
                    X-GitHub-SSO,
                    X-GitHub-Request-Id,
                    Deprecation, Sunset]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 217



PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  