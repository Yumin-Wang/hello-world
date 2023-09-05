# Running Jupyter Notebook on WSL2

1. First set up WSL2 and download Ubuntu distribution following steps on: https://docs.microsoft.com/en-us/windows/wsl/install
   `wsl --install` 

3. Folders and Files can be accessed at: `\\wsl$`

4. use powershell type `wsl -l -v` to check ubuntu versions
   if ubuntu version is 2, change to 1 if you would like to use vpn and use ubuntu as a terminal by following code `wsl --set-version Ubuntu 1`
   
5. Download Anaconda Distribution via:
	```
	wget https://repo.continuum.io/archive/Anaconda3-2020.07-Linux-x86_64.sh
	bash Anaconda3-2020.07-Linux-x86_64.sh
	```
6. Install Jupyter Notebook

	```
	sudo apt-get update
	sudo apt install jupyter-core
	sudo apt install jupyter
	```

7. Open jupyter notebook by `jupyter notebook --no-browser`

8. Set GitHub Personal Access Token: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

9. To solve `command conda not found` error when already downloaded anaconda as step 3
  - find where `conda` is installed. Use `pwd` to find present working directory. Usually it's at `/home/YourWSLUserName/anaconda3/bin` if you didn't change any setup. for example `/home/yumin/anaconda3/bin`. 
  - add `export PATH=$PATH:/home/yumin/anaconda3/bin` to your `~/.bashrc` file by nano `~/.bashrc`.

  - add `export PATH=$PATH:/home/yumin/mambaforge/bin` to your `~/.bashrc` file by nano `~/.bashrc`. to enable mamba in mambaforge

Reference: [http://mcb112.org/w00/w00-section.html](http://mcb112.org/w00/w00-section.html)
