# Installation notes

## master.key and credentials 
Because it's not good practice to share secrets. This repo is missing a `master.key` file, therefore it is unable to unencrypt `credentials.yml.enc`. For knock to run correctly it requires a *secret_key_base* As such you may encounter an error when trying to generate a jwt if you haven't dealt with this. The best course of action is to delete `credentials.yml.enc` and then run 

```
EDITOR="code --wait" rails credentials:edit
``` 
In your ternimal, this will generate a new `master.key` and `credentials.yml.enc`