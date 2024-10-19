*UI* is client side and *business logic* is server-side
## MVC of Early Web Apps 
- Model on *server* sends webpage to *browser* to render View 
- Controller in *browser* sends events to Model on *server*
- Model processes changes and sends new webpage to *browser*
![[Pasted image 20240227212854.png]]

## MVC of Single Page Application (SPA)
- Browser handles full MVC Cycle 
![[Pasted image 20240227212959.png]]

## Git Concepts 
![[Pasted image 20240227213105.png]]
![[Pasted image 20240227213127.png]]

`.gitignore`: File to specify things that you don't want to commit 

### VSCode Shortcuts 
- `ctrl + SHIFT  + P ` : Command Pallet 
- `ctrl + SHIFT + ~ ` : New Terminal 
- `ctrl + J` : Hide terminal 
- `ctrl + .` : Fix Problem 
- `shift + alt + F`: Set Formatter 

#### Font Ligatures 
**Ligature**: unique character created by joining multiple characters 
![[Pasted image 20240227221120.png]]
## Node.js
- JS Run-time environment 
- Event driven and asynchronous 
- Use **nvm** (Node Version Manager)

### npm 
Node Package Manager. Responsible for installing packages 
#### Common Commands 
![[Pasted image 20240227221248.png]]
#### Package.json
- list of all packages installed in project 
- every npm install adds to this file, often with many dependent packages as well
- has information to re-create installed packages node init # if package.json exists, installs all packages
#### npx (Node Package Execute)
Execute command from an npm package 
`npx some-package`

## Chrome 
Web browser that uses *V8 JavaScript Engine* which is written in C++. Two main components are 
- **Interpreter**: reads JS code and executes it directly
- **Just-in-time (JIT) Compiler**: compile frequently executed code to machine code 

Chrome also uses the *Blink Rendering Engine*. It implements the DOM 

## Vite 
Tooling framework that has:
 - **Dev Server**: Runs code on a web server locally 
 - **Build Command**: Bundles code for deployment to prod