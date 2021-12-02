## A Complete Beginner's Guide to Solidity

Solidity is an object-oriented, high-level programming language for creating smart contracts on the blockchain that automate transactions. The language was created by participants to the Ethereum project when it was proposed in 2014. This language is mostly used to make smart contracts on the Ethereum blockchain.

According to its documentation, "Solidity is a curly-bracket language. It is influenced by C++, Python, and JavaScript, and is designed to target the Ethereum Virtual Machine (EVM)."

Solidity is also considered a dialect of JavaScript. This implies that if you know JavaScript, learning Solidity should be simple. Before learning more about solidity let's understand some basic terms of blockchain.


## Ethereum Virtual Machine

The Ethereum Virtual Machine (EVM) is the Ethereum smart contract runtime environment. The Ethereum Virtual Machine is focused on providing security and allowing machines all around the world to execute programs.

Virtual machines effectively create a layer of abstraction between the code and the machine that executes it. It is required to promote software portability and to ensure that programs are isolated from one another and from their host.

The Ethereum Virtual Machine was created to serve as a runtime environment for Ethereum-based smart contracts.
![Solidity (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633147481115/4fOoXr7hf.png)


## Smart Contract

A smart contract is a decentralized program that responds to events by executing business logic. The exchange of money, delivery of services, unlocking of information controlled by digital rights management, and other forms of data manipulation, such as altering the name on a property title, are all possible outcomes of smart contract execution. Smart contracts are often written in Solidity.

Smart contract languages like Solidity cannot be directly executed by the Ethereum Virtual Machine. They are instead converted to low-level machine instructions called opcodes.

Now that you have an idea about EVM and Smart Contract, we can continue learning about the Solidity

## Environment Setup 

Before installing Solidity, you need to make sure that you have Node.js and NPM installed on your computer. To install node.js in your Linux (Ubuntu) you can follow this   [article](https://blog.suhailkakar.com/how-to-install-nodejs-and-npm-on-ubuntu). 

Once you have successfully installed Node.js and NPM in your machine, you can proceed to install Solidity compiler as below:

```
sudo npm install -g solc 

```

The command above will install the Solcjs and make it available globally throughout the system. Now you can run 

```
solcjs --version
```
If everything goes fine, you see something similar to below in your terminal 

```txt
0.8.9+commit.e5eed63a.Emscripten.clang
```


> You can also use an online editor called Remix IDE to Compile and Run your Solidity code.




## Reserved Keywords

Following are the reserved keywords in Solidity:
<table>
<tbody><tr>
<td>abstract</td>
<td>after</td>
<td>alias</td>
<td>apply</td>
</tr>
<tr>
<td>auto</td>
<td>case</td>
<td>catch</td>
<td>copyof</td>
</tr>
<tr>
<td>default</td>
<td>define</td>
<td>final</td>
<td>immutable</td>
</tr>
<tr>
<td>implements</td>
<td>in</td>
<td>inline</td>
<td>let</td>
</tr>
<tr>
<td>macro</td>
<td>match</td>
<td>mutable</td>
<td>null</td>
</tr>
<tr>
<td>of</td>
<td>override</td>
<td>partial</td>
<td>promise</td>
</tr>
<tr>
<td>reference</td>
<td>relocatable</td>
<td>sealed</td>
<td>sizeof</td>
</tr>
<tr>
<td>static</td>
<td>supports</td>
<td>switch</td>
<td>try</td>
</tr>
<tr>
<td>typedef</td>
<td>typeof</td>
<td>unchecked</td>
<td></td>
</tr>
</tbody></table>


## Importing other files in Solidity  

Importing a file in Solidity is similar to JavaScript, to import a file you can simply write

```js
import "file";
```
All global symbols from the "file" are imported into the current global scope by the above statement. But if you want to create a new global symbol someName with all the global symbols from "file" as members, you can write

```js
import * as someName from "file";
```
## Comments in Solidity

Just like other programming languages, Solidity support both single-line and multi-line comments. 


- Start the line with `//` to include a single-line comment.
- Start with `/*` and end with `*/` to include a multi-line comment.

```js
 // This is a single-line comment
 ```
```js
 /*
   but this is a multi-line comment in solidity
   It is easy, right?
 */
```

## Variables in Solidity

There are mainly two types of variables available in Solidity.

- **Local Variables**: Variables with values that will **persist** till the function is completed
- **State Variables**: Variables whose values are kept in a contract storage system permanently

### State variable

State variables store the value permanently in the contract storage. Each method should have its own scope, and state variables should be declared outside of any defined functions.


![State variable.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633149710337/iEqkLKqc4.png)

### Local Variable

A local variable's context is contained within the function, and it cannot be retrieved from outside of it. These variables are typically used to store temporary values.


![Local variable.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633149968342/Cp9CXU1Bv.png)

## Operators in Solidity
Operators are important in every programming language because they establish the groundwork for the programming. Similarly, the functionality of Solidity is also incomplete without the use of operators.

Solidity supports the following types of operators:
- Arithmetic Operators
- Relational Operators
- Logical Operators
- Bitwise Operators
- Assignment operators
- Conditional Operators


However in this article we are going to study only 3 of them but in future article I will try to explain all of them :)

### Arithmetic Operators

These operators are used to perform mathematical operations. 

<table><thead><tr><th>Operator</th><th>Denotation</th><th>Description</th></tr></thead><tbody><tr><td>Addition</td><td>+</td><td>Used to add two operands</td></tr><tr><td>Subtraction</td><td>–</td><td>Used to subtract the second operand from first</td></tr><tr><td>Multiplication</td><td>*</td><td>Used to multiply both operands</td></tr><tr><td>Division</td><td>/</td><td>Used to divide numerator by denominator</td></tr><tr><td>Modulus</td><td>%</td><td>Gives the remainder after integer division</td></tr><tr><td>Increment</td><td>++</td><td>Increases the integer value by one</td></tr><tr><td>Decrement</td><td>—</td><td>Decreases the integer value by one</td></tr></tbody></table>

### Relational Operators

These operators are used to compare two values

<table><thead><tr><th>Operator</th><th>Denotation</th><th>Description</th></tr></thead><tbody><tr><td>Equal</td><td>==</td><td>Checks if two values are equal or not, returns true if equals, and vice-versa</td></tr><tr><td>Not Equal</td><td>!=</td><td>Checks if two values are equal or not, returns true if not equals, and vice-versa</td></tr><tr><td>Greater than</td><td>&gt;</td><td>Checks if left value is greater than right or not, returns true if greater, and vice-versa</td></tr><tr><td>Less than</td><td>&lt;</td><td>Checks if left value is less than right or not, returns true if less, and vice-versa</td></tr><tr><td>Greater than or Equal to</td><td>&gt;=</td><td>Checks if left value is greater and equal than right or not, returns true if greater and equal, and vice-versa</td></tr><tr><td>Less than or Equal to</td><td>&lt;=</td><td>Checks if left value is less than right or not, returns true if less and equals, and vice-versa</td></tr></tbody></table>

### Logical Operators

These operators are used to combine two or more conditions

<table><thead><tr><th>Operator</th><th>Denotation</th><th>Description</th></tr></thead><tbody><tr><td>Logical AND</td><td>&amp;&amp;</td><td>Returns true if both conditions are true and false if one or both conditions are false</td></tr><tr><td>Logical OR</td><td>||</td><td>Returns true if one or both conditions are true and false when both are false</td></tr><tr><td>Logical NOT</td><td>!</td><td>Returns true if the condition is not satisfied else false</td></tr></tbody></table>

This is just part 2 of Web 3.0 however in the future we will discuss more about the solidity. 

## Conclusion

That is it for this article. I hope you found this article useful, if you need any help please let me know in the comment section. 

Would you like to buy me a coffee, You can do it [here](https://www.buymeacoffee.com/suhailkakar).

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/). 

👋 Thanks for reading, See you next time
