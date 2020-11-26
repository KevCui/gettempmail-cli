tempmail-cli
===========

A script to use [temp-mail](https://temp-mail.org/) service in terminal.

### Dependency

- [cURL](https://curl.haxx.se/download.html)
- [jq](https://stedolan.github.io/jq/)
- [faker-cli](https://github.com/lestoni/faker-cli)

### How to use

```
Usage:
  ./tempmail.sh [-i <inbox>|-c <inbox>|-d <uid>|-s]

Options:
  no option        Optional, randamly get an inbox
  -i <inbox>       Optional, get an inbox by its mail address
  -c <inbox>       Optional, delete inbox
  -d <uid>         Optional, delete mail by its uid
  -s               Optional, show available domains
  -h | --help      Display this help message

Examples:
  - Generate a random inbox:
    ~$ ./tempmail.sh

  - Get mails in test@temp-link.net:
    ~$ ./tempmail.sh -i test@temp-link.net

  - Delete inbox test@temp-link.net:
    ~$ ./tempmail.sh -c test@temp-link.net

  - Delete mail uUa4V5Hjmkqf9O:
    ~$ ./tempmail.sh -d uUa4V5Hjmkqf9O

  - Show all available domains:
    ~$ ./tempmail.sh -s
```

### Run tests

```
~$ bats test/tempmail.bats
```