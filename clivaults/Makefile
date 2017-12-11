PWD	:=	$(pwd)
VAULT_VERSION	:=	0.9.0
VAULT_DIR	:=	clivaults
VAULT_ZIP_FILE	:=	vault_$(VAULT_VERSION)
#_$(OSNAME).zip

download.linux:
	cd /tmp
	curl -O https://releases.hashicorp.com/vault/$(VAULT_VERSION)/vault_$(VAULT_VERSION)_linux_amd64.zip
	unzip vault_$(VAULT_VERSION)_linux_amd64.zip
	mv vault vault-Linux
	rm -fv *.zip

download.osx:
	cd /tmp
	curl -O https://releases.hashicorp.com/vault/$(VAULT_VERSION)/vault_$(VAULT_VERSION)_darwin_amd64.zip
	unzip vault_$(VAULT_VERSION)_darwin_amd64.zip
	mv vault vault-Darwin
	rm -fv *.zip


git.push:
	git add *
	git commit -m "Next Version $(date +'%Y.%M.%D')"
	git push
