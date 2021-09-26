# OpenSSL

Inspired e.g. by https://wiki.openssl.org/index.php/Command_Line_Utilities or https://www.keycdn.com/blog/openssl-tutorial :

1. [`openssl list`](../examples/openssl/list)

1. [`openssl enc`](../examples/openssl/enc)

1. [`openssl [gen]rsa`](../examples/openssl/rsa)

1. [`openssl` for EC`](../examples/openssl/ec) _ToDo - this doesn't work yet as-is_

1. [OpenSSL with TPM](../examples/openssl/tpm), after `sudo dnf install tpm2-tss-engine-utilities`.
   Based https://github.com/tpm2-software/tpm2-tss-engine from https://github.com/tpm2-software,
   see also https://wiki.archlinux.org/title/Trusted_Platform_Module.
   (NB: _TPM 2.0 requires UEFI boot; BIOS or Legacy boot systems can only use TPM 1.2.)_

<!-- TODO Inline content from scripts above and run it and update MD with output automatically -->


## ToDo

* Cert

* Generate private key on a YubiKey using PIV, see https://developers.yubico.com/PIV/.
  This is traditionally for non-web applications (although it should be possible to use for client certs, no?),
  and WebAuthn is the modern way to go instead.
