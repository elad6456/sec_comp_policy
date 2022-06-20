# seccomp policy for nginx docker image

## Image:
nginx        latest    0e901e68141f

## How To run:
'$ docker run -d -p 8080:80 --security-opt seccomp=./hardenedcalls.json nginx'

## Stress tests were made for running the docker with the hardened policy:

`$ ab -n 100000 -c 10 -k -H "Accept-Encoding: gzip, deflate" localhost:8080/`

## Default policy that was used:

https://raw.githubusercontent.com/docker/labs/master/security/seccomp/seccomp-profiles/default.json
