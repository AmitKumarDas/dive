## fingerprint
```sh
# retrieve SHA256 fingerprint of my SSH public key
$ ssh-keygen -lf ~/.ssh/id_rsa.pub

3072 SHA256:7DYNsDYMMbsss+jwrFnTH4YnnzBDBnvNlcnTCzzz xxxx2@xxxx2-a01.xxx.com (RSA)
```

```sh
# To get the GitHub (MD5) fingerprint format with newer versions of ssh-keygen
$ ssh-keygen -E md5 -lf ~/.ssh/id_rsa.pub

3072 SHA256:7DYNsDYMMbsss+jwrFnTH4YnnzBDBnvNlcnTCzzz xxxx2@xxxx2-a01.xxx.com (RSA)
```

```sh
# Worth noting that the fingerprint should be the same for both keys in a public / private keypair
# so the fingerprint of .ssh/id_rsa should be the same as the one for .ssh/id_rsa.pub
# So, you can use either one
```

```sh
# Alternative way to find your key
# Works on Ubuntu & Mac
$ ssh-add -l
3072 SHA256:7DYNsDYMMbxxxx+jwrFnTH4YnnzBDBnvNlcnTCCxxx sss@ss-a01.ddd.com (RSA)
```

```sh
# If however you get an error like:

Could not open a connection to your authentication agent

# Then it means that ssh-agent is not running
# You can start/run it with:

ssh-agent bash
```

```sh
# ssh authentication
$ ssh-add
Enter passphrase for /Users/amitd2/.ssh/id_rsa: __enter_your_ssh_pass__
Identity added: /Users/xxx/.ssh/id_rsa (xxx@xxx-a01.sss.com)
```

## Convert key to pem
- refer: https://gist.github.com/phrfpeixoto/8b04a2516ec559eddbfe7520ddde9ad2
```sh
# convert
$ ssh-keygen -f ~/.ssh/id_rsa.pub -e -m PKCS8 > id_rsa.pem.pub

# Use the public pem file to encrypt a string
echo "sometext" | openssl rsautl -encrypt -pubin -inkey ~/id_rsa.pub.pem > ~/encrypted.txt

# Or a file
cat ~/some_file.txt | openssl rsautl -encrypt -pubin -inkey ~/id_rsa.pub.pem > ~/encrypted.txt

# To decrypt, you'll need the private key
cat ~/encrypted.txt | openssl rsautl -decrypt -inkey path/to/id_rsa > ~/decrypted.txt
```
