```Python
import sys

  

class Translator:

def __init__(self) -> None:

self.charMap = {

'a': 'O.....', 'b': 'O.O...', 'c': 'OO....', 'd': 'OO.O..', 'e': 'O..O..',

'f': 'OOO...', 'g': 'OOOO..', 'h': 'O.OO..', 'i': '.OO...', 'j': '.OOO..',

'k': 'O...O.', 'l': 'O.O.O.', 'm': 'OO..O.', 'n': 'OO.OO.', 'o': 'O..OO.',

'p': 'OOO.O.', 'q': 'OOOOO.', 'r': 'O.OOO.', 's': '.OO.O.', 't': '.OOOO.',

'u': 'O...OO', 'v': 'O.O.OO', 'w': '.OOO.O', 'x': 'OO..OO', 'y': 'OO.OOO',

'z': 'O..OOO', ' ': '......', 'capital': '.....O', 'number': '.O.OOO'}

self.digitMap = {

'1': 'O.....', '2': 'O.O...', '3': 'OO....', '4': 'OO.O..', '5': 'O..O..',

'6': 'OOO...', '7': 'OOOO..', '8': 'O.OO..', '9': '.OO...', '0': '.OOO..'}

  
  

self.brailleMap = {v: k for k, v in self.charMap.items()}

self.brailleDigitMap = {v: k for k, v in self.digitMap.items()}

self.brailleSet = {'.', 'O'} # Efficient O(1) look-up

self.isBraille = False

self.numberFollows = False

self.isCapital = False

  

def findBraille(self, stream: str) -> bool:

return all(char in self.brailleSet for char in stream)

def convert(self, stream: str) -> str:

self.isBraille = self.findBraille(stream)

outStream = ""

  

if self.isBraille:

ind = 0

while ind <= len(stream) - 1:

braille = stream[ind: ind+6]

outStream += self.brailleToChar(braille)

ind += 6

else:

for char in stream:

outStream += self.charToBraille(char)

  

return outStream

  

def charToBraille(self, char: str) -> str:

outChar = ""

  

if char.lower() not in self.charMap and char not in self.digitMap:

raise Exception(f"Unsupported character in input stream: {char}")

if char.isdigit() and not self.numberFollows:

outChar += self.charMap['number']

outChar += self.digitMap[char]

self.numberFollows = True

elif char.isdigit() and self.numberFollows:

outChar += self.digitMap[char]

elif not char.isdigit() and self.numberFollows:

self.numberFollows = False

elif char.isupper():

outChar += self.charMap['capital']

outChar += self.charMap[char.lower()]

else:

outChar += self.charMap[char]

return outChar

  

def brailleToChar(self, braille: str) -> str:

outChar = ""

  

if braille not in self.brailleMap:

raise Exception(f"Unsupported braille sequence in input stream: {braille}")

if self.brailleMap[braille] == 'capital':

self.isCapital = True

elif self.brailleMap[braille] == 'number':

self.numberFollows = True

elif self.isCapital:

outChar += self.brailleMap[braille].upper()

self.isCapital = False

elif self.numberFollows and self.brailleMap[braille] == " ":

outChar += self.brailleMap[braille]

self.numberFollows = False

elif self.numberFollows:

outChar += self.brailleDigitMap[braille]

else:

outChar += self.brailleMap[braille]

  

return outChar

  

def main():

argStream = " ".join(sys.argv[1:])

translator = Translator()

outStream = translator.convert(argStream)

print(outStream)

  

if __name__ == "__main__":

main()
```