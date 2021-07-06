# Resume Website on Azure
My own resume website built using Azure services

## Architecture
![alt text](https://github.com/mumanoha/azure-resume/blob/main/architecture.png?raw=true)

## First steps

- Fronteend folder contains the website.
- main.js contains visitor counter code.

```js
window.addEventListener('DOMContentLoaded', (event) =>{
    getVisitCount();
})

const functionApi = '';

const getVisitCount = () => {
    let count = 30;
    fetch(functionApi).then(response => {
        return response.json()
    }).then(response =>{
        console.log("Website called function API.")
        count = response.count;
        document.getElementById("counter").innerText = count;
    }).catch(function(error){
        console.log(error);
    });
    return count;
}
```