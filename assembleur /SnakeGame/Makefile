all: liste_Mouvement.o liste_Section.o Serpent.o Grille.o Fonction_Jeu_1_Serpent.o main.o
	gcc liste_Mouvement.o liste_Section.o Serpent.o Grille.o Fonction_Jeu_1_Serpent.o main.o -o snake_game -lncurses 

liste_Section.o: liste_Section.c liste_Section.h
	gcc -c -Wall -pedantic -std=c99 liste_Section.c

liste_Mouvement.o: liste_Mouvement.c liste_Mouvement.h
	gcc -c -Wall -pedantic -std=c99 liste_Mouvement.c

Serpent.o: Serpent.c Serpent.h liste_Section.h liste_Mouvement.h
	gcc -c -Wall -pedantic -std=c99 Serpent.c

Grille.o: Grille.c Grille.h Serpent.h liste_Section.h liste_Mouvement.h
	gcc -c -Wall -pedantic -std=c99 Grille.c

Fonction_Jeu_1_Serpent.o: Fonction_Jeu_1_Serpent.c Fonction_Jeu.h Grille.h Serpent.h liste_Section.h liste_Mouvement.h
	gcc -c -Wall -pedantic -std=c99 Fonction_Jeu_1_Serpent.c

main.o: main.c Fonction_Jeu.h Grille.h Serpent.h liste_Section.h liste_Mouvement.h
	gcc -c -Wall -pedantic -std=c99 main.c

clean:
	rm *.o snake_game
