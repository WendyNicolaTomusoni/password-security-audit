## Password Security Audit

This project demonstrates a password security audit using John the Ripper on Kali Linux WSL.

## Tools Used
- John the Ripper
- Kali Linux WSL
- Git & GitHub

## Objective
To identify weak passwords through dictionary attacks on MD5 hashes.

## Results
Weak passwords such as admin, password, and qwerty were successfully cracked.


## Install John the Ripper

```bash
sudo apt update
sudo apt install john -y
```

## Create Wordlist

```bash
nano data/wordlist.txt
```

## Run John the Ripper

```bash
john --format=raw-md5 --wordlist=data/wordlist.txt data/hashes.txt
```

## Show Results

```bash
john --show --format=raw-md5 data/hashes.txt
```

## Save Results

```bash
john --show --format=raw-md5 data/hashes.txt > output/results.txt
```
