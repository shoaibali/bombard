Debian/Ubuntu
=============

```
sudo apt-get install siege libgd-gd2-perl libchart-perl
```

Generate .siege.config
---------------------
run 'siege.config' to generate a new .siegerc file

```
siege.conf
```

New configuration template added to ${HOME}/.siegerc
Run siege -C to view the current settings in that file


### Set logfile in .siege.config

```
if cat ${HOME}/.siegerc | grep -v "#" | grep "\b" | grep "logfile"; then echo "logfile found"; else echo "adding logfile to .siegerc" && echo "logfile = ${HOME}/siege.log" >> ${HOME}/.siegerc;  fi;
```

