Hello and welcome to Docker

Here we will go through the installation proccess of Docker Engine and understanding what exactly is Docker and why do we need it.

table of contents
1 what is an image
2 what is a container
3 what is docker
4 Docker installation
5 how to test docker installation
6 quick and easy commands
7 Kubernetes
8 Exercising and understanding docker better - docker testing site

1.What is Docker? What is an Image? What is a Container?

Docker - A tool developed by microsoft in order to eliminate a Worldwide techie problem - " it works on my pc".
Jokes aside, Docker is a contanerization tool that takes your code and makes it into an easy to distibute image in which you can open with no effort on other pcs.
Lets break it down.

Image - an image is like a virtual copy of a pc, with a shell and everything, you can place appropriate apps / code that you want to execute on it.
    Ex: an image called Dylan(User):ExampleImage(Image name) that is running a linux distro of my choise and a small app that when i send it 2 different numbers it will send me it back.

Container - When we talked about image you can imagine it as more of the software side of the virtual machine, but the Container is like the hardware of the pc, meaning you allocate specific hardware from the original pc (lets say your current PC/Mac), like ram, cpu and storage, in order for the image to work and be able to do so as efficiant as you want, Docker engine AUTOMATICALY take as much as it needs without overconsuming your hardware resources but you can still limit its amount, also the Container allows me to contact the Image inside, which allows me to see its status, procedures, logs and interact with the application inside. 
    Ex: my previous app as you have seen above doesn't do much other than take two number and sends it back, meaning its not that hardware intensive, allowing me to let Docker engine to take as it needs without worring, afterwards i check the container via docker -status container name so on and so forth

Docker Engine Installation

To install Docker engine on your system head over to Docker's official site on https://www.docker.com/products/docker-desktop/ 
there you will be able to see an installation box and you will have to choose a download specific to your machine
(add photo here downloaddocker.png)


Testing That Docker is installed properly

After downloading and signing up open up your terminal of choice, in my case i have MacOs Terminal, and do the following command to see if docker is properly installed and that you are able to interact with it:

make it so you can copy paste it - docker --version

add photo of terminal with output

If you recvived a message back with "Docker version ..." then you are set to go and test out docker!
If by any chance you have gotten an error message instead, please check that wsl2 is installed on your machine, if you are on windows please ensure that 'Virtual Machine Platform', is enabled.
if the error persists, try to redownload docker.

Kubernetes

If you want to dive deeper into the rabbit hole you can try out Kubernetes
Kubernetes is an open-source platform for automating the deployment, scaling, and management of containerised applications. It helps coordinate clusters of servers, ensuring applications run efficiently and reliably across different environments.

to activate Kuberenetes - Open Docker engine, Go to setting at the top right of the window, To your left you will se a setting called 'Kubernetes' enter it, switch kubernetes on, Dont forget to press APPLY after in the bottom right.
WARNING: Having Kubernetes active in the background may slow down your system since Docker and Kubernetes are system Ram and Cpu heavy.

add aproptiate images here

To check and see if Kubernetes is active, go to your terminal and put in the following command

kubectl get nodes

add image of terminal here

if you get this message, great! kubernetes is active.
if by any chance you get an error instead, check to see if kuberenetes has installed on your Docker enginge, if it has, turn it off and on, or try to restart your system.

Exercising and understanding Docker