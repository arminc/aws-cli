#AWS cli

For more information about the AWS cli see https://aws.amazon.com/cli/

##Building
`docker build -t aws-cli .`

##Running
```bash
aws() {
	docker run --rm -it \
		-m 1024m \
		-v ${HOME}:${HOME}:rw \
		-w ${PWD} \
		--env AWS_ACCESS_KEY_ID=${AWS_ACCESS_KEY_ID} \
		--env AWS_SECRET_ACCESS_KEY=${AWS_SECRET_ACCESS_KEY} \
		--env AWS_DEFAULT_REGION=${AWS_DEFAULT_REGION} \
		aws-cli "$@"
}
```
