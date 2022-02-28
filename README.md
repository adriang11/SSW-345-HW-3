# REST Client
For the listBranches function, I edited index.js to take in owner and repo as a parameter for the path in getDefaultOptions() as specified by the GitHub API documentation for a get request.
For the createRepo function, I added "/user/repos" as a parameter for the path in getDefaultOptions() as specified by the GitHub API documentation for a post request. Additionally I specified that options.json be set to {"name":repo} which sets the name of the new repository as the repo input.
For the createIssue function, I added `/repos/${owner}/${repo}/issues` as a parameter for the path in getDefaultOptions() as specified by the GitHub API documentation for a post request. Additionally I specified that options.json be set to {"title":issueName, "body":issueBody} which sets the issue's name and body from input values.
Lastly, for the enableWikiSupport function, I added "/repos/${owner}/${repo}" as a parameter for the path in getDefaultOptions() as specified by the GitHub API documentation for a patch request. Additionally I specified that options.json be set to {"has_wiki":true} which updates the current value, thus enabling wiki support. I also changed the last line to resolve(body) as the json response is already parsed.

# REST Server
This exercise was fairly straightforward. I found that curl requests only worked in Git Bash on my machine so I completed it from there. The only modification I made was including the -s in the commands (short for silent) to hide a progress table that showed up and cluttered the terminal.
