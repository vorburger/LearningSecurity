# OpenSSL

Inspired e.g. by https://wiki.openssl.org/index.php/Command_Line_Utilities or e.g. https://www.keycdn.com/blog/openssl-tutorial at al:

1. [`openssl list`](../examples/openssl/list)

1. [`openssl enc`](../examples/openssl/enc)

1. [`openssl [gen]rsa`](../examples/openssl/rsa)

1. [`openssl` for EC](../examples/openssl/ec) _ToDo - this doesn't work yet as-is_

1. [OpenSSL with TPM](../examples/openssl/tpm), after `sudo dnf install tpm2-tss-engine-utilities`.
   Based https://github.com/tpm2-software/tpm2-tss-engine from https://github.com/tpm2-software,
   see also https://wiki.archlinux.org/title/Trusted_Platform_Module.
   (NB: _TPM 2.0 requires UEFI boot; BIOS or Legacy boot systems can only use TPM 1.2.)_

1. [Signing](concepts.md#signatures) by [example](../examples/openssl/sign)

1. [Certificates](concepts.md#certificates) by [example](../examples/openssl/cert),
   based e.g. on https://www.baeldung.com/openssl-self-signed-cert.

<!-- TODO Inline content from scripts above and run it and update MD with output automatically -->
