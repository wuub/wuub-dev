PLAIN=$(wildcard *.plain)
ENCRYPT_SECRETS=$(PLAIN:=.gpg)

DECRYPT_PLAINS=$(wildcard *.gpg)


decrypt: $(basename $(DECRYPT_PLAINS)) 

%.plain: .encryption_password
	gpg --decrypt --out $@ --batch --yes --passphrase-file .encryption_password  $@.gpg	

encrypt: $(ENCRYPT_SECRETS) 

%.plain.gpg: %.plain .encryption_password
	gpg --symmetric --batch --yes --passphrase-file .encryption_password $(basename $@)

clean:
	rm *.plain
