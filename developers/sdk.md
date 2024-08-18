# SDK

[https://github.com/unibaseio/unibase-sdk-go](https://github.com/unibaseio/unibase-sdk-go/releases)

### Upload File / Directory / Model

```
> git clone https://github.com/MOSSV2/dimo-sdk-go.git
> cd example/upload
> go build
# if sk not set, will generate a new key, model means upload model or regualr file/dir
> ./upload --model=false --sk=<your secret key> --path=<your local file/dir path>
# example, upload file
> ./upload --sk=4215875d8ac13ac4fb0876a0ecd0384aca0ce16b627bf975c8084915aad79470 --path=./upload
```

### Download File / Directory / Model

```
> cd example/download
> go build
# if sk not set, will generate a new key, model means upload model or regualr file/dir
> ./download --model=false --sk=<your secret key>  --name=<file name> --path=<your local file/dir path to save>
# example, upload file
> ./download --sk=4215875d8ac13ac4fb0876a0ecd0384aca0ce16b627bf975c8084915aad79470 --name=4b59a3a5fa50d178dc4594c400097d497a206cff98865e815333ed7504558336 --path=./upload
```

### Example: Upload huggingface repo

```
> cd example/hub
> go build
# huggingface public repo name, such as: CompVis/stable-diffusion-v1-1, empty revision means latest
# hub node will sync data from hugginface and upload to dimo
> ./hub --name=<repo name> --revision=<repo revision>
# example, sync repo
> ./hub --name=CompVis/stable-diffusion-v1-1
```



