==============================
 Error while reading sideband
==============================

J'ai une erreur

Connection to bitbucket.org closed by remote host.KiB/s
fetch-pack: unexpected disconnect while reading sideband packet
fatal: early EOF
fatal: fetch-pack: invalid index-pack outpu

Donc j'ai fait :

export GIT_TRACE_PACKET=1
export GIT_TRACE=1
export GIT_CURL_VERBOSE=1

et

git config --global core.compression 0
git clone --depth 1 <repo_URI>
# cd to your newly created directory
git fetch --unshallow
git pull --all

et cela n'a pas marché j'ai toujours la meme erreur.
