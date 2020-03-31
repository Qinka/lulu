# lulu
Dynamic DNS?


## Usage

First:

```bash
source `which lulu`
```


### Look up ip for interface

```bash
lookup_if_ipv4 [-i INTERFACE] [-n N]
```

**INTERFACE**: ethernet interface, like eth0, wifi0, enp1s0

**N** offset`[=2]`

### Look up ip via taobao API

```bash
lookup_ip_taobao
```

### Get records list of DNSPOD

```bash
dnspod_list_record -k TOKEN -d DOMAIN [-o OFFSET] [-l LENGTH]
```

**TOKEN** API TOKEN for dnsapi

**DOMAIN** domain

**OFFSET** offset`[=0]`

**LENGTH** length`[=3000]`

### Update one record of DNSPOD

```bash
dnspod_update_record -k TOKEN -d DOMAIN -s SUB_DOMAIN -t RECORD_TYPE -i RECORD_ID -v VALUE -l LINE
```

**TOKEN** API TOKEN for dnsapi

**DOAMIN** domain

**SUB_DOAMIN** sub domain

**RECORD_TYPE** record type, such A, AAAA, CNAME

**RECORD_ID** record id (get from `dnspod_list_record`)

**VALUE** value

**LINE** line`[=0]`
