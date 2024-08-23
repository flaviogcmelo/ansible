### CentOS ###
```shell
  sudo yum -y install epel-release

  sudo yum -y install python3 python3-bcrypt

  python3 -c 'import crypt,getpass;pw=getpass.getpass();print(crypt.crypt(pw) if (pw==getpass.getpass("Confirm: ")) else exit())'

``` 



## Basic Command from ansible
```shell

ansible all -i localhost, -m debug -a "msg={{ 'W3lcome#' | password_hash('sha512', 'POC-IBM#Inep2024') }}"

"$6$POC-IBM#Inep2024$/3jW9n/G3OlAMzfzxOniK2ewrWSBxqmcbzj61AZbwY7ASgz6Awey73VT/X9Az1P30htGIgLS5P7Sbpssc4HI20"
```
