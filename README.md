## What it's used for

Script `spf_to_ip.sh` is used to query SPF DNS record of given mail domain
names and print converted IP addresses.

## USAGE

Run command with the mail domain names which you want to avoid gryelisting:

```shell
$ bash spf_to_ip.sh <domain> [domain ...]
```

For example:

```
$ bash spf_to_ip.sh google.com aol.com
```

it will print all IP addresses converted from spf record.

## Required commands:

* dig
* awk
* sed
* grep
* head
* tr

## KNOWN ISSUES

* not supported spf syntax:

    * ptr ptr:<domain>
    * a/24 a:<domain>/24
    * mx/24 mx:<domain>/24
    * exists:<domain>

## REFERENCES

* [SPF Record Syntax](http://www.open-spf.org/SPF_Record_Syntax)

## TODO

* support spf syntax: ptr ptr:<domain>
