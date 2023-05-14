# hello-world
MyTestRepo
#Adding some comments to my first git hub project


Open SSL command to create SSL certificate:
openssl req -x509 -newkey rsa:4096 -keyout PartyBPrivatekey.pem -out PartyBPubcert.pem -days 365

Command to create .p12 keystore
openssl pkcs12 -export -out partyA-as2.p12 -inkey PartyBPrivatekey.pem -in PartyBPubcert.pem

command to export public key as text
openssl x509 -in PartyAPubcert.pem -noout -pubkey > public_key.txt

Command to export private key as text
openssl rsa -in as2Privatekey.pem -noout -text > as2_private_key.txt

command to extart .cer file from cert.pem
openssl x509 -inform PEM -in as2cert.pem -outform DER -out as2CFTcert.cer
