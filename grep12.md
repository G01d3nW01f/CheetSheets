#Taking Users to bruteforce

##smb

Using enum4linux
 
`./enum4linux.pl -U <rhost> | grep 'user:' | cut -d'[' -f2 | cut -d']' -f1 > Users`

Using nmap *smb-enum-users.nse*

`nmap <rhost> --script smb-enum-users.nse | grep "Full name:"`
