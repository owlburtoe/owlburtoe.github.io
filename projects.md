# Projects

I use my homelab as a place to learn, break things, and then make them reliable again.  
Below are a few of the projects I plan to write up in more detail.

---

## Immich on Kubernetes with NFS storage

Running Immich in the k3s cluster with NFS backed persistent volumes from the Synology NAS.

I plan to document:

- how I designed the storage layout  
- how I handled ingress and certificates  
- how I tuned resources for the ML workloads  

---

## Single sign on with Authentik

Using Authentik to provide OIDC based login for multiple self hosted services under my own domain.

I plan to cover:

- setting up Authentik  
- integrating apps like Nginx Proxy Manager and others  
- managing users and access cleanly  

---

## Reverse proxy and DNS automation

Fronting my services with Nginx Proxy Manager and Cloudflare, so everything lives under clean subdomains with SSL.

I plan to cover:

- DNS configuration in Cloudflare  
- routing in Nginx Proxy Manager  
- how traffic flows from the internet to individual services  

---

More detailed writeups will go here as I continue to formalize what I already run in the lab.
