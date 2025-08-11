# CSF Installation

## Installation
```bash
cd /usr/src
rm -fv csf.tgz
tar -xzf csf.tgz
cd csf
sh install.sh
```

## Test iptables Modules
```bash
perl /usr/local/csf/bin/csftest.pl
```

## Remove APF+BFD
```bash
sh /usr/local/csf/bin/remove_apf_bfd.sh
```

## Kernel Logging Daemon
```bash
nano /etc/init.d/syslog
service syslog restart
```

## Perl Modules

### RPM
```bash
yum install perl-libwww-perl.noarch perl-LWP-Protocol-https.noarch perl-GDGraph
```

### APT
```bash
apt-get install libwww-perl liblwp-protocol-https-perl libgd-graph-perl
```

### CPAN
```bash
perl -MCPAN -eshell
cpan> install LWP LWP::Protocol::https GD::Graph
```

## InterWorx
```
InterWorx > NodeWorx > Plugins > csf
```

## Webmin
```
Webmin > Webmin Configuration > Webmin Modules
From local file: /usr/local/csf/csfwebmin.tgz
Install Module
```

## Uninstall
```bash
cd /etc/csf
sh uninstall.sh
```
