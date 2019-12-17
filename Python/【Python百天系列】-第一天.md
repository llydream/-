###【Python百天系列】-第一天

#### 一：认识python

#### 二：准备环境

##### 1:安装python解释器

​    homebrew->brew install python3

##### 2:安装python开发工具

   下载pycharm，破解激活

##### 3:练习

  使用python交互环境练习`turtle`绘图

##### 4:扩展

- mac os查看系统是32位还是64位

- mac os 开启64位系统

- homebrew 更新慢，修改安装源

- mac os查看软件安装路经

- mac os未知来源软件的开启（sudo spctl --master-disable）

- 安装python解释器

  ```shell
  Last login: Mon Dec 16 20:17:16 on ttys000
  MacBook-Pro:~ lly$ brew install python3
  Updating Homebrew...
  ==> Auto-updated Homebrew!
  Updated 3 taps (homebrew/cask-versions, homebrew/services and caskroom/versions).
  
  ==> Installing dependencies for python: gdbm, openssl, readline, sqlite and xz
  ==> Installing python dependency: gdbm
  ==> Downloading https://homebrew.bintray.com/bottles/gdbm-1.18.1.mojave.bottle.1
  ######################################################################## 100.0%
  ==> Pouring gdbm-1.18.1.mojave.bottle.1.tar.gz
  🍺  /usr/local/Cellar/gdbm/1.18.1: 20 files, 586.8KB
  ==> Installing python dependency: openssl
  ==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2s.mojave.bottl
  ==> Downloading from https://akamai.bintray.com/c4/c4a762d719c2be74ac686f1aafabb
  ######################################################################## 100.0%
  ==> Pouring openssl-1.0.2s.mojave.bottle.tar.gz
  ==> Caveats
  A CA file has been bootstrapped using certificates from the SystemRoots
  keychain. To add additional certificates (e.g. the certificates added in
  the System keychain), place .pem files in
    /usr/local/etc/openssl/certs
  
  and run
    /usr/local/opt/openssl/bin/c_rehash
  
  openssl is keg-only, which means it was not symlinked into /usr/local,
  because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.
  
  If you need to have openssl first in your PATH run:
    echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile
  
  For compilers to find openssl you may need to set:
    export LDFLAGS="-L/usr/local/opt/openssl/lib"
    export CPPFLAGS="-I/usr/local/opt/openssl/include"
  
  ==> Summary
  🍺  /usr/local/Cellar/openssl/1.0.2s: 1,795 files, 12.0MB
  ==> Installing python dependency: readline
  ==> Downloading https://homebrew.bintray.com/bottles/readline-8.0.0_1.mojave.bot
  ==> Downloading from https://akamai.bintray.com/fa/faab004773e6449dd97971311cb62
  ######################################################################## 100.0%
  ==> Pouring readline-8.0.0_1.mojave.bottle.tar.gz
  ==> Caveats
  readline is keg-only, which means it was not symlinked into /usr/local,
  because macOS provides the BSD libedit library, which shadows libreadline.
  In order to prevent conflicts when programs look for libreadline we are
  defaulting this GNU Readline installation to keg-only.
  
  For compilers to find readline you may need to set:
    export LDFLAGS="-L/usr/local/opt/readline/lib"
    export CPPFLAGS="-I/usr/local/opt/readline/include"
  
  ==> Summary
  🍺  /usr/local/Cellar/readline/8.0.0_1: 48 files, 1.5MB
  ==> Installing python dependency: sqlite
  ==> Downloading https://homebrew.bintray.com/bottles/sqlite-3.28.0.mojave.bottle
  ==> Downloading from https://akamai.bintray.com/e3/e360850758d2104b4ae9eab8ae579
  ######################################################################## 100.0%
  ==> Pouring sqlite-3.28.0.mojave.bottle.tar.gz
  ==> Caveats
  sqlite is keg-only, which means it was not symlinked into /usr/local,
  because macOS provides an older sqlite3.
  
  If you need to have sqlite first in your PATH run:
    echo 'export PATH="/usr/local/opt/sqlite/bin:$PATH"' >> ~/.bash_profile
  
  For compilers to find sqlite you may need to set:
    export LDFLAGS="-L/usr/local/opt/sqlite/lib"
    export CPPFLAGS="-I/usr/local/opt/sqlite/include"
  
  ==> Summary
  🍺  /usr/local/Cellar/sqlite/3.28.0: 11 files, 3.7MB
  ==> Installing python dependency: xz
  ==> Downloading https://homebrew.bintray.com/bottles/xz-5.2.4.mojave.bottle.tar.
  ==> Downloading from https://akamai.bintray.com/01/010667293df282c8bceede3bcd369
  ######################################################################## 100.0%
  ==> Pouring xz-5.2.4.mojave.bottle.tar.gz
  🍺  /usr/local/Cellar/xz/5.2.4: 92 files, 1MB
  ==> Installing python
  ==> Downloading https://homebrew.bintray.com/bottles/python-3.7.3.mojave.bottle.
  ==> Downloading from https://akamai.bintray.com/cd/cd6b258f036893a4126975f4f5862
  ######################################################################## 100.0%
  ==> Pouring python-3.7.3.mojave.bottle.1.tar.gz
  ==> /usr/local/Cellar/python/3.7.3/bin/python3 -s setup.py --no-user-cfg install
  ==> /usr/local/Cellar/python/3.7.3/bin/python3 -s setup.py --no-user-cfg install
  ==> /usr/local/Cellar/python/3.7.3/bin/python3 -s setup.py --no-user-cfg install
  ==> Caveats
  Python has been installed as
    /usr/local/bin/python3
  
  Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
  `python3`, `python3-config`, `pip3` etc., respectively, have been installed into
    /usr/local/opt/python/libexec/bin
  
  If you need Homebrew's Python 2.7 run
    brew install python@2
  
  You can install Python packages with
    pip3 install <package>
  They will install into the site-package directory
    /usr/local/lib/python3.7/site-packages
  
  See: https://docs.brew.sh/Homebrew-and-Python
  ==> Summary
  🍺  /usr/local/Cellar/python/3.7.3: 3,862 files, 59.9MB
  ==> `brew cleanup` has not been run in 30 days, running now...
  Removing: /Users/queenme/Library/Caches/Homebrew/icu4c--64.2.mojave.bottle.tar.gz... (26.1MB)
  Removing: /Users/queenme/Library/Caches/Homebrew/node--12.4.0.mojave.bottle.1.tar.gz... (14.5MB)
  Removing: /Users/queenme/Library/Caches/Homebrew/p7zip--16.02_1.mojave.bottle.tar.gz... (2.0MB)
  Removing: /Users/queenme/Library/Caches/Homebrew/unrar--5.7.5.mojave.bottle.tar.gz... (243.2KB)
  Removing: /Users/queenme/Library/Caches/Homebrew/tomcat@7--7.0.94.tar.gz... (8.8MB)
  Removing: /Users/queenme/Library/Logs/Homebrew/p7zip... (64B)
  Removing: /Users/queenme/Library/Logs/Homebrew/tomcat@7... (104B)
  Removing: /Users/queenme/Library/Logs/Homebrew/icu4c... (64B)
  Removing: /Users/queenme/Library/Logs/Homebrew/unrar... (64B)
  Removing: /Users/queenme/Library/Logs/Homebrew/node... (64B)
  Pruned 0 symbolic links and 2 directories from /usr/local
  ==> Caveats
  ==> openssl
  A CA file has been bootstrapped using certificates from the SystemRoots
  keychain. To add additional certificates (e.g. the certificates added in
  the System keychain), place .pem files in
    /usr/local/etc/openssl/certs
  
  and run
    /usr/local/opt/openssl/bin/c_rehash
  
  openssl is keg-only, which means it was not symlinked into /usr/local,
  because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.
  
  If you need to have openssl first in your PATH run:
    echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile
  
  For compilers to find openssl you may need to set:
    export LDFLAGS="-L/usr/local/opt/openssl/lib"
    export CPPFLAGS="-I/usr/local/opt/openssl/include"
  
  ==> readline
  readline is keg-only, which means it was not symlinked into /usr/local,
  because macOS provides the BSD libedit library, which shadows libreadline.
  In order to prevent conflicts when programs look for libreadline we are
  defaulting this GNU Readline installation to keg-only.
  
  For compilers to find readline you may need to set:
    export LDFLAGS="-L/usr/local/opt/readline/lib"
    export CPPFLAGS="-I/usr/local/opt/readline/include"
  
  ==> sqlite
  sqlite is keg-only, which means it was not symlinked into /usr/local,
  because macOS provides an older sqlite3.
  
  If you need to have sqlite first in your PATH run:
    echo 'export PATH="/usr/local/opt/sqlite/bin:$PATH"' >> ~/.bash_profile
  
  For compilers to find sqlite you may need to set:
    export LDFLAGS="-L/usr/local/opt/sqlite/lib"
    export CPPFLAGS="-I/usr/local/opt/sqlite/include"
  
  ==> python
  Python has been installed as
    /usr/local/bin/python3
  
  Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
  `python3`, `python3-config`, `pip3` etc., respectively, have been installed into
    /usr/local/opt/python/libexec/bin
  
  If you need Homebrew's Python 2.7 run
    brew install python@2
  
  You can install Python packages with
    pip3 install <package>
  They will install into the site-package directory
    /usr/local/lib/python3.7/site-packages
  
  See: https://docs.brew.sh/Homebrew-and-Python
  
  ```

  



