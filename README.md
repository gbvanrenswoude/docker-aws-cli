# AWS CLI in Docker

Containerized AWS CLI on alpine to avoid requiring the aws cli to be installed on CI machines.

Forked off [mesosphere/aws-cli](https://github.com/mesosphere/aws-cli).
Original work Copyright 2016-2017 Mesosphere, Inc.
Updated by yours truly.

## Get it here
[Dockerhub registry](https://hub.docker.com/r/gbvanrenswoude/aws-cli/)

## Build

```
docker build -t gbvanrenswoude/aws-cli .
```

## Usage

If no instance role is available, configure:

```
export AWS_ACCESS_KEY_ID="<id>"
export AWS_SECRET_ACCESS_KEY="<key>"
export AWS_DEFAULT_REGION="<region>"
```

```
docker run --rm -v /tmp:/tmp gbvanrenswoude/aws-cli s3 cp /tmp/something.txt s3://somebucket/something.txt
```

## References

AWS CLI Docs: https://aws.amazon.com/documentation/cli/
