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
| `stable-20221127` | `sha256:5fd5b39b1751bf3a3d389f97dd51805ae7a939c9155a3543d2e9ab4ff5f66f38`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5fd5b39b1751bf3a3d389f97dd51805ae7a939c9155a3543d2e9ab4ff5f66f38) | `amd64` `arm64` `armv7` |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221128` | `sha256:b33ef90c2716a2ec2ec4d703d8fbccd90719cfb0dad0a0b31b22a577bc4f2699`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b33ef90c2716a2ec2ec4d703d8fbccd90719cfb0dad0a0b31b22a577bc4f2699) | `amd64` `arm64` `armv7` |
| `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |
| `stable-20221122` | `sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50) | `amd64` `arm64` `armv7` |
| `stable-20221125` | `sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c) | `amd64` `arm64` `armv7` |
| `stable-20221126` | `sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab) | `amd64` `arm64` `armv7` |
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:e20ac1fb3515aa2bd167c9552938eb11325bdd01cc87ebe8ede200e09654842a`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e20ac1fb3515aa2bd167c9552938eb11325bdd01cc87ebe8ede200e09654842a) | `amd64` `arm64` `armv7` |
| `stable-20221123` | `sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4) | `amd64` `arm64` `armv7` |
| `stable-20221124` | `sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26) | `amd64` `arm64` `armv7` |


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
        "docker-manifest-digest": "sha256:e20ac1fb3515aa2bd167c9552938eb11325bdd01cc87ebe8ede200e09654842a"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "7fa202ea0d3b5e4ef52eb6eb2d794480cd7928f6",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCIECURhQA+IXak+D2TLGaeeX4yv9dKWXIiw9urezBmg4JAiBbSEreq/HlmtZnQtZUexlOSGJxjJ0u9PHca8oHZfBbdA==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIxODRlOWQ2MTYzZjgzMTNmZmRlMmI3MDgyNzg0ZTMxZjgzNGY5MjBhYWUzMTZmMDRiMWY5ODcyNTlhNDU1YTlhIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUNrSFM2VDFVRFFaVUNtTWZZa3ZNVmIrejBIUW9wRzRHRmFaNy96Y2tvMzNBSWdPMVVBWjVYSFpGSnowaktVQUNGcGorV2xVcVFYUkJ6WDBwVnQ1Y2VWd2NjPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhWRU5EUVhrclowRjNTVUpCWjBsVlZIWldiR1JJYjJWU1dHbHpVVUZzVEdKbVZWSnJlbVZvVGpsQmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1RSTlJFRjVUbXBWZWxkb1kwNU5ha2w0VFZSSk5FMUVRWHBPYWxWNlYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZFV2pSUWFtbEJNM2htYzFWbUwzcEZaekZzTHpGc2RWTmlVMUVyZUVFek1GQjJOMlFLVEhoRVUwa3liWGRCY25Fd1NXSnVZVnB6V0ZCSFMxRm5helZPYWpaRWVrWkxkM0pqWm10RFFYRkdhV04xYWtGVWJVdFBRMEZyTkhkblowcExUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlY2UWxkRUNsWXZUV2N2VkU1VU1IWjROVkZVTHpWVVdqaEdZMjVWZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVmRDWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZvZWxreWFHeGFTRlp6V2xSQk1ncENaMjl5UW1kRlJVRlpUeTlOUVVWRVFrTm5NMXB0UlhsTlJFcHNXVlJDYTAweVNURmFWRkpzV21wVmVWcFhTVEphVjBsNVdrUmpOVTVFVVRSTlIwNXJDazU2YTNsUFIxa3lUVUozUjBOcGMwZEJVVkZDWnpjNGQwRlJVVVZFYTA1NVdsZEdNRnBUUWxOYVYzaHNXVmhPYkUxRFZVZERhWE5IUVZGUlFtYzNPSGNLUVZGVlJVWXlUbTlaVjJ4MVdqTldhR050VVhSaFZ6Rm9XakpXZWt3eU5XNWhWelUwVFVJd1IwTnBjMGRCVVZGQ1p6YzRkMEZSV1VWRU0wcHNXbTVOZGdwaFIxWm9Xa2hOZG1KWFJuQmlha05DYVdkWlMwdDNXVUpDUVVoWFpWRkpSVUZuVWpoQ1NHOUJaVUZDTWtGT01EbE5SM0pIZUhoRmVWbDRhMlZJU214dUNrNTNTMmxUYkRZME0ycDVkQzgwWlV0amIwRjJTMlUyVDBGQlFVSm9USFZvVERFd1FVRkJVVVJCUldOM1VsRkpaMDAxZWxFNGJUbGtkUzlUVmxSV09VWUtaM2N5VkZSWmRHaGxaVWRXVWpSS2EwZHdRMjUxY0dkeFNFRTRRMGxSUTBFeE1Hd3ZjMjUyWWtOVmRXWjNSa3cwVDA1VGNVTm9ka0oxWm1JeU9DdHllQW80VTNodGMzSXplSEZxUVV0Q1oyZHhhR3RxVDFCUlVVUkJkMDV2UVVSQ2JFRnFSVUYyWVZJNVVrdEpORE5OZURBNWFWbG9ZMGRsSzBnM2RFNXdZVVJhQ25KeWFuQmlVR0pvWkdGdmJWWXlSM1oyYkVsMFdXOW9kVVZ4UTNWSWFEVndiVGhvTTBGcVFYQnJSa2xvYlV4TE1VZE5SVVZwVDBGRVEzZDBlbkF4VkdFS1lrZGlhSHBWUkZWUVdWcHBRMmQxTmpabWJXcHpjWGhQYVVSVGVXTlJSMFJoU1daa09HbHZQUW90TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1669595223,
          "logIndex": 7978309,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "7fa202ea0d3b5e4ef52eb6eb2d794480cd7928f6",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3560595920",
      "sha": "7fa202ea0d3b5e4ef52eb6eb2d794480cd7928f6"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

