---
layout: wiki
title: 工具使用总结
categories: Tools
description: 工作中工具使用总结
keywords: Tools
---

### Glaunch  

* command: /local/sandbox/scm/phx-> /local/myglaunch76  

### TraceBoard  
* Conrotl start, stop and clear through IP in browser  
* Get log: getTrace_db 15.96.136.151 /local/sandbox/scm/phx/EXE/debuglist Trace_withoutaoao_OK.log
* Set checkpoint level: vim src/gen/homer2.0/linux-86/gh517-arm/debug/GNUmakefile.dbg

## DownloadFirmware  
* ddb: /local/sandbox/scm/phx/exe/gen/homer/linux-x86/gh517-arm/debug->download -n -p 15.33.204.103 homer.bbd  
* cat phx.1.rfu > /dev/usb/lp0
* hpnpf -x 15.96.146.53 phx.1.rfu
* Homer can't be reprogarmmed by download and hpnpf command, because it's rom version, need reprogram using special version first.

## Send file to printer
* hpnpf -x 15.33.204.115 landscape.pcl

## Compile error solution
* License error: open phx/tools/linux-x86/gh201314pT2-arm/bin/ghs  Copy url from latest commit and replace the old file.

## Auto test  
* VNC Viewer: 15.96.138.61:8
* Password: bys_010
* temrc file path: .temconfig/
* Edit temrc_Yangfan and run tem --config temrc_Yangfan --gui
* Choose test cases in test/phx_test/config/ews/auto/xxxx.tst
* Plugout connection in GUI and run the selected test case. Test log will be saved in a tar file and the path will show after finished.

## bbd to rfu
* download -n -b0 nebula.bbd -o nebula.rfu

## Python script debug
* tem --testspl ews_security EWS_alllinksSecurityTest

## Repo,git,Gerrit
* A working Repo flow:
```
1. mkdir CR63440
2. repo init -u git.boi.rd.hpicorp.net:phx-manifests -b phx -m release/nebula1.0.xml
3. repo sync
4. repo start nebula1.0 --all
5. git cherry-pick xxxxx
6. post-review
```    
## License compile fail    
 gvim scm/phx/tools/linux-x86/nowcompiler/ghs
 gvim scm/phx/tools/linux-x86/newestcompiler/ghs
 copy newer to now.
