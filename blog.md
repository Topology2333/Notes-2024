# 处理问题的简单日志

<!-- ## 目录

Table Contents

- [About Git](#about-git)
- [About VScode](#about-vscode)
- [About Ubuntu](#about-ubuntu) -->

## About Git

`git reset --soft HEAD^` 取消上一次 commit

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
