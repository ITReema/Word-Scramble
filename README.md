# Word-Scramble
Very simple scramble game, Involves guessing as many words as possible from a given string.

## Challenge
1. Disallow answers that are shorter than three letters or are just our start word. For the three-letter check, the easiest thing to do is put a check into isReal() that returns false if the word length is under three letters. For the second part, just compare the start word against their input word and return false if they are the same ✅


```
guard answer.count >= 3 else {
   return showErrorMessage(errorTitle: "Word is too short", errorMessage: "Add a word that contains 3 or more characters!")
  }
```

```
guard word != title else {return false}
```

2. Refactor all the else statements we just added so that they call a new method called showErrorMessage(). This should accept an error message and a title, and do all the UIAlertController work from there ✅

```
func showErrorMessage(errorTitle: String, errorMessage: String) {
        let ac = UIAlertController(title: errorTitle, message: errorMessage, preferredStyle: .alert)
        ac.addAction(UIAlertAction(title: "OK", style: .default))
        present(ac, animated: true)
    }
```

3. Add a left bar button item that calls startGame(), so users can restart with a new word whenever they want to ✅
```
navigationItem.leftBarButtonItem = UIBarButtonItem(title: "New Game", style: .plain, target: self, action: #selector(startGame))
```

<p align="center">
  <img width="250" height="500" src="https://user-images.githubusercontent.com/27751735/56820039-a1f0d500-6853-11e9-8a77-b0e4ea270a17.png">
</p>
<p align="center">
  <img width="250" height="500" src="https://user-images.githubusercontent.com/27751735/56820045-a4ebc580-6853-11e9-81c5-8465259ca531.png">
</p>
<p align="center">
  <img width="250" height="500" src="https://user-images.githubusercontent.com/27751735/56820046-a4ebc580-6853-11e9-93a6-a7e719ecc644.png">
</p>
<p align="center">
  <img width="250" height="500" src="https://user-images.githubusercontent.com/27751735/56820047-a4ebc580-6853-11e9-8ac9-f330b799ffb0.png">
</p>
<p align="center">
  <img width="250" height="500" src="https://user-images.githubusercontent.com/27751735/56820051-a61cf280-6853-11e9-9797-5cc107fcc302.png">
</p>

