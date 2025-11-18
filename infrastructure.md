# Infrastructure

This is the high level view of the environment I run at home.  
It behaves like a small production setup with a gateway, switching, storage, compute, identity, and an application layer.

![Homelab architecture diagram](architecture.png)

---

## Network

- UDM SE as gateway, firewall, and router  
- UniFi switching for internal connectivity  
- Cloudflare for DNS and public entry points  
- Nginx Proxy Manager on the NAS for reverse proxy and SSL  
- Everything behind the gateway, with internal services on the LAN

---

## Compute

- MS 01 as the main k3s control plane and worker node  
- GMK mini PC as an additional worker node  
- Raspberry Pi running Home Assistant bare metal  

The k3s cluster hosts most of the application workloads, while some services run directly on the NAS or the Pi.

---

## Storage

- Synology NAS providing NFS exports used as persistent volumes in Kubernetes  
- Media and data storage for apps like Plex, Immich, and others  
- ARR stack (Sonarr, Radarr and related services) running on the NAS  
- Backups and snapshots handled at the NAS level and by scheduled jobs

---

## Kubernetes

- k3s cluster for lightweight but fully featured orchestration  
- Ingress controller to route internal traffic from Nginx Proxy Manager to services  
- NFS backed persistent volumes for stateful workloads  
- Mix of media, automation, and utility services deployed as containers

---

## Identity and access

- Authentik providing OIDC and single sign-on across services  
- Centralized login experience under my own domain  
- Easier account management and a more consistent security model

---

## Applications

Some of the core services I run:

- Immich for photo management and machine learning based features  
- Plex, Overseerr and Tautulli for media  
- Kavita, Calibre and Audiobookshelf for books and audio  
- Vaultwarden for password management  
- ARR stack on the NAS for media automation  
- Home Assistant on the Raspberry Pi for home automation

This setup is always evolving, but the structure above is the foundation I build on.
