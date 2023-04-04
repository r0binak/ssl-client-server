# Motivation

TLS (Transport Layer Security) and SSL (Secure Sockets Layer) are both cryptographic protocols that provide secure communication over the internet. SSL was the predecessor to TLS and was widely used for secure communication on the web until the release of TLS.

The main differences between TLS and SSL are:

- Security: TLS is generally considered more secure than SSL because it has fixed many of the vulnerabilities in SSL. TLS uses stronger encryption algorithms, has more secure key exchange protocols, and provides better protection against attacks such as man-in-the-middle attacks.

- Compatibility: TLS is backward compatible with SSL, meaning that servers and clients that support TLS can also support SSL. However, SSL is not forward compatible with TLS, meaning that if a server or client supports only SSL, it cannot communicate with a server or client that only supports TLS.

- Performance: TLS is generally faster than SSL because it uses more efficient cryptographic algorithms and has better support for parallel processing.

- Versions: TLS has different versions, such as TLS 1.0, TLS 1.1, TLS 1.2, and TLS 1.3, each with different security features and capabilities. SSL, on the other hand, has only a few versions, with SSL 3.0 being the most widely used.

In summary, TLS is a more secure and efficient version of SSL that has replaced SSL as the primary protocol for secure communication on the internet. Also, SSL is not natively supported by many programming languages. That's why I ended up using TLS.


# Prerequisites

Firstly, you need generate key:
```bash
openssl genpkey -algorithm RSA -out key.pem
```

Then, you can generate self-signed cert based on generated key:
```bash
openssl req -new -x509 -key key.pem -out cert.pem -days 3650
```
