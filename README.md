# srv

[![Build Status](https://travis-ci.org/davegallant/srv.svg?branch=master)](https://travis-ci.org/davegallant/srv)
[![Go Report Card](https://goreportcard.com/badge/github.com/davegallant/srv)](https://goreportcard.com/report/github.com/davegallant/srv)

View RSS feeds from the terminal.

![image](https://user-images.githubusercontent.com/4519234/86504202-b861bd00-bd83-11ea-8a8e-4f28e38a71ce.png)


## install

### via releases

```shell
VERSION='0.1.0'; \
sudo curl --progress-bar \
-L "https://github.com/davegallant/srv/releases/download/v${VERSION}/srv_${VERSION}_$(uname -s)_x86_64.tar.gz" | \
sudo tar -C /usr/bin --overwrite -xvzf - srv
```

### via go

```shell
go get github.com/davegallant/srv
```

## configure

srv reads configuration from `~/.config/srv/config.yaml`

If a configuration is not provided, a default configuration is generated.

- `feeds` is a list of RSS/Atom feeds to be loaded in srv.
- `externalViewer` defines an application to override the default web browser (optional).

An example config can be copied:

```shell
cp ./config-example.yaml ~/.config/srv/config.yaml
```

## navigate

Key mappings are statically defined for the time being.

- `TAB` switches between Feeds and Items.
- `UP/DOWN` navigates feeds and items`
- `ENTER` either selects a feed or opens a feed item in an external application.
- `F5` refresh list of feeds

## build

```shell
make build
```

## test

```shell
make test
```
