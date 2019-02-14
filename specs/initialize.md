# Initialize (in 3bot itself)


## As a user initialize through PC

### Assumptions
* A user can type a place and the city/country will be extracted from it. This will be in an auto filling field (first version is ok with Google Maps API)
* Threefold double name or email address as reference (use regex to check usecase, descriptive for user)
* Private key is created by backend
* Mnemonic words / private key are shared with TFT wallet
* Flow finishes after QR scanning
* A code should be provisioned to the 3bot so the user can surf to it the first time (can be provided in url)

### API
[TODO]

GET /tfgrid/3bot/{doublename}

### Flow
* Send data to backend
* Register TOTP through API (https://localhost:80443/api/totp)

### Relevant links
- [rivine mnemonic documentation](https://github.com/threefoldtech/rivine/blob/master/doc/wallet.md#private-key-generation) 

### Mockups

![Initialize mockups](./images/initialize.svg)

(Last screen should show QR code :-) )


## As a user initialize through mobile

### Assumptions
* Assumptions for PC registration are also valid here
* Flow is only valid using the app, when visiting without the app the user will then be redirected to Play Store

## Flow
* Last QR code is not shown, instead POST https://localhost:80443/api/totp  is called
