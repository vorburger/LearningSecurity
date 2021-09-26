# Security Concepts

## Identity

Principals are entities having identity, e.g. a human (you) or a computer server, or a program.


## Encryption




## Public-key cryptography

[Public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)...

One of the oldest such systems is called _RSA._ It is based on two large prime numbers:

1. ...

RSA is not the only public-key cryptography system. Another one is e.g.
[Elliptic-curve cryptography](https://en.wikipedia.org/wiki/Elliptic-curve_cryptography) (ECC).


## Keys

Both public and private keys can be represented in the PEM human-readable ASCII format, or binary DER format (used by Java).


## Signatures

_[Signing](https://en.wikipedia.org/wiki/Digital_signature)_ an input with a private key produces a _signature_ which can be _verified_ against the same input given a public key.

Input to signing is typically be limited in size.  Therefore a digest (hash) of an input file is used.


## Certificates

A [public key certificat](https://en.wikipedia.org/wiki/Public_key_certificate)
(also [this](https://en.wikipedia.org/wiki/Key_authentication#Authentication_using_Public_Key_Cryptography))
is used to prove the ownership of a public key by a _subject_ through a signature of it by an _issuer's_ private key.

Issuer can be trusted certificate authorities (CA), of which there may be hierarchy (chain) of certificates.
The _root_ CA certificate of the tree is _self signed._

X.509 is a [standard format](https://en.wikipedia.org/wiki/X.509#Structure_of_a_certificate) for certificates.
It also defines certificate revocation lists. Like keys, certificates' ASN.1 too can be in PEM and DER format.

[TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) (formerly SSL) is based on X.509.
The _subject's identity_ in a certificate is just a String which is interpreted by usage of the certificate;
e.g. in TLS, the Subject name (CN) is the hostname used to verify connections to a server having access
to the private key of the certificate, which it can use to descrypt session keys proposed by the client.
