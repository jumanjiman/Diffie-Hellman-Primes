# Diffie-Hellman-Primes
A collection of Diffie-Hellman primes generated by random people, no idea if they are legitimate or not.

So it occurs to me that we have no corpus of data on Diffie Helman primes. With this in mind I would 
like to create one. Openssl command line can easily create them, using either the 2 (default) or 5 
generator (explained at 
http://security.stackexchange.com/questions/54359/what-is-the-difference-between-diffie-hellman-generator-2-and-5 ) 

For example the following code:

```
#!/bin/bash
for i in `seq 1 100`;
do
  openssl dhparam 2048 -text >> $i
done
```

will generate 100 2048 bit primes. If you can ideally simply commit the files to the following github repo,
simply create a directory in the root with your name/whatever you want to call it (nothing rude please) and
have a "2048" directory for the 2048 bit primes and a "4096" directory for the 4096 bit primes I would
appreciate it. If you use a tool other than OpenSSL command line to generate the primes please make a note of
it (especially any command line options used) in a .txt file in the root of your data directory. My goal is to
collect a few million primes of each size so we have some real data to work with.
