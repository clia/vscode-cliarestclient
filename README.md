# Clia REST Client

Clia REST Client is a personal temporary VSCode plugin, forked from [REST Client](https://github.com/Huachao/vscode-restclient).

## Added Features

### URL Signature

URL Signature method like AliYun's: [https://help.aliyun.com/document_detail/30563.htm](https://help.aliyun.com/document_detail/30563.htm).
The signature algorithm is configurable. Configuration contains two parts:

- `Url Sign Configuration`: Configuration for the signature algorithm and names.
- `Url Sign Key Secrets`: Key and secret pairs for use.

You should enable it in the configuration if you want to use this function, the default is disabled.

The default configuration is our use case.

An example AliYun's signature algorithm configuration:

```json
{
    "enableUrlSign": true,
    "algorithm": {
        "step1OrderParams": true,
        "step1UrlEncodeParams": true,
        "step1PercentEncode": true,
        "step1AddEqual": true,
        "step1AddAnd": true,
        "step2SeparatorAnd": true,
        "step2AddHttpMethod": true,
        "step2AddPercentEncodeSlash": true,
        "step2PercentEncode": true,
        "step3ComputeAlgorithm": "hmacsha1",
        "step3SecretAppend": "&",
        "step3TextAlgorithm": "base64"
    },
    "keyParamName": "AccessKeyId",
    "signParamName": "Signature"
}
```
