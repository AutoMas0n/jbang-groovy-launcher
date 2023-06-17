# jbang-groovy-launcher
Use jbang to run any groovy script
## Jbang download
https://www.jbang.dev/download/  
*You may have to run `Set-ExecutionPolicy RemoteSigned -scope CurrentUser` & then `iex "& { $(iwr https://ps.jbang.dev -UseBasicParsing) } app setup"` if using powershell*
### Download Jbang using Choco
https://chocolatey.org/install  
## Usage
```bash
git clone https://github.com/automationStati0n/jbang-groovy-launcher
cd jbang-groovy-launcher
jbang -Dscript="yourGroovyScript.groovy" main.java
``` 
or  
```bash
jbang -Dscript="yourGroovyScript.groovy" https://gist.github.com/automationStati0n/2854188e8e75b5266f97ef25f912f956
```
## Extras
You can pass in as many properties and arguments as you want with jbang and be able to access them from your groovy script
```bash
jbang -Dtest="Hello World!" main.java hello.groovy myarg1
```
hello.groovy:
```groovy
println "${args[0]}"
println "${System.properties['test']}"
```
result:
```text
myarg1
Hello World!
```
