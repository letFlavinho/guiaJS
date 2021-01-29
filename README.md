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
    
In this feature i just did the same thing but in this case you can imagine a store selling everything by half of the price, i create an array with all the prices, then i build new const with all the prices by the half. 
