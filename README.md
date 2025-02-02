# ![HomelabOS](https://gitlab.com/NickBusey/HomelabOS/raw/master/static/logo.png)

Your very own offline-first open-source data-center! Includes over 50 services!

## Beta Software Warning

This software has not reached version 1.0 and should therefore be considered unstable. While any tagged version should work well on its own, a nice friendly upgrade path from one version to another is not guaranteed.

If you like getting your hands dirty in early versions of software, this is for you. If you prefer to wait till things are stable and friendly, maybe hold off for a while.

Also, if you trash your server or wreck your data, that's on you. Test your backups. Trust nothing.

## [Documentation](https://nickbusey.gitlab.io/HomelabOS/)

## Summary

A set of Ansible scripts to configure a Docker based Homelab server with all sorts of goodies. Following the unix philosophy we gather together many specific tools to build the exact end result desired.

## Goals

To make it easy for anyone to own all their data in an easy and secure way, without the need of cloud providers.

## Features

- One command deployment
- Automated Backups
- Easy Restore
- Automated Apple Health Data import
- Automated Tor Onion Service access
- Automated HTTPS via LetsEncrypt
- [Automated Settings Sync](https://nickbusey.gitlab.io/HomelabOS/setup/installation/#syncing-settings-via-git)
- OpenVPN
- OpenLDAP
- Cloud Bastion Server with Tinc VPN

### [Planned Features](https://gitlab.com/NickBusey/HomelabOS/issues?label_name%5B%5D=enhancement)

## [Installation Tutorial / Demo](https://youtu.be/p8cD349BGRI)

### Local Demo

If you have the latest version of Vagrant and Virtual Box setup you can demo things locally by running `make develop`. This will spin up a temporary developer copy on your local computer without needing an actual server to point things at. Note no data will actually be saved from inside the VM, so this is for testing only.

## Available Software

- [Airsonic](https://airsonic.github.io/) - Airsonic is a free, web-based media streamer, providing ubiquitous access to your music.
- [Beets](https://beets.io) - Beets is the media library management system for obsessive-compulsive music geeks.
- [Bitwarden](https://bitwarden.com/) - Password and secrets manager via [bitwarden-rs](https://github.com/dani-garcia/bitwarden_rs)
- [BookStack](https://www.bookstackapp.com/) - Simple & Free Wiki Software
- [BulletNotes](https://gitlab.com/NickBusey/BulletNotes.git) - Note taking application
- [Calibre](https://calibre-ebook.com) - Complete ebook library management.
- [Code-Server](https://github.com/codercom/code-server) - Run VS Code on a remote server.
- [Darksky](http://darksky.net/) - Local weather reported via [darksky-influxdb](https://github.com/ErwinSteffens/darksky-influxdb)
- [Dasher](https://github.com/maddox/dasher) - Amazon Dash button support
- [Documentation](https://nickbusey.gitlab.io/HomelabOS/) - Offline, searchable documentation via [MkDocs](https://www.mkdocs.org/)
- [Drone](https://drone.io) - Drone is a self-service continuous delivery platform
- [Emby](https://emby.media/) - Personal Media Server
- [Firefly III](https://firefly-iii.org/) - Money management budgeting app
- [FreshRSS](https://freshrss.org) - A free, self-hostable aggregator
- [Ghost](https://ghost.org/) - Ghost is a platform for building and running a modern online publication
- [Gitea](https://gitea.io/en-US/) - Git hosting
- [Grafana](https://grafana.com/) - Pretty graphs
- [Guacamole](https://guacamole.apache.org) - a clientless remote desktop gateway
- [Home Assistant](https://www.home-assistant.io/) - Home Automation
- [Homedash](https://lamarios.github.io/Homedash2/) - Dashboard
- [InfluxDB](https://www.influxdata.com/time-series-platform/influxdb/) - Time series data storage
- [Inventario](https://gitlab.com/NickBusey/inventario) - Home inventory management
- [Jackett](https://github.com/Jackett/Jackett) - API Support for your favorite torrent trackers (helps Sonarr and Radarr)
- [Jellyfin](https://github.com/jellyfin/jellyfin) - The Free Software Media System
- [Kibitzr](https://kibitzr.github.io/) - IFTTT replacement
- [Lidarr](https://lidarr.audio) - Sonarr but for Music.
- [Mailserver](https://github.com/hardware/mailserver/) - Fully featured mail server
- [Mashio](https://gitlab.com/NickBusey/mashio) - Home brewery management software
- [Matomo](https://matomo.org/) - Web analytics
- [Mayan EDMS](https://gitlab.com/mayan-edms/mayan-edms) - Free Open Source DMS (document management system).
- [Minio](https://minio.io/) - S3 hosting
- [Miniflux](https://miniflux.app/) - Miniflux is a minimalist and opinionated feed reader.
- [Monica](https://www.monicahq.com/) - Contact / relationship manager
- [NetData](http://my-netdata.io/) - Monitor your systems and applications, the right way!
- [NextCloud](https://nextcloud.com/) - Private Cloud Storage, Calendar, Contacts, etc.
- [Organizr](https://github.com/causefx/Organizr) - Access all your HomelabOS services in one easy place.
- [OwnPhotos](https://github.com/hooram/ownphotos) Self hosted Google Photos clone.
- [Paperless](https://github.com/danielquinn/paperless) - Document management
- [phpLDAPadmin](https://github.com/osixia/docker-phpLDAPadmin) - LDAP management interface
- [Pi-hole](https://pi-hole.net/) - Ad blocking
- [Piwigo](https://piwigo.org/) - Manage your photo collection
- [Plex](https://www.plex.tv/) - Personal Media Server
- [Portainer](https://www.portainer.io/) - Easy Docker management
- [Radarr](https://radarr.video/) - Automated movie downloading
- [Sonarr](https://sonarr.tv/) - Automated TV downloading
- [Syncthing](https://syncthing.net/) - File syncing software
- [Telegraf](https://www.influxdata.com/time-series-platform/telegraf/) - Server statistics reporting
- [The Lounge](https://thelounge.chat/) - Always-on IRC client (IRC bouncer)
- [Transmission](https://transmissionbt.com/) - BitTorrent client
- [Wallabag](https://wallabag.org/en) - Save and classify articles. Read them later. Freely.
- [WebVirtMg](https://github.com/retspen/webvirtmgr) is a complete Kernel Virtual Machine (KVM) hypervisor manager.
- [Zulip](https://github.com/zulip/zulip) - Threaded chat software

## Requirements

A server with:

- Ubuntu 18.04 and passwordless SSH via SSH keys

Another computer with:

- Docker

## Optional Items

### Domain Name

A domain configured with a `A` type DNS record of `*.yourdomain.com` pointed at your server's IP address. (This is optional because you can use Tor to access your services without registering a domain. For best support from 3rd party clients an actual domain is highly recommended. Also certain services do not work through TOR at the moment.) Note you can hang this off a subdomain as well, so `*.homelab.yourdomain.com` will work as well.

### Port Forwarding

Ports 80 and 443 punched through any firewalls and port forwarded at your server in question. (This is also optional due to Tor access, but again highly recommended.)

### [Cloud Bastion Server](https://nickbusey.gitlab.io/HomelabOS/setup/tinc/)

Rather than pointing the domain at your home IP and having to manage DDNS, you can utilize a cloud server
to act as a bastion host via Tinc vpn and nginx.

## [Installation](https://nickbusey.gitlab.io/HomelabOS/setup/installation/)

## Alternatives

- [Ansible NAS](https://github.com/davestephens/ansible-nas)
- [DockSTARTer](https://dockstarter.com/)

## Get Support

- [File an issue](https://gitlab.com/NickBusey/HomelabOS/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=)
- [Ask a question on Reddit](https://www.reddit.com/r/HomelabOS/)
- Threaded support and development discussion on [Zulip](https://homelabos.zulipchat.com/)

## Give Support

[Become a Supporter on Patreon](https://www.patreon.com/nickbusey)

## [Contributing](https://nickbusey.gitlab.io/HomelabOS/development/contributing/)

## Watch Live Development

You can watch live development of this project on [Nick Busey's Twitch Stream](https://www.twitch.tv/nickbusey).
