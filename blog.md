# 处理问题的简单日志

<!-- ## 目录

Table Contents

- [About Git](#about-git)
- [About VScode](#about-vscode)
- [About Ubuntu](#about-ubuntu) -->

## About Git

`git reset --soft HEAD^` 取消上一次 commit

---

突然想重命名一下远程分支名。

```bash
git checkout -b main
git push origin main
git push origin --delete master
git fetch --prune
```

但是失败。

```txt
To github.com:Topology2333/Notes-2024.git
 ! [remote rejected] master (refusing to delete the current branch: refs/heads/master)
error: failed to push some refs to 'git@github.com:Topology2333/Notes-2024.git'
```

原因是 master 被设置为 default 了。直接在 github 管理界面 rename，再在本地执行以下即可。

```bash
git branch -m main <BRANCH>
git fetch origin
git branch -u origin/<BRANCH> <BRANCH>
git remote set-head origin -a
```

## About VScode

markdown 预览时 `Ctrl+K V`, 而非 `Ctrl+K, Ctrl+V`  
检查过程：打开了 `default keyboard shortcuts` 没问题 hh  
解决：要先松开 `Ctrl`, 参见 [Link](https://github.com/Microsoft/vscode/issues/60063#issuecomment-427585711)

## About Ubuntu

> 已解决

翻译工具 [stardict](https://askubuntu.com/questions/95252/is-there-any-application-tool-for-quick-translations-of-a-selected-word)
, 体验良好。本地存储在 dic.txt  
然而使用一段时间之后会 `Segmentation fault (core dumped)`  
[someone reported this bug](https://bugs.launchpad.net/ubuntu/+source/stardict/+bug/1999288) (unfixed)

解决了。翻开原来的 [askubuntu](https://askubuntu.com/questions/95252/is-there-any-application-tool-for-quick-translations-of-a-selected-word), 发现下面有评论：
"I found that the hotkey function in Stardict works quite unreliably in Ubuntu 14.04"

好吧，我决定放弃这个古物 🌾 转而使用 `goldendict`

---

某日突发奇想要加加 swap 分区，然而遇到报错  
`Can not use Swap file on ZFS: Files with holes`  
参考 [askubuntu](https://askubuntu.com/questions/1198903/can-not-use-swap-file-on-zfs-files-with-holes) [zfsonlinux](https://github.com/zfsonlinux/pkg-zfs/wiki/HOWTO-use-a-zvol-as-a-swap-device)

---

<!-- 为了下载字典而[安装 7-zip](https://gcore.com/learning/how-to-extract-7z-files-linux/)

```shell
sudo apt update
sudo apt install p7zip-full

7za x yourfile.7z #extract, ‘x’ stands for extract
``` -->

<!-- --- -->

> 未解决

处理字典问题，没找到、

---

[解压缩](https://phoenixnap.com/kb/extract-tar-gz-files-linux-command-line)

---

解决 [epub 阅读器](https://askubuntu.com/questions/14378/what-software-can-i-use-to-view-epub-documents)

---

遇到报错

```txt
error: file `ubuntu_7jrd25` not found
you need to load the kernel first
```

解决：

```bash
sudo apt install --reinstall grub-efi-amd64
sudo update-grub
sudo reboot
```

---

```bash
Errors were encountered while processing:  network-manager-gnome  ppp
```

解决

```bash
apt --fix-broken install
```

---

今天收到了朋友买的微软鼠标。不得不说，在 Linux 上使用微软的玩意有一种 ntr 的感觉。

具体体现在，鼠标滚轮用不了。但这应该不是微软的问题。在微软官网上也没看到对 Linux 的支持。

最终解决了，参考这篇博客，修改 [/etc/X11/xorg.conf 文件](https://www.linuxidc.com/Linux/2008-05/12999.htm#:~:text=Ubuntu%20%E4%B8%8B%E9%BC%A0%E6%A0%87%E6%BB%9A%E8%BD%AE%E5%A4%B1%E6%95%88%E4%B8%BB%E8%A6%81%E6%98%AF%E9%85%8D%E7%BD%AE%E4%B8%8D%E6%AD%A3%E7%A1%AE%E5%BC%95%E8%B5%B7%EF%BC%8C%E8%A7%A3%E5%86%B3%E6%96%B9%E6%B3%95%E5%A6%82%E4%B8%8B%EF%BC%9A%201%E3%80%81%E9%94%AE%E5%85%A5sudo,gvim%20%2Fetc%2FX11%2Fxorg.conf%202%E3%80%81%E6%89%93%E5%BC%80%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E4%B9%8B%E5%90%8E%EF%BC%8C%E5%B0%86%E9%BC%A0%E6%A0%87%E9%85%8D%E7%BD%AE%E5%8F%82%E6%95%B0%E9%83%A8%E5%88%86%E6%94%B9%E5%86%99%E6%88%90%E5%A6%82%E4%B8%8B%E5%BD%A2%E5%BC%8F%EF%BC%9A)

---

结果登录界面又出问题了。

选项右下角改一下就好了？
