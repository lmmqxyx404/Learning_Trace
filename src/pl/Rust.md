```
Welcome to Rust!

This will download and install the official compiler for the Rust
programming language, and its package manager, Cargo.

Rustup metadata and toolchains will be installed into the Rustup
home directory, located at:

   C:\Users\LMMQXYX\.rustup </u>

This can be modified with the RUSTUP_HOME environment variable.

The Cargo home directory located at:

  C:\Users\LMMQXYX\.cargo

This can be modified with the CARGO_HOME environment variable.

The cargo, rustc, rustup and other commands will be added to
Cargo's bin directory, located at:

  C:\Users\LMMQXYX\.cargo\bin

This path will then be added to your PATH environment variable by
modifying the HKEY_CURRENT_USER/Environment/PATH registry key.

You can uninstall at any time with rustup self uninstall and
these changes will be reverted.

Current installation options:


   default host triple: x86_64-pc-windows-msvc
     default toolchain: stable (default)
               profile: default
  modify PATH variable: yes

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
>
```

# if the download speed is too low, then try the following way. remember to execute the rustup-init.exe in the later command line.If your computer system is linux, then change the .sh file.
The command is only used to speed up rustup-init.exe.
``` $ENV:RUSTUP_DIST_SERVER='https://mirrors.ustc.edu.cn/rust-static' ```
``` $ENV:RUSTUP_UPDATE_ROOT='https://mirrors.ustc.edu.cn/rust-static/rustup' ```

# When you use rustlings(or try to install relative dependencies),you can change the origin to speed up.
in general, you shouhld add a config file named ```config``` (without any type name) under ```.cargo ``` directory. Here are the [content][link]
```
# 放到 `$HOME/.cargo/config` 文件中
[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"

# 替换成你偏好的镜像源
replace-with = 'sjtu'
#replace-with = 'ustc'

# 清华大学
[source.tuna]
registry = "https://mirrors.tuna.tsinghua.edu.cn/git/crates.io-index.git"

# 中国科学技术大学
[source.ustc]
registry = "git://mirrors.ustc.edu.cn/crates.io-index"

# 上海交通大学
[source.sjtu]
registry = "https://mirrors.sjtug.sjtu.edu.cn/git/crates.io-index"

# rustcc社区
[source.rustcc]
registry = "git://crates.rustcc.cn/crates.io-index"

```

# cargo run restart
Please read the [passage][link2]

# About rustup
Here is a useful [link][link3]

# Rust tutorial
##  dev tools
### cargo-watch
### cargo-limit
### cross
### cargo-edit
This can indicate the dependency version
# About more details
look the [repository][link4]

## primitive types
### fn
function pointer

### bool
### all kinds of numbers
### char
### str

## ownership rules
- Each value in Rust has a variable that’s called its owner.
- There can only be one owner at a time.
- When the owner goes out of scope, the value will be dropped.



[link2]:https://stackoverflow.com/questions/29461693/how-can-i-get-cargo-to-recompile-changed-files-automatically
[link3]:https://www.jianshu.com/p/cf1b534dbb16
[link]:https://learnku.com/articles/49977
[link4]:https://github.com/lmmqxyx404/Rust_Tutorial