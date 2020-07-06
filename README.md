Baseline Setup
=========

Ansible role to setup OS baseline on RHEL based systems.


Role Variables
--------------

```
selinux_state: enforcing 
``

Password Policy
```
PASS_MAX_DAYS: 60
PASS_MIN_DAYS: 1
PASS_MIN_LEN: 12
PASS_WARN_AGE: 7
minlen: 12
minclass: 4 
```

Number of days to disable inactive account after password expiry
```
disable_inactive_account: 60
```

PAM Settings
```
account_lockout_max_try: 5
unlock_time: 900
password_remember: 5
```

SNMP Settings 
```
enable_snmp: true
monitoring_host: 192.168.122.1
snmp_string: My$cR3t$tr!ng
```

SSH Settings 
```
Port: 22
MaxAuthTries: 4
IgnoreRhosts: 'yes'
HostbasedAuthentication: 'no'
PermitRootLogin: 'yes'
PermitEmptyPasswords: 'no'
ClientAliveInterval: 300
ClientAliveCountMax: 0
LoginGraceTime: 1m
Banner: /etc/issue.net
AllowTcpForwarding: 'no'
maxstartups: 10:30:60
maxsessions: 4
```

MTA
```
enable_mta: true
```


License
-------

MIT

Author Information
------------------

Muhammed Iqbal <iquart@hotmail.com>
