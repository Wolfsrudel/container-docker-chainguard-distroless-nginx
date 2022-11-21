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
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:defe9227d47b5152038979dbe9b55f11a75de3cc2e8ab38d65f131171cf83cfc`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:defe9227d47b5152038979dbe9b55f11a75de3cc2e8ab38d65f131171cf83cfc) | `amd64` `arm64` `armv7` |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |


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
        "docker-manifest-digest": "sha256:defe9227d47b5152038979dbe9b55f11a75de3cc2e8ab38d65f131171cf83cfc"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "push",
      "1.3.6.1.4.1.57264.1.3": "c1aa584ce46dd205e3e4f9725f2f0c256007d970",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQDG+M/+vZHX0uf8eymWzgXIuWtBK302L1IJPQKWjqiZSQIgOIUd98fwBD0jk5iK8t9/JiPHKeyq7hGPojzyJx8LWKI=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIzOTE3YjlhNTI0ZmM3MTIzYjI1MWUwOGVhNWRkMzEyNzEyODM5MTFmOWFmODVkMzY4ZDNiYWYyMTIwMWJiMGZmIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJRHdJdXZTblBwWFFFR3NUUHQxSjNFbHl5cVFGeDg4QWFadENlQ2gxM1lPVUFpRUExNGVXUENaaFhTeWlPK0xkV281YTJvQmtvamRTd0ZnRkpMQ2h4V3hYUG84PSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUndWRU5EUVhseFowRjNTVUpCWjBsVlQyTlNMMHRuVUVGT1dEWktkRE5DTjJaWE1HcHNOa0p4YTJaWmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hoTlZHY3dUV3BCZVZkb1kwNU5ha2w0VFZSSmVFMVVaekZOYWtGNVYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVV2V2xjM1JYVnphRlJtUzNGNk1sVTFTV3hDTmxvMVNVRjZTR2h2ZGtjcmNrMDFZMlFLV0ZaeVRtSjNVbEJYWlVkck5ESjRVRGhsYlRSa1RqYzJSR2xRUmt0aWRITmpLMHBzVDJwMFdUUkJiVWR2WVV4d0x6WlBRMEZyYTNkblowcEdUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZzWlhSR0NrTkxMMEpsT1ZGTVpURlRaMWQxT0hGU1IwWk9ZMlkwZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVk5DWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZTZDJSWVRtOU5SRmxIUTJselJ3cEJVVkZDWnpjNGQwRlJUVVZMUjAxNFdWZEZNVTlFVW1wYVZGRXlXa2RSZVUxRVZteE5NbFV3V21wck0wMXFWbTFOYlZsM1dYcEpNVTVxUVhkT01sRTFDazU2UVhkSVFWbExTM2RaUWtKQlIwUjJla0ZDUWtGUlQxRXpTbXhaV0ZKc1NVWktiR0pIVm1oak1sVjNTbEZaUzB0M1dVSkNRVWRFZG5wQlFrSlJVVmdLV1RKb2FHRlhOVzVrVjBaNVdrTXhjR0pYUm01YVdFMTJZbTFrY0dKdVozZElVVmxMUzNkWlFrSkJSMFIyZWtGQ1FtZFJVR050Vm0xamVUbHZXbGRHYXdwamVUbDBXVmRzZFUxSlIwcENaMjl5UW1kRlJVRmtXalZCWjFGRFFraHpSV1ZSUWpOQlNGVkJNMVF3ZDJGellraEZWRXBxUjFJMFkyMVhZek5CY1VwTENsaHlhbVZRU3pNdmFEUndlV2RET0hBM2J6UkJRVUZIUlcwek9WRktVVUZCUWtGTlFWSnFRa1ZCYVVKd2FsWlBjRXRLZG5aeVpYcGpjR2xwYWpOek9Fb0tjRE00ZURsc1FWWktkRU5vZFUwd01uQk1NbXhLZDBsblNub3hkR2R3UkRoamNGTmxZWEI1WkU1clVrcHZhME5STTJsa1VpOHJWR2R6Wm1SWFVGWk5id28zUXpSM1EyZFpTVXR2V2tsNmFqQkZRWGROUkdGUlFYZGFaMGw0UVV3ME1YUkxPRkp5Vm5GUmQwVlVVR1IzVDBGaFQwdHZaemhQYUdSYWFXVnZSalUyQ2pSRlFWRkpkMGhPTURablJtWkVabWhXWTJkeldFdEtUbFFyU3l0NlFVbDRRVW94Y0dKcE1EZDZiVlZEWlZwc055OU5hbFJwVURKQk5UZHJWekk1WVRNS1NFTXJOVlpWYm01SGRFUmhiREZ4VkhVelVHODBTbTVWTTFWQ1FYZDNNREpJWnowOUNpMHRMUzB0UlU1RUlFTkZVbFJKUmtsRFFWUkZMUzB0TFMwSyJ9fX19",
          "integratedTime": 1669056131,
          "logIndex": 7559214,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "c1aa584ce46dd205e3e4f9725f2f0c256007d970",
      "githubWorkflowTrigger": "push",
      "run_attempt": "1",
      "run_id": "3517088826",
      "sha": "c1aa584ce46dd205e3e4f9725f2f0c256007d970"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

