# Blinkt Setup

```bash
# Git
$ sudo -E apt-get update && \
  sudo -E apt-get install -qy git
```

```bash
# Clone the blinkt library
$ git clone http://github.com/pimoroni/blinkt
```
```bash
# Build the blinkt docker image
$ cd blinkt
$ docker build -t blinkt .
```

```bash
# Run the Knight Rider example
$ docker run --privileged -ti blinkt
```