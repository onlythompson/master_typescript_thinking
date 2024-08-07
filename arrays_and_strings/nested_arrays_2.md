# From Russian Dolls to Mathematical Scrolls: The Nested Array-Matrix Connection

Welcome back, data structure adventurers and mathemagicians! Remember our journey through the world of Nested Arrays, those Russian nesting dolls of the programming realm? Well, hold onto your wizard hats, because we're about to discover how those very same nested arrays transform into the powerful magical scrolls known as Matrices! Let's embark on this interdimensional adventure! 🌠🔮

## The Great Transformation: From Nested Arrays to Matrices 🦋

Imagine our Russian nesting dolls (nested arrays) suddenly unfolding and arranging themselves into a perfect grid formation. That's essentially what happens when we use nested arrays to represent matrices!

```TypeScript
const nested_array: number[][] = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

console.log("Behold! This nested array is also a 3x3 matrix!")
```

## The Magical Properties: Nested Arrays vs. Matrices 🎭

Let's compare the magical properties of our nested arrays and matrices:

1. **Dimensional Flexibility:**
   - Nested Array: "I can nest as deep as you want! Arrays within arrays within arrays!"
   - Matrix: "I prefer to keep things 2D, thank you very much. Rows and columns are my jam!"

2. **Element Access:**
   - Nested Array: `nested_array[i][j]`
   - Matrix: Also `matrix[i][j]` (Surprise! They're the same!)

3. **Use Cases:**
   - Nested Array: "I'm great for representing hierarchical data like file systems or JSON!"
   - Matrix: "I excel at mathematical operations and representing grids or tables!"

## Adventuring Through the Nested Array-Matrix Multiverse 🌌

### Level 1.1: The Shape-Shifter's Challenge 🦎

Remember our treasure map? Let's transform it into a matrix and back!

```TypeScript
const printMap = (nested_map) => {
    for(let row of nested_map):
        console.log(row.join(" "))
}

const treasure_map: string[][] = [
    ["🌳", "🌊", "🌳"],
    ["🌊", "💎", "🌳"],
    ["🌳", "🌊", "🌳"]
]

console.log("Our Nested Array Treasure Map:")
printMap(treasure_map)
```
### Level 1.2: Traversing a Matrix 🚶‍♂️

Imagine you're an explorer in a strange land represented by a matrix. How do you visit every location?

```TypeScript
const exploreMatrix = (matrix:string[][]) => {
    for(let i = 0; i < matrix.length; i++) { // For each row
        for(let j = 0; j < matrix[0].length; j++){ // For each column in the row
            console.log(`Visiting coordinate (${i},${j}): ${matrix[i][j]}`)
        }
    }
}

magic_land = [
    ["🌳", "🏰", "🌳"],
    ["🌊", "🗻", "🌊"],
    ["🏜️", "🌋", "🏜️"]
]

exploreMatrix(magic_land)
```

### Level 2.1: Transposing a Matrix 🔄

Transposing a matrix is like looking at our magical land from a different angle – we swap rows and columns!

```TypeScript
const transposeMatrix = (matrix:string[][]) => {
    for(let i = 0; i < matrix.length; i++){
        for(let j = i + 1; j < matrix.length; j ++){
            const temp = matrix[i][j]
            matrix[i][j] = matrix[j][i]
            matrix[j][i] = temp
        }
    }
}

original_land = [
    ["🌳", "🏰", "🌳"],
    ["🌊", "🗻", "🌊"]
    ["🏜️", "🌋", "🏜️"]
]

transposed_land = transposeMatrix(original_land)
console.log("Original land:")
exploreMatrix(original_land)
consolo.log("\nTransposed land:")
exploreMatrix(transposed_land)
```
## The Mathemagician's Toolbox: Matrix Operations 🧰

### 1. The Adder's Stone: Matrix Addition ➕

Adding matrices is like combining two magical lands into one!

```TypeScript
const addMatrices = (matrix1: number[][], matrix2: number[][]): number[][] => {
    return [[matrix1[i][j] + matrix2[i][j] for j in range(len(matrix1[0]))] for i in range(len(matrix1))]
    let result_matrix: number[][] = []
    for(let i = 0; i < matrix1.length; i++){
        result_matrix[i] = []
        for(let j = 0; j < matrix1.length; j++){
            result_matrix[i][j] = matrix1[i][j] + matrix2[i][j]
        }
    }
    return result_matrix
}

land_of_numbers = [
    [1, 2],
    [3, 4]
]

land_of_magic = [
    [10, 20],
    [30, 40]
]

combined_land = addMatrices(land_of_numbers, land_of_magic)
console.log("Combined Magical Number Land:")
exploreMatrix(combined_land)
```

### 2. The Multiplier's Wand: Matrix Multiplication ✖️

Multiplying matrices is where the real magic happens! It's like casting a complex spell that transforms our magical land.

```TypeScript
const multiplyMatrices = (matrix1:number[][], matrix2:number[][]):number[][] => {
    let result_matrix : number[][] = Array.from({ length: matrix2[0].length }, () => Array.from({ length:matrix1.length }, () => 0))
    for(let i = 0; i < matrix1.length; i++){
        for(let j = 0; j < matrix2[0].length; j++){
            for(let k = 0; k < matrix2.length; k++){
                result_matrix[i][j] += matrix1[i][k] * matrix2[k][j]
            }
        }
    }

    return result_matrix
}

spell_components = [
    [1, 2],
    [3, 4]
]

magical_catalyst = [
    [2, 0],
    [1, 2]
]

spell_result = multiplyMatrices(spell_components, magical_catalyst)
console.log("Result of the Magical Transformation:")
exploreMatrix(spell_result)
```


## Real-World Adventures: When Nested Arrays Meet Matrices 🌍

1. **Image Processing:** Use nested arrays to represent pixel data, then convert to matrices for fast computations!
2. **Game Development:** Represent game boards as nested arrays, use matrix operations for game logic.
3. **Data Analysis:** Store data in nested arrays, convert to matrices for statistical operations.
4. **Machine Learning:** Prepare data as nested arrays, transform into matrices for model training.

## The Ultimate Fusion Challenge: Nested Matrix Adventure Game! 🏆

Your mission, should you choose to accept it:

1. Create a game board as a nested array of emoji representing different terrains.
2. Implement player movement using nested array indexing.
3. Use matrix operations (like convolution) to determine valid moves or calculate scores.
4. Bonus: Add items for the player to collect, using matrix addition to update the player's inventory!

## Words of Wisdom from the Nested Array-Matrix Sage 🧙‍♂️

"Remember, young data wizard, nested arrays and matrices are two sides of the same magical coin. Nested arrays offer flexibility and intuitive representation, while matrices unlock the power of mathematical operations. Master both, and you'll be unstoppable in the realms of data and computation!"

Are you ready to wield the combined power of nested arrays and matrices? The multiverse of data structures awaits your command! 🚀🌟

- [Fundamental Coding Techniques for Matrices](/arrays_and_strings/matrix_tehniques.py)  
- [Common Problems to Enhance Understanding](/arrays_and_strings/code_challenges/intro_array_challenges.md)