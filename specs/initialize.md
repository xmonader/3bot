# Initialize (in 3bot itself)


## As a user initialize through PC

### Assumptions
* A user can type a city and a suggested location can be chosen. This will be in an auto filling field (first version is ok with Google Maps API)
* ThreeFold double name or email address as reference (use regex to check usecase, descriptive for user)
* Private key is created by backend
* Mnemonic words / private key are shared with TFT wallet
* Flow finishes after QR scanning
* A code should be provisioned to the 3bot so the user can surf to it the first time (can be provided in url)
* A first wallet is created when the user creates its 3bot private key, using the same key (this is the default wallet)

### API
[TODO]

GET /tfgrid/3bot/{doublename}

### Flow
* Send data to backend
* Register TOTP through API (https://localhost:80443/api/totp)

### Technical
- [rivine mnemonic documentation](https://github.com/threefoldtech/rivine/blob/master/doc/wallet.md#private-key-generation) 
- Generating and decoding a mnemonic is present in Jumpscale

### Mockups

![Initialize mockups](./images/initialize.svg?sanitize=true)

(Last screen should show QR code :-) )


## As a user initialize through mobile

### Assumptions
* Assumptions for PC registration are also valid here
* Flow is only valid using the app, when visiting without the app the user will then be redirected to Play Store

## Flow
* Last QR code is not shown, instead POST https://localhost:80443/api/totp  is called
