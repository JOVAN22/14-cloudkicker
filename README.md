## Public IP
```
http://34.123.196.155

```

## Confirmation
> Flask bound to 127.0.0.1:5000, Nginx on 80

Flask is **NOT** exposed to the internet directly.  
All public traffic hits Nginx on port 80, which proxies internally to Flask on port 5000.

---

## Port Verification
```
LISTEN  127.0.0.1:5000  →  Flask  (localhost only, not public)
LISTEN  0.0.0.0:80      →  Nginx  (public-facing)
```
