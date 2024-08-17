# File Operations

# Notes on File Operation with C

| Function	|Description |
|-|-|
| `fopen()`	|opens new or existing file |
| `fprintf()`|	write data into the file  \["ফাইল" স্ট্রিম, কি স্ট্রিং ফরম্যাটে সেইভ করব, স্ট্রিম সোর্স] |
| `fscanf()`|	reads data from the file  `    while(fscanf(fp,"%d",&temp_num)!=EOF){` |
| `fputc()`	|writes a character into the file |
| `fgetc()`	|reads a character (in loop, character by character) from file  `while ((c = fgetc(fp)) != EOF) {printf("%c", c);` |
| `fputs()`	|put(WRITE) a whole string to the file |
| `fgets()`	|using while(fgets!=NULL), reads "line by line" from file with whitespace and sets to buffer string  `  while (fgets(str, 300, f) != NULL) {printf("%s", str);`; `while (fgets(line, sizeof(str_line), f)) {` |
| `fclose()`|	closes the file |
| `fseek()`	|sets the file pointer to given position |
| `fputw()`	|writes an integer to file |
| `fgetw()`	|reads an integer from file |
| `ftell()`	|returns current position |
| `rewind()`|	sets the file pointer to the beginning of the file |

## notes and tricks

* `scanf("%[^EOF]",str);` read full file at once
* `freopen("fileout.txt", "w", stdout);` directly save into the file (steam bypass)
* `fprintf()` e W+ dile full file override hoy, r+ thakle shudhu oi position er char gulo
* `fscanf()`: format `%c` ar `%s` er upor depend kore kivabe source theke ek ek kore collect korbe. jodi `%s` use kori then: ek ekta word by word catch kore, so, \_buff (steam) e ekta ekta kore word dhukse, without counting whitespace characters, so, while loop er vitore amake `printf()` er vitore ekta space ditei hosse Jemon silo temon paite hole `fscanf` er vitore `C` ar `printf` er vitore `S`.
* `int temp = 0;    while (fscanf(f_input, "%d", &temp) != EOF) {`
* `while (fscanf(ptr, "%c", &str[i]) != EOF && i < 199) { i++;}`
* `    while((ptr=strstr(str,word))!=NULL) {memmove(ptr,ptr+len,strlen(ptr+len)+1);}`
