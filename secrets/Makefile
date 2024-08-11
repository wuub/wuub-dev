PLAIN=$(wildcard *.plain)
SECRET=$(PLAIN:=.gpg)

decrypt:
	gpg --batch --yes --passphrase-file .encryption_password  *.gpg

encrypt: $(SECRET) 

%.plain.gpg: %.plain .encryption_password
	gpg --symmetric --batch --yes --passphrase-file .encryption_password $(basename $@)
