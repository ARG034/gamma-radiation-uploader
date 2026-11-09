# gamma-radiation-uploader:

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Flet](https://img.shields.io/badge/Flet-DA291C?style=flat)

This repo uses [cdump/radiacode](https://github.com/cdump/radiacode) to connect your computer to a radiacode-102 device and catch its lectures in order to send them to an existing database.Additionally in order to make it more pleasing to the user,in [App](./App) we have the necesary files in order to create a simple linux desktop app. Work in progress - For now its Linux compatible but Im working in an easier way to pack all the program dependencies

## Radiacode_info_uploader:

In this directory you will find :

* **Dependecies Instalation**: You will find a python3 script that installs the dependencies necesaries to run /Program.In this directory there is also a .bat for windows but its not finished.
* **Program**:Here is /radiacode_data_uploader.py.Once every dependency is installed this program contains all the logic behind this project it connects to the radiacode device plugged via USB (BLUETOOTH conection isnt supported yet)and using json format it uses OpenRed API to send the data allong with the user location wich is obtained scanning every wifi available,usig their IPs for more precision we use an open library to triangulate the user location as almost every PC doesnt have GPS incorporated and we avoided using APIs wich require token $ID == $ Payment.

## App:

![Radiacode App Screenshot](App/screenshot.png)

I recommend running it in a virtual envoiroment

Since it was our first time using flet or building an executable app this version has a lot of work to be done.I encourage people to upgrade it,but it basically uses [Program](./Radiacode_info_uploader/Program) logic and combine it with some visual elements.

In [Flet App](./App) you will find every python script needed to run :

```bash
flet build linux
