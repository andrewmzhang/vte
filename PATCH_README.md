# VTE w/ OSC 52 support

See full explanation at: [link](https://andrewmzhang.com/blog/2020/osc-52-patch-for-vte-0425/)

## Ubuntu Dependencies Install

```
apt-get install gtk-doc-tools gobject-introspection valac libvala-dev libgnutls-dev libgirepository1.0-dev gperf
```

## Install from source

```
# Will install to /opt/vte
./autogen.sh --prefix=/opt/vte
make
sudo make install
```


## Modifying gnome-terminal-server


```
sudo patchelf --replace-needed libvte-2.91.so.0 /opt/vte/lib/libvte-2.91.so.0 /usr/lib/gnome-terminal/gnome-terminal-server

```



