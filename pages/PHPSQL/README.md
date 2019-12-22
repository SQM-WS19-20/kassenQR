# Function Set

### Defintion
* % shopID
* § productID
* ? Quantity
* $ priceID

### Example:

* shopID(Ted's Grocery)= 43;
* productID(Apple) = 4;   && Quantity = 5;
* productID(Tomato Soup) = 1; && Quantity = 1;


### Resulting String: 
%43§4?5§1?1


### Resulting QR-Code
<img src="https://raw.githubusercontent.com/SQM-WS19-20/kassenQR/master/pages/PHPSQL/rec/IMG/qrcode.png" height="100">



### SQL Request


#### display rows for: 

https://sqm-ws19-20.github.io/kassenQR/pages/UXD/

```
SELECT Shop.Name, product.price, kassenbon.id FROM Kassenbon, Shop, Produkt [...]
WHERE product.ID = kassenbon.productID   [...]
    for( kassenbon.id 1:N ) {
        echo "<a [GOTO: EXAMPLE] ><div class="box">" + shop.NAME + <p> + SUM(product.PRICE) + </p></div></a>
    }
```

#### display rows for: 

https://sqm-ws19-20.github.io/kassenQR/pages/UXD/example.html

```
FUNCTION(EXAMPLE){
    SELECT kassenbon.id FROM Kassenbon, Produkt [...]
        WHERE [...]
            for( item.id 1:N ) {
                echo "<a [...] ><div class="box">" + produkt.NAME + <p> + product.PRICE + </p></div></a>
            }
        }
}
```
