## zsh-bin-for-netcup-webhosting
dd & stty addon scripts for installing [zsh-bin](https://github.com/romkatv/zsh-bin) in netcup.net's webhosting

### Requirements
- [busybox](https://busybox.net/downloads/binaries)
- dd	script executable (busybox dd   "${@}")
- stty	script executable (busybox stty "${@}")

### Installation
1. download busybox binary (link above)
2. ```mkdir -pv /.local/bin```
3. ```cp -pv busybox dd stty /.local/bin```
4. ```chmod +x /.local/bin/busybox /.local/bin/dd /.local/bin/stty```
5. ```echo $PATH | grep -q '/.local/bin' || { echo 'export PATH="/.local/bin:$PATH"' >> /.profile && source /.profile; }```
6. go ahead with installation of zsh-bin:  
   ```curl https://raw.githubusercontent.com/romkatv/zsh-bin/master/install | sh -s -- -d /.local```
