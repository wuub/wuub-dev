README.md

--
ssh root@wuub.dev "git init --initial-branch=main --bare /root/wuub-dev.git"
scp ./hooks/post-receive root@wuub.dev:/root/wuub-dev.git/hooks/