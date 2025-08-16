# jbang-groovy-launcher
Use jbang to run any groovy script
## Jbang download
https://www.jbang.dev/download/ 

### Windows
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
jbang -Dscript="yourGroovyScript.groovy" https://gist.github.com/automationStati0n/d8d28cfb7a68592c79fd052419597e04
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
