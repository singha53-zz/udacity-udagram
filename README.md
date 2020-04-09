# Submission for Cloud DevOps Nanodegree: Project 2 - a highly available web app using CloudFormation

## Infrastructure diagram

<p align="center">
	<img src="https://github.com/singha53/udacity-udagram/blob/master/Udacity%20Project%202.png" width={400} alt="app" />
</p>

## Steps to reproduce
- assuming aws-cli is install and aws account is configured

### 1) create infrastucture

```shell
sh create.sh STACK_NAME_NETWORK udagram_network_template.yml udagram_network_params.json AWS_REGION AWS_PROFILE
```

### 2) create servers and upload webapp from S3

```shell
sh create.sh STACK_NAME_SERVERS udagram_servers_template.yml udagram_servers_params.json AWS_REGION AWS_PROFILE
```

- output is a link to the webapp

## Clean-up

```shell
sh delete.sh STACK_NAME_SERVERS
sh delete.sh STACK_NAME_NETWORK
```
