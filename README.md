## Experimental aarch64 based Android emulator on Github runner

### Getting Started
For connection this package uses [bore](https://github.com/ekzhang/bore)  
To use the emulator you can start by forking this repository.  
To start the emulator you can go to Action tab and manually start the CI workflow.  
You can get the bore.pub port from 'run bore' section.  
```bash
## It wil be listed like this 
listening at bore.pub:2344
```

### Connect to emulator from client
Install required package

```bash
sudo apt update
sudo apt install cargo adb scrcpy
```
Then connect to devices using adb and mirror using [scrcpy](https://github.com/Genymobile/scrcpy)

```bash
adb connect bore.pub:2344
scrcpy -s bore.pub:2344
```
### TODO
- Add GMS
- Create custom tunnel for scrcpy
- ...
