## Candy Sale

![Screenshot 2022-12-05 at 2 35 40 PM](https://user-images.githubusercontent.com/89284873/205737906-b595d61a-a2e2-4bff-87b3-b930fe7e0048.png)
![Screenshot 2022-12-05 at 2 35 52 PM](https://user-images.githubusercontent.com/89284873/205737949-5908ace5-712e-478e-9af5-e27ff810223e.png)

```
const body = document.querySelector("body");

function getSaleItems(data){
    // get sweets
    let shoppingCart = data.filter(({item, price, type}) => {
        return type === "sweet";
    }).map(({item, price, type}) => {
        return {item, price};
    })
    // render
    shoppingCart.forEach(({item, price}) => {
        body.innerHTML += `
        <div class="candy">
          <p>${item}</p>
          <p>${price}</p>                    
        
        </div>
        `
    })
};

getSaleItems(products);
```

## Shh.. whispering function

![Screenshot 2022-12-05 at 2 59 03 PM](https://user-images.githubusercontent.com/89284873/205741543-9b46340f-260f-4bbe-bdca-36b0f8b00af9.png)
```
function whisper(sentence) {
    if (sentence.includes("!")) {
        let s = sentence.replaceAll("!", ".");
        return `shh... ${s.toLowerCase()}`;
    } else {
        return `shh... ${sentence.toLowerCase()}`;
    }
}

console.log(whisper("PLEASE STOP SHOUTING."));
console.log(whisper("MA'AM, this is a Wendy's!"));
```
