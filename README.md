[![Build Status](https://travis-ci.org/iwan/go-qr-generator.svg?branch=master)](https://travis-ci.org/iwan/go-qr-generator)

# A QR code generator written in Golang
Starts an HTTP server (listening on port 8080) that generates QR codes. Once installed and running (see below), the service accepts the following two parameters:
* ```data```: (Required) The (URL encoded) string that should be encoded in the QR code
* ```size```: (Optional) The size of the image (default: 250)

E.g. ```http://your-domain.tld:8080/?data=Hello%2C%20world&size=300```

## Installation
Download the source code and build it
```
git clone https://github.com/iwan/go-qr-generator.git

cd go-qr-generator.git

go mod init github/iwan/go-qr-generator

go get github.com/boombuler/barcode
go get github.com/boombuler/barcode/qr
go build

```

Then build the Docker image and run it
```
docker build . -t iwan/go-qr-generator-2021
docker run -p 8080:8080 iwan/go-qr-generator-2021
```

## References
* Barcode Library: https://github.com/boombuler/barcode
