# linux-kmod-practice

Reference: [Linuxカーネルモジュール自作入門](https://booth.pm/ja/items/1056339)

## Progress

- [x] Section-1. Introduction
- [x] Section-2. "Hello World" module
- [x] Section-3. Module dissection
- [x] Section-4. "kprobes"
- [x] Section-5. "sysfs"

## Default Usage

```bash
$ make
$ sudo insmod <name>.ko
$ dmesg | tail -n 5
$ sudo rmmod <name>
$ dmesg | tail -n 5
$ make clean
```

## Furthermore

* [Kernel Debugging Using Kprobe and Jprobe](https://www.opensourceforu.com/2011/04/kernel-debugging-using-kprobe-and-jprobe/)
* [Linux カーネルハック実践入門](https://yasukata.hatenablog.com/entry/2020/07/15/141332)
