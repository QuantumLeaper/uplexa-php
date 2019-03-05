# uPlexa Library
A uPlexa library written in PHP for private payment processing.

## How It Works
This library has 3 main parts:

1. A uPlexa daemon JSON RPC API wrapper, `daemonRPC.php`
2. A uPlexa wallet (`uplexa-wallet-rpc`) JSON RPC API wrapper, `walletRPC.php`
3. A uPlexa/Cryptonote toolbox, `cryptonote.php`, with both lower level functions used in uPlexa related cryptography and higher level methods for things like generating uPlexa private/public keys.

In addition to these features, there are other lower-level libraries included for portability, *eg.* an ed25519 library, a SHA3 library, *etc.*

## Documentation

Documentation can be found in the [`/docs`](https://github.com/uplexa/uplexa-php/tree/master/docs) folder.

## Configuration
### Requirements
 - uPlexa daemon (`uplexad`)
 - Webserver with PHP, for example XMPP, Apache, or NGINX
    - cURL PHP extension for JSON RPC API(s)
    - GMP PHP extension for about 100x faster calculations (as opposed to BCMath)

Debian (or Ubuntu) are recommended.

### Getting Started

1. Start the uPlexa daemon (`uplexad`) on testnet.
```bash
uplexad --testnet --detach
```

2. Start the uPlexa wallet RPC interface (`uplexa-wallet-rpc`) on testnet.
```bash
uplexa-wallet-rpc --rpc-bind-port 21065 --disable-rpc-login --wallet-dir /path/to/wallet/directory
```

3. Edit `example.php` with your the IP address of `uplexad` and `uplexa-wallet-rpc`

4. Serve `example.php` with your webserver (*eg.* XMPP, Apache/Apache2, NGINX, *etc.*) and navigate to it.  If everything has been set up correctly, information from your uPlexa daemon and wallet will be displayed.
