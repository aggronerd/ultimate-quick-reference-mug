---
#Markdown (.md)
##Headers
	# h1
	## h2
	...
##Emphasis
	 *em*
	 **strong**
	 ***both***
##Code
	Double indent ...or...
```ruby 
foo = 'bar'
```
---
#Bash
```bash
if [ $# -eq 0 ]
  then
    echo "No arguments supplied"
fi
```
##Variables
	LAST_EXIT_CODE=$?
	FIRST_ARGUMENT=_$1 
##Conditionals
```bash
if [ ! -d "$DIRECTORY" ]; then

 -eq (arg1 is equal to arg2)
  -ne (arg1 is not equal to arg2)
  -lt (arg1 is less than arg2)
  -le (arg1 is less than or equal to arg2)
  -gt (arg1 is greater than arg2)
  -ge (arg1 is greater than or equal to arg2)
String operators
  -z string (length of string is zero)
  -n string (length of string is non-zero)
  string1 == string2 (strings are equal)
  string1 != string2 (string are not equal)
  string1 < string2 (string1 sorts before string2)
  string1 > string2 (string1 sorts after string2)
File operators
  -a file (file exists)
  -b file (file exists and is a block special)
  -c file (file exists and is a character special)
  -d file (file exists and is a directory)
  -e file (file exists)
  -f file (file exists and is a regular file)
  -g file (file exists and is set-group-id)
  -h file (file exists and is a symbolic link)
  -k file (file exists and is sticky)
  -p file (file exists and is a named pipe)
  -r file (file exists and is readable)
  -s file (file exists and has a size greater than zero)
  -t fd   (file descriptor is open and refers to a terminal)
  -u file (file exists and is set-user-id)
  -w file (file exists and is writable)
  -x file (file exists and is executable)
  -O file (file exists and is owned by the current user)
  -G file (file exists and is owned by the current user group)
  -L file (file exists and is a symbolic link)
  -S file (file exists and is a socket)
  -N file (file exists and has been modified since last read)
  file1 -nt file2 (file1 is newer by modification date than file2)
  file1 -ot file2 (file1 is older by modification date than file2)
  file1 -ef file2 (file1 and file2 have the same device and inode)
```
---
#GIT

---
#Postgres

---
#AWS Cli

---
#OpenSSL
```bash
Generate a new private key and Certificate Signing Request
openssl req -out CSR.csr -new -newkey rsa:2048 -nodes -keyout privateKey.key

Generate a self-signed certificate (see How to Create and Install an Apache Self Signed Certificate for more info)
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout privateKey.key -out certificate.crt

Generate a certificate signing request (CSR) for an existing private key
openssl req -out CSR.csr -key privateKey.key -new

Generate a certificate signing request based on an existing certificate
openssl x509 -x509toreq -in certificate.crt -out CSR.csr -signkey privateKey.key

Remove a passphrase from a private key
openssl rsa -in privateKey.pem -out newPrivateKey.pem
```