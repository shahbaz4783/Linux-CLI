## Exercise 1
Count the number of Pokemon files in the PokeDex/ folder.

```bash
ls ./PokeDex | wc -w
```

## Exercise 2
Create a new single file called all-pokemon.txt in the PokemonExercise folder (NOT the PokeDex folder)that contains the LOWERCASED name of every single Pokemon file in the directory, sorted in numerical order! 

```bash
ls ./PokeDex | tr A-Z a-z | sort -n > ./all-pokemon.txt
```

## Exercise 3
 Print out the three pigeon-related Pokemon: pidgey, pidgeotto, and pidgeot.  Using the command-line, print out lines 16-18.

 ```bash
 cat all-pokemon.txt | head -18 | tail -3
 ```

 ## Exercise 4
 Next, up let's isolate the original 151 Pokemon.  Using a single pipeline...
    - output the first 151 lines of the `all-pokemon.txt` file
    - remove all digits 0-9 from the lines (using `tr` )
    - sort the now number-less lines alphabetically
    - store the new result in a file called `original-151.txt` in `PokemonExercise`

```bash
cat all-pokemon.txt | head -151 | tr -d 0-9 | sort > original-151.txt
```