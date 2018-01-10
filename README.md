# Maven2Gh
Simple process of a maven project compiled by travis and stored on Github pages

1 - register travis and enable the project CI
2 - create github token in https://github.com/settings/tokens/new
3 - add token in travis project settings (Environment Variables)
4 - create a new ssh key and add it as deploy key of the github project
5 - encrypt the private key with travis client (travis encrypt-file <file> -r USER/REPO)
6 - add encryption label from previous step in travis project settings (Environment Variables)
7 - modify deploy.sh for your needs, here it setup a local .m2 repository and
commit diff for a selected package (repository/com/epic/exmapleproject/*)

Thanks to :
 - https://gist.github.com/domenic/ec8b0fc8ab45f39403dd
 - https://docs.travis-ci.com/user/languages/java/