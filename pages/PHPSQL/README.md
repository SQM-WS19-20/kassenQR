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


Resulting String: %43§4?5§1?1


### QR

![Image of Yaktocat](https://raw.githubusercontent.com/SQM-WS19-20/kassenQR/master/pages/PHPSQL/rec/IMG/qrcode.png)


### SQL Request


#### display rows for: 

https://sqm-ws19-20.github.io/kassenQR/pages/UXD/

```
SELECT Shop.Name, product.price, kassenbon.id FROM Kassenbon, Shop [...]
WHERE product.ID = kassenbon.productID   [...]
    while([...] ) {
        echo "<a [...] ><div class="box">" + shop.NAME + <p> + SUM(product.PRICE) + </p></div></a>
    }
```

#### display rows for: 

https://sqm-ws19-20.github.io/kassenQR/pages/UXD/

```
SELECT Shop.Name, product.price, kassenbon.id FROM Kassenbon, Shop [...]
WHERE product.ID = kassenbon.productID   [...]
    while([...] ) {
        echo "<a [...] ><div class="box">" + shop.NAME + <p> + SUM(product.PRICE) + </p></div></a>
    }
```
