# sshprox (a.k.a ATFP)
sshprox (a.k.a. AutoSSH Tunnelling for FreeBSD, Fun &amp; Profit)

---
These RC unit files use Autossh to enable several on-boot persistent tunnels.

## TODO (in order of priority)
1. Expand README.md with more detailed install/setup instructions
2. use either `INSTALL.sh` or `Makefile` for initial install
3. clean-up `rc` service files, remove redundancies, tighten service management functions (`start`, `stop`, `status`)
4. create additional script for creating new tunnel definitions
5. incorporate [goExpose](https://github.com/minyk/goexpose) & [jc](https://github.com/kellyjonbrazil/jc), for remote monitoring & management
6. possibly use growl/ gntp/ xmpp to send network alerts about sudden tunnel outages

## suggested Folder/ File Layout

- modifications to: `~/.ssh/config`
- modifications to: `/root/.ssh/config`

```
├── ~/bin/
|   └── get_sshprox
├── /tmp/
|   └── sshprox/
├── /etc
│  ├── hosts
│  └── rc.conf
└── /usr/
    └── local/
        └── etc/
            └── rc.d/
                └── sshprox
                    ├── sshprox_<TUNNEL_1>
                    ├── sshprox_<TUNNEL_...>
                    └── sshprox_<TUNNEL_N>
```
