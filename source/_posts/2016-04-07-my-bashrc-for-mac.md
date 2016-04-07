---
title: 一些用得到的MAC下面的bashrc配置
date: 2016-04-07 14:41:52
tags: 
  - bash
  - java
---

```bash
export JAVA_6_HOME=/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
export JAVA_7_HOME=/Library/Java/JavaVirtualMachines/jdk1.7.0.jdk/Contents/Home
export JAVA_8_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
export JAVA_HOME=$JAVA_6_HOME

alias jdk8='export JAVA_HOME=$JAVA_8_HOME'
alias jdk7='export JAVA_HOME=$JAVA_7_HOME'
alias jdk6='export JAVA_HOME=$JAVA_6_HOME'

alias flushdns='sudo killall -HUP mDNSResponder'
alias resetLunchpad='defaults write com.apple.dock ResetLaunchPad -bool true; killall Dock'
```

说明：

1. 切换JAVA环境，使用命令 `jdk8` `jdk7` `jdk6` 就可以切换本机的JAVA环境，以便于需要不同java版本的开发调试工作
2. 命令 `flushdns` 可以快速的清除本机的dns缓存，用于切换hosts以后有缓存不及时生效的情况
3. 命令 `resetLunchpad` 更新Dock和lanchpad的app列表缓存并重置Dock