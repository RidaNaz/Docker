# Docker Installation

## 1. Enable Virtualization
* On your laptop/pc and press `esc`. (then you got this)

![App Screenshot](/public/img-1.jpeg)

* Press `f10`

![App Screenshot](/public/img-2.jpeg)

* Go to `Device Configurations`

![App Screenshot](/public/img-3.jpeg)

* Tick Virtualization Technology (Vtx)

* **Then confirm that 'virtualizaion is enabled'**

- Right click  task bar and select **Task Manager**, then go to **Performance**

![App Screenshot](/public/img-4.jpg)

- Congratulaions if virtualization is `enabled`!

## 2. On Windows Features

* Go to ***Windows*** then type "windows fetaures on or off", open it.

![App Screenshot](/public/img-5.jpg)

* Tick the following:
    - Containers
    - Hyper-V
    - Virtual Machine Platform
    - Windows Hypervisor Platform
    - Windows Subsystem for Linux

## 3. Install WSL

* type `powershell` in windows and right click it and choose `run as adminstrator`.

![Ss](/public/img-6.jpg)

* Run the following commands:
    - wsl --list --online
    - wsl --install -d Ubuntu-24.04

* the you got the new terminal window.
    - give username and password

![Ss](/public/img-7.jpg)

## 4. Upgrade version from WSL 1 to WSL 2

![Ss](/public/img-8.jpg)

* After checking that you have `version-1`, run the following commands:
    - wsl --install
    - wsl --set-version
    - wsl --set-version Ubuntu-24.04 2

* Run `wsl.exe --install` / `wsl.exe --update` (when WSL 2 requires an update to its kernel component)

* Now, re-run the `wsl --set-version Ubuntu-24.04 2` for conversion and also run `wsl -l -v` to check the version.

![Ss](/public/img-9.jpg)
