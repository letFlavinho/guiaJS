# guiaJS
guia pessoal de JavaScript puro

We'll see some functions for arrays here right now


<h2>map()</h2>

    const numbers = [1, 2, 3];
    const doubleNumbers = numbers.map(item => item * 2);
    console.log(doubleNumbers)
    
In this feature i was able to create an array called 'numbers' with 3 numbers inside it in the line 6, line 7 i create another const called 'doubleNumber' that receives the 'numbers' array and aplicate the function 'map()', with this function you can map all the items from your array and do whatever you want with then, in this case i multiplied all the items by 2, then you can see my 'doubleNumbers' const is actually just a way to reuse the 'numbers' const to create another one but with this numbers multiplied by 2. If you run this code in your browser you can see the console will have the array with all the number but multiplied by 2.

Another example of the 'map()' function:

    const prices = [10 , 5, 30, 40, 80, 20];
    const salePrices = prices.map(price => price / 2);
    console.log(salePrices)
    
In this feature i just did the same thing but in this case you can imagine a store selling everything by half of the price, i create an array with all the prices, then i build new const with all the prices by the half. In the next feature we'll see that you can apply the 'map()' to very usefull things in your web application.

        const products = [
        { name: 'Mouse Sem Fio', price: 30 },
        { name: 'Pen Drive', price: 25 },
        { name: 'Cartucho de Tinta', price: 50 },
        { name: 'Suporte Ergonômico para Notebook', price: 23 },
        { name: 'Repetidor de Sinal Wi-Fi', price: 44 }
      ]
    const saleProducts = products.map(product => {
        if(product.price >= 30){
            return { name: product.name, price: product.price / 2}
        }
        return product
    })
    console.log(saleProducts)
    
First we have all the items from the array 'products' then we made a new const called 'saleProducts' that receives the value wich at same time is a function that transform all the prices over 30 by the half, but in this case we have to pass all the parameters because the array will be all changed, thats why i have to return the 'product.name' and the 'price' again.

<h2>filter()</h2>

The 'filter()' function filter it can 5 parameters of an array, 'callback', 'element', 'index', 'array' and 'this arg'. Is only required one os this parameters, in this case i only used the 'element' parameter.

    const randomNumbers = [36, 56, 29, 99];
    const numbersBiggerthan37 = randomNumbers.filter(item => item > 37);

    console.log(numbersBiggerthan37);
    
I created a array called 'randomNumbers' with some random numbers but the idea is to filter the numbers that you want from this array with your parameter, in this case i created another const that filter the numbers that are bigger than 37, in this process the new array is just reusing the elements from the 'randomNumbers' but the 'filter' is filtering the 'elements' that i want, in this case bigger than 37. The result in the console is like 'numbersBiggerthan37 = [56, 99 ]'

In a pratic way, we can use this function to guarantee if some members of your community are premium like in this example.

        const users = [
        { name: 'Ada Lovelace', premium: true },
        { name: 'Grace Hopper', premium: false },
        { name: 'Alan Turing', premium: true },
        { name: 'Linus Torvalds', premium: false },
        { name: 'Margaret Hamilton', premium: true }
      ]

    const premiumUser = users.filter(user => user.premium)
    console.log(premiumUser)

Here we have an array with the users list with a parameter that says if the user is premium or not, the 'filter' can see if is true, when the new const 'premiumUser' is created the 'filter' only filter the users that have a 'true' in the 'premium' parameter and it creates a new array only with members that have premium.
