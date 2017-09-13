# Mail Subject decoder
A little tool for decoding email subjects to readable variant with encoding auto detection.

## Examples of usage
String decoding given as argument:
```
root@bt:~/ # subj-decoder =?UTF-8?B?QWN0aXZhdGUgdXNlciBhY2NvdW50?=
Decoded header: Activate user account
```

Decoding pipe-forwarded string:
```
root@~/ # exim -Mvh 1dr7zE-000725-53 | grep "Subject:" | awk '{print $3}' | xargs subj-decoder
Decoded header: Activate user account
```
Also you can convert many strings:
```
root@bt:~/ # subj-decoder =?UTF-8?Q?dodz1r?= =?iso-8859-1?q?p=F6stal?= =?utf-8?B?UkU6IHByb2Zlc3Npb25hbCBoYW5nZXIgbWFudWZhY3R1cmVy?=
Decoded header: dodz1r
Decoded header: pöstal
Decoded header: RE: professional hanger manufacturer
```
![Usage example](https://raw.githubusercontent.com/keedhost/subj-encode/master/img.JPG)

## Support and propositions
[Write me on Telegram](https://t.me/kondraryev1488)
