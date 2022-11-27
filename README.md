# nginx

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/nginx/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/nginx/actions/workflows/release.yaml)

A minimal nginx base image rebuilt every night from source.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/nginx:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `stable-20221123` | `sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4) | `amd64` `arm64` `armv7` |
| `stable-20221124` | `sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26) | `amd64` `arm64` `armv7` |
| `stable-20221125` | `sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c) | `amd64` `arm64` `armv7` |
| `stable-20221126` | `sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab) | `amd64` `arm64` `armv7` |
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:5a1572d4d06dbe36492415e2c5dcf82d2f6ba01cb1d936dece1720aacc55495c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5a1572d4d06dbe36492415e2c5dcf82d2f6ba01cb1d936dece1720aacc55495c) | `amd64` `arm64` `armv7` |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221127` | `sha256:5fd5b39b1751bf3a3d389f97dd51805ae7a939c9155a3543d2e9ab4ff5f66f38`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5fd5b39b1751bf3a3d389f97dd51805ae7a939c9155a3543d2e9ab4ff5f66f38) | `amd64` `arm64` `armv7` |
| `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |
| `stable-20221122` | `sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50) | `amd64` `arm64` `armv7` |


## Usage

To try out the image, run:

```
docker run -p 8080:80 cgr.dev/chainguard/nginx
```

If you navigate to `localhost:8080`, you should see the nginx welcome page.

To run an example Hello World app, navigate to the root of this repo and run:

```
docker run -v $(pwd)/examples/hello-world/site-content:/var/lib/nginx/html -p 8080:80 cgr.dev/chainguard/nginx
```

If you navigate to `localhost:8080`, you should see `Hello World from Nginx!`.



## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/nginx:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/nginx:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/nginx"
      },
      "image": {
        "docker-manifest-digest": "sha256:5a1572d4d06dbe36492415e2c5dcf82d2f6ba01cb1d936dece1720aacc55495c"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "fc849d53bf4377a6d7ccaec51ed7c1d33eb794b0",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQCvtVRY/f6/Q+ZVUE6jMHrUkdHt3JossEZ7rrdPLLOl5wIgaqYKUt/xb9LRkr+YBFlMBZFN68V2dfRQtZlFZTr4p4g=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI3OWYwMDc2MDI2ODA0ZmVhNjQ4NmVmYzVjZmM0MmE2NmFjY2I2OGIzOTVmZmQ1N2NlNzgwY2JmMmExZTlhMTc0In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJRDNYV1R0VWZLRitGanBMVlZpQTVQVC9UVVZDRG00U1BCa0JpRUoxVGQ3S0FpRUE5OThuZTZ3QlpPekpIeUJuQkVmNXpWRDVkOG1nSDVGL3hXSzNPMmFYcTJNPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhWRU5EUVhrclowRjNTVUpCWjBsVlFWVmhRaTh4Y25GVFIwRlRUamhVUVVwR1owa3pNQzlYVTAxUmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1ROTlJFRjVUbXBOZUZkb1kwNU5ha2w0VFZSSk0wMUVRWHBPYWsxNFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVYxVFhkaWFVZFBUREJwYjB0NGJIQnBhbU55UmpsMWRuUllTV05OVGs1SFVXZzVXVlVLVG5scVVXSmFVVTVwZVRjNFJrUjVhWGRvZVVGbU5HVnpjV0ZYWkU5M2FrZGpUazFyVjIxRlN6SnNkVFZ3YVRkRVZVdFBRMEZyTkhkblowcExUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZMY2poQkNsbHdjR2xhZEZaRE5UUmhPV0pGT0V4dU1IWlFlVWhOZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVmRDWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZvZWxreWFHeGFTRlp6V2xSQk1ncENaMjl5UW1kRlJVRlpUeTlOUVVWRVFrTm9iVmw2WnpCUFYxRXhUVEpLYlU1RVRUTk9Na1V5V2tSa2Fsa3lSbXhaZWxWNFdsZFJNMWw2Um10TmVrNXNDbGxxWXpWT1IwbDNUVUozUjBOcGMwZEJVVkZDWnpjNGQwRlJVVVZFYTA1NVdsZEdNRnBUUWxOYVYzaHNXVmhPYkUxRFZVZERhWE5IUVZGUlFtYzNPSGNLUVZGVlJVWXlUbTlaVjJ4MVdqTldhR050VVhSaFZ6Rm9XakpXZWt3eU5XNWhWelUwVFVJd1IwTnBjMGRCVVZGQ1p6YzRkMEZSV1VWRU0wcHNXbTVOZGdwaFIxWm9Xa2hOZG1KWFJuQmlha05DYVdkWlMwdDNXVUpDUVVoWFpWRkpSVUZuVWpoQ1NHOUJaVUZDTWtGT01EbE5SM0pIZUhoRmVWbDRhMlZJU214dUNrNTNTMmxUYkRZME0ycDVkQzgwWlV0amIwRjJTMlUyVDBGQlFVSm9URm8yWms1QlFVRkJVVVJCUldOM1VsRkphRUZKYjNCTFdXeEhWMjVLVlRJdk4xb0tWVVV6WlZnek1HRkViVnBuWTFKMk1USmhaSFJNUVhoeU5URXJZMEZwUWt4dlpXTkVNVWxTWWpsa1dHOHlUbXRTWTBsbVRtNVRVbUl2YVhkRVNGZHBRd3BoYTBOYVoydDRkVmRxUVV0Q1oyZHhhR3RxVDFCUlVVUkJkMDV2UVVSQ2JFRnFSVUZ3VG5WTlZWQjBTRGtyZVROMVUzSTFOVkpLYzFsT1VsWnVNQ3Q2Q21WTlMya3ZPRFJCV1VOU1JEZHdkbWxDUTB0RlZXVnBVVTA1ZUROa2Npc3dhMmt5VVVGcVFtVjBRVUp6VUVaQmFrcHFkbkZCUjJwWFRtSk9SakJvTmpVS2NHRjZlRUpuZUd0WFNYaERNRUV6U0RjNFNuZDZSbTR3Vm1GVE4xRkxkbVUxVGk5b09HZ3dQUW90TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1669508799,
          "logIndex": 7918106,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "fc849d53bf4377a6d7ccaec51ed7c1d33eb794b0",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3555934820",
      "sha": "fc849d53bf4377a6d7ccaec51ed7c1d33eb794b0"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

