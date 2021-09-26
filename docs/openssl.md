# OpenSSL

<!-- Put this into a script and run it and update MD with putput automatically -->

Inspired e.g. by https://www.keycdn.com/blog/openssl-tutorial:

    openssl version -a
    # 1.1.1

    openssl list -help
    openssl list -commands
    openssl list -digest-commands
    openssl list -cipher-commands
    openssl list -public-key-methods

    echo "hello, world" | openssl enc -aes-256-cbc -pbkdf2 -pass pass:demo
    echo "hello, world" | openssl enc -aes-256-cbc -pbkdf2 -pass pass:demo | openssl enc -aes-256-cbc -pbkdf2 -pass pass:demo -d

    openssl genrsa -out /tmp/private.pem 4096
    openssl rsa -in /tmp/private.pem -text -noout
    
