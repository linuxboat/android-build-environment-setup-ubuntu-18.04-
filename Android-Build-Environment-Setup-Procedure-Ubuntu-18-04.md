sudo apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 libncurses5 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig

Prerequisites:
	Repo and Git Configuration:
			Installing Repo
			  
			  sudo apt-get update
			  sudo apt-get install repo
			 
			 If repo command not detected Then follow bellow manual installation steps	
				$ cd ~
				$ mkdir bin
				$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
				$ chmod a+x ~/bin/repo
				$ export PATH="~/bin:$PATH"
				
				(from /usr/bin/repo) indicates installation from a package.
				(from /home/<>/bin/repo) indicates manual installation.
				
	Initializing a Repo client:
		
		mkdir WORKING_DIRECTORY
		cd WORKING_DIRECTORY
		
		git config --global user.name Your Name
		git config --global user.email you@example.com
		
		repo init -u https://android.googlesource.com/platform/manifest
		repo init -u https://android.googlesource.com/platform/manifest -b master
		repo sync -c -j8


