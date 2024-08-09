README.md

--
ssh root@wuub.dev "git init --initial-branch=main --bare /root/wuub-dev.git"
ssh root@wuub.dev "git clone /root/wuub-dev.git /root/wuub-dev"
scp ./hooks/post-receive root@wuub.dev:/root/wuub-dev.git/hooks/
