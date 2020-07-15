compilador: lex.yy.c parser.tab.o clean
	gcc parser.tab.o -o compilador -ly -ll -lm
#	gcc parser.tab.o lex.yy.o -o compilador -ly -ll -lm
lex.yy.c: parser.l
	flex parser.l
parser.tab.c: parser.y
	bison -d parser.y
parser.tab.o: parser.tab.c
	gcc -c -g  parser.tab.c 
#lex.yy.o: lex.yy.c parser.tab.c
#	gcc -ll -c -g lex.yy.c  parser.tab.c
clean:
	rm lex.yy.c
	rm parser.tab.c
	rm parser.tab.h
	#rm parser.tab.o
	#rm lex.yy.o
	clear 


