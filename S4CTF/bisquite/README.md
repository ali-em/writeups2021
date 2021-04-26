# Bisquite

## Description

May we have some [bisquite](bisquite)

## Files provided

An archive containing [bisquite](bisquite)

## Writeup

Running `binwalk` on the file we get the following result:

![binwalk output](screenshots/binwalk.png)

So there is a file system from address 1099776 that we probably can mount it. But first we can skip the first 1099776 bytes.

So we skip the first bytes and output it in a file called skipped, using `dd` command as below:

```
dd if=bisquite of=skipped skip=1099776 bs=1
```
