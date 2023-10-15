========== HOW TO PREPARE BUILDER ==========

Step 1: Change the Git path in Dockerfile
CMD git clone https://github.com/yaneurao/YaneuraOu.git -b v5.33 && \

Step 2: Replace the Makefile with the correct revision of Makefile in the repository

Step 3: Inside the Makefile, change the following settings:
TARGET_CPU = SSE42, COMPILER = g++


========== HOW TO BUILD ENGINES ==========

Step 1: Set up Docker
Install Docker on your system if you haven't already. You can download Docker for your platform from the official website: https://www.docker.com/get-started

Step 2: Navigate to folder
Open a terminal (command prompt or PowerShell on Windows).
Navigate to the directory containing your Dockerfile and Makefile using the cd command. For example, if your files are in the ~\shogi-api\builder\YO488 directory:
	cd ~\shogi-api\builder\YO488

Step 3: Build the Engine Inside Docker
	docker build -t yo488 .

Step 4: Run a Docker container
Start the "Docker Desktop" porgram installed on step 1, the new image "yo488" should be shown in "Images". Click "Start" from the actions to run a container for this image.

Step 5: Download the engine build
After a successful build, the engine "YaneuraOu-by-gcc" should be found under "/work/YaneuraOu/source/" in the container's file directory. Right-click to save it on your host computer.
