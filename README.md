<Image src="/Ridalogo.png" alt="logo" width="50" height="50" align="left"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Roboto+Slab&weight=500&size=25&duration=4000&pause=500&color=CFB53B&center=true&vCenter=true&width=665&height=55&lines=%E2%9C%A8Hey%2C+I'm+Rida+Naz%E2%9C%A8;%E2%9C%A8Install+Docker+with+Me%E2%9C%A8;%E2%9C%A8Rate+my+GitHub+Repository%E2%9C%A8)](https://git.io/typing-svg)

<p align="left"> <img src="https://komarev.com/ghpvc/?username=ridanaz&label=Profile%20views&color=0e75b6&style=flat" alt="ridanaz" /> </p>

<h1> Docker Installation <h1>

## 1. Enable Virtualization (for 'HP')
* On your laptop/pc and press `esc`. (then you got this page)  Press `f10` for **BIOS setup**

![App Screenshot](/public/img-1.jpeg)

* In `advance` section, go to `Device Configurations`

![App Screenshot](/public/img-2.jpeg)

* Tick `Virtualization Technology (Vtx)`

![App Screenshot](/public/img-3.jpeg)

* **Then confirm that 'virtualizaion is enabled'**

- Right click  task bar and select **Task Manager**, then go to **Performance**

![App Screenshot](/public/img-4.jpg)

- Congratulations if virtualization is `enabled`!

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

* Run the following commands:
    - wsl --list --online
    - wsl --install -d Ubuntu-24.04

![Ss](/public/img-6.jpg)

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

## 5. Install Docker Dekstop

[for downloading, visit:](https://www.docker.com/products/docker-desktop/)

![Ss](/public/img-10.jpg)

* After downloading the docker dekstop, install it and `sign-in` with your google account.

* Finally, you got docker dekstop!

![Ss](/public/img-11.jpg)
 

### 6. ***Check docker version with `docker -v` and `docker version`***

![Ss](/public/img-12.jpg)


## 🔗 About Me

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ridanaz67/)

[![linkedin](https://img.shields.io/badge/linkedin-E1306C?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/rida_naz67/)

[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://rida-portfolio-virid.vercel.app/)