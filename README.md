# IRSX Api-H2H
## Transaksi
### Trx Request
POST /api/h2h
```
{
    "id": "OK0022",
    "pin": "xxxxx",
    "user": "xxxxx",
    "pass": "xxxxx"
    "idtrx":"1122",
    "kodeproduk":"S10",
    "tujuan":"081234567890",
    "jenis":1
}
```
### Trx Response
```
{
    "success": true,
    "tujuan": "08124125125",
    "kode": "S10",
    "reffid": "1124",
    "rc": "68",
    "sn": "",
    "status": 0,
    "msg": "Under proses"
}
```
## Cek Balance Request
POST /api/balance
```
{
    "id": "OK0022",
    "pin": "xxxxx",
    "user": "xxxxx",
    "pass": "xxxxx"
}
```

## Cek Balance Response
```
{
    "success": true,
    "rc": "00",
    "msg": "Cek Balance",
    "balance": 2999990000
}
```


## Cek Status Request
POST /api/status
```
{
    "id": "OK0022",
    "pin": "xxxxx",
    "user": "xxxxx",
    "pass": "xxxxx",
    "idtrx":"1122"
}
```
## Cek Status Response
### Transaction Success
```
{
    "success": true,
    "idtrx": "459",
    "tujuan": "081234567890",
    "kode": "S10",
    "reffid": "1122",
    "rc": "00",
    "sn": "03558600000923122366",
    "status": 1,
    "msg": "Success"
}
```
### Transaction Failed/Gagal
```
{
    "success": false,
    "idtrx": "459",
    "tujuan": "081234567890",
    "kode": "S10",
    "reffid": "1122",
    "rc": "02",
    "sn": "",
    "status": 2,
    "msg": "failed"
}
```
### Transaction Proses/Pending
```
{
    "success": true,
    "idtrx": "459",
    "tujuan": "081234567890",
    "kode": "S10",
    "reffid": "1122",
    "rc": "68",
    "sn": "",
    "status": 0,
    "msg": "process"
}
```
### Transaction Not Found
```
{
    "success": false,
    "idtrx": "",
    "tujuan": "",
    "kode": "",
    "reffid": "11221",
    "rc": "404",
    "sn": "",
    "status": 0,
    "msg": "Transaction not found"
}
```

## Negative Response:
```
{
    "success": false,
    "rc": "14",
    "msg": "user atau pasword salah"
}
```
```
{
    "success": false,
    "rc": "13",
    "msg": "PIN Tidak Sesuai"
}
```
