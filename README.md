[![TM Logo](tm_logo.png)](https://www.timemachine.eu)

# Requests for Comments

This repository is the main location for work on and release of finalised Time Machine *Request for Comments*.

## Files

### Drafts in preparation

| ID       | Title                              |
| -------- | ---------------------------------- |
| RFC-0001 | Time Machine Glossary              |
| RFC-0002 | RFC on RFC Tree                    |
| RFC-0003 | RFC on RFC Platform                |
| RFC-0004 | RFC on the RFC Editorial Committee |
| RFC-0005 | RFC on LTM                         |

### Current open drafts

| ID       | Contribution deadline | Public Discussion URL                                                                     |
| -------- | --------------------- | ----------------------------------------------------------------------------------------- |
| RFC-0000 | 2020-07-21            | [Pull Request #20](https://github.com/time-machine-project/requests-for-comments/pull/20) |

### Current open candidates

| ID  | Review deadline | Peer Review URL |
| --- | --------------- | --------------- |

### Published releases

| ID  | File | Release | Release date |
| --- | ---- | ------- | ------------ |

## Building PDF files locally

It is possible to build PDF files locally using [Docker](https://www.docker.com/) with the following commands. These will build a Docker image that will then be used to build the PDF files (the drafts in this specific command) and store them in the provided output location: the `temp` folder in the root directory of the local repository.

### Linux

```shell
cd [path/to/the/repository/folder]
docker build -t time-machine-project/publish_pdfs build
docker run -v $PWD\files\drafts:/opt/input -v $PWD\temp:/opt/output time-machine-project/publish_pdfs
```

### Windows

```shell
cd [path/to/the/repository/folder]
docker build -t time-machine-project/publish_pdfs build
docker run -v %cd%\files\drafts:/opt/input -v %cd%\temp:/opt/output time-machine-project/publish_pdfs
```


