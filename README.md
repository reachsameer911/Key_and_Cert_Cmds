# Key_and_Cert_Cmds
Commands to create RSA and GPG key pair

Commands to create RSA and GPG Key pair:

X.509 commands:

Key Pair Creation:
openssl req -new -x509 -newkey rsa:2048  -keyout Private.key -out Public.crt -days 365 -nodes -sha256

Dump Private key contents:
openssl rsa -in Private.key -noout –text

Dump public key contents:
openssl x509 -in Public.crt -noout -text



GPG Commands:

Key pair creation:
gpg --gen-key

List gpg keys:
gpg --list-keys

Dump key contents:
gpg -a --export <key-name> | gpg --list-packets --debug 0x02

