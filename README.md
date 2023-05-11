# CTkMaskedEntry

A masked entry for custom tkinter.

## Installation

Download Raw files and import all for you code.

## Usage

```python
from customtkinter import CTk
from CTkMaskedEntry import CTkMaskedEntry, Mask

root = CTk()
mask = Mask('fixed', '+99 (99) 999-999-999')
c = CTkMaskedEntry(root, mask=mask)
c.insert(0, '6611122266647')
c.pack()
mask = Mask('fixed', '99/99/9999')
c = CTkMaskedEntry(root, mask=mask)
c.insert(0, '29091991')
c.pack()
CTkMaskedEntry(root, mask=Mask('numeric')).pack()
text_variable = tkinter.StringVar()
c = CTkMaskedEntry(root, textvariable=text_variable,
                   mask=Mask('numeric', decimal_separator=",", thousand_separator='.', symbol="R$"))
text_variable.set('12659.96')
c.pack()

# Cleaning text
c = CTkMaskedEntry(root, mask=Mask('numeric', decimal_separator=",", thousand_separator='.', symbol="R$"))
c.insert(0, '12659.96')
c.pack()
c.clean()

root.mainloop()
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## How it looks?

![Screenshot](https://github.com/RickWalkerOne/CTkMaskedEntry/blob/main/Capturar.jpg?raw=true)

## License

[MIT](https://opensource.org/license/mit/)

## Acknowledgements

Thank you to [Max Morais](https://gist.github.com/MaxMorais/5388218), my code is based in his implementation in Tkinter.
