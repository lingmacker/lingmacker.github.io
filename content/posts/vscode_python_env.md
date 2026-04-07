---
title: "Vscode_python_env"
date: 2026-04-07T17:57:47+08:00
draft: true
---

### Visual Studio Code Python 开发环境配置

1. 插件安装

   - Pyhton、Pylance、Python Debugger，核心插件。
   - Ruff 代码格式化以及问题检查等。
   - Code Runner，运行 python 文件或项目。

2. 插件配置

   - Ctrl + Shift + P，打开命令面板，搜索**首选项：打开用户设置(JSON)**

   - Python 插件配置

     ```json
     "python.terminal.executeInFileDir": true,  // cd到python目录执行
     "python.terminal.activateEnvironment": true  // 打开终端自动激活虚拟环境
     ```

   - Code Runner 配置

     ```json
     "code-runner.runInTerminal": true, // 在terminal中执行
     "code-runner.fileDirectoryAsCwd": true, // cd到python目录执行
     ```

   - PYTHONPATH 配置

     不配置这个可能运行项目的时候找不到包，Pycharm 中会自动配置这个。

     ```json
     "terminal.integrated.env.linux": {
         "PYTHONPATH": "${workspaceFolder}/"
     },
     "terminal.integrated.env.windows": {
         "PYTHONPATH": "${workspaceFolder}/"
     },
     "terminal.integrated.env.osx": {
         "PYTHONPATH": "${workspaceFolder}/"
     },
     ```

     

   
