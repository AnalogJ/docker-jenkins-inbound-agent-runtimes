# docker-jenkins-inbound-agent-runtimes
Language specific Jenkins inbound agent containers. See https://github.com/jenkinsci/docker-inbound-agent/



# Tagging

We use a standardized tagging convention to ensure that version tracking is easy:

`{JENKINS_AGENT_VERSION}-[JAVA_VARIANT or blank if java8]-{LANGUAGE}[LANGUAGE_VERSION or blank when latest]`

eg. `docker pull analogj/jenkins-inbound-agent-runtime:latest-java11-go1.13`

Here's a partial list of Docker image tags that are available for `jenkins-inbound-agent-runtime`. You can find the full list of base images for each
supported language and operating system by looking at the `hooks/versions.txt` file in each subdirectory.


## Golang

| | Golang latest | Golang 1.13 |
| --- | --- | --- |
| latest | latest-go | latest-go1.13 |
| latest-java11 | latest-java11-go | latest-java11-go1.13 |
| 4.3 | 4.3-go | 4.3-go1.13  |
| 4.3-java11 | 4.3-java11-go | 4.3-java11-go1.13 |

## Java

| | Java 8 | Java 11 |
| --- | --- | --- |
| latest | latest-java8 | latest-java11 |
| 4.3 | 4.3-java8 | 4.3-java11 |

## Node

| | Node latest | Node 12 |
| --- | --- | --- |
| latest | latest-node | latest-node12 |
| latest-java11 | latest-java11-node | latest-java11-node12 |
| 4.3 | 4.3-node | 4.3-node12  |
| 4.3-java11 | 4.3-java11-node | 4.3-java11-node12 |

## Python

| | Python latest | Python 3 | Python 2.7 |
| --- | --- | --- | --- |
| latest | latest-python | latest-python3 | latest-python2 |
| latest-java11 | latest-java11-python | latest-java11-python3 | latest-java11-python2 |
| 4.3 | 4.3-python | 4.3-python3  | 4.3-python2 |
| 4.3-java11 | 4.3-java11-python | 4.3-java11-python3 | 4.3-java11-python2 |

## Ruby

| | Ruby latest | Ruby 2.7 |
| --- | --- | --- |
| latest | latest-ruby | latest-ruby2.7 |
| latest-java11 | latest-java11-ruby | latest-java11-ruby2.7 |
| 4.3 | 4.3-ruby | 4.3-ruby2.7 |
| 4.3-java11 | 4.3-java11-ruby | 4.3-java11-ruby2.7 |
