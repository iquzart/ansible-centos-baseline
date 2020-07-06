Baseline Setup
=========

Ansible role to setup OS baseline on RHEL based systems.
```
  1. Set Hostname
  2. Set Timezone
  3. configure date and time
  4. SELinux
  5. Password Policy
  6. Harden SSH
  7. Configure SNMP
  8. Logging
```

Role Variables
--------------

Basic Settings
```
hostname: jenkins-server
timezone: Asia/Dubai
ntp_server: 1.ae.pool.ntp.org
selinux_state: enforcing 
```

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
smtp_relay_host: smtp.domain.com
```

Aliases
```
admin_mail_id: user@domain.com
```



License
-------

MIT

Author Information
------------------

Muhammed Iqbal <iquart@hotmail.com>
