> gcc -E calculator.c -o calculator.pp.c
Espero encontrar en el Header referencia al fuente (calculator.c)
Ha agregado referencias a las librerias básicas (stdio.h) y del sistema (..linux-gnu..)

> gcc -S calculator.c -o calculator.asm
aparecen comando de assembler
con call aparecen printf y add_numbers (e incluye las instruccion). Printf es la única de stdio invocada en el fuente.
Nota : comentando la linea 4 "int sum;" falla la generacion del assembler dando error
Nota : cambiando printf por print da un warning

> gcc -c calculator.c -o calculator.o
> nm calculator.o
aparece add_numbers y main con T (texto)
aparece printf con U (Undefined)

> gcc -v calculator.c -o calculator.e
> nm -u calculator.e 
Linkea printf con los @@: U printf@@GLIBC_2.2.5


