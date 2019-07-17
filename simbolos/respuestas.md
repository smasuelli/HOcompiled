> gcc -c visibility.c -o visibility.o
Da un warning porque abs no esta declarada explicitamente
> nm visibility.o
t add_abs (en area de texto)
T main (en area de texto)
U printf (undefined)
r val1 static const int => read only data section
R val2 const int => read only data section
d val3 static int => initialized data section
D val4 int => initialized data section

> Make executable
hace el .e 
como sabe que lo toma a visibility.o??? Porque hay un *.c en SOURCE de Makefile
