# Projet NSI Sudoku

*le but du jeu est de compléter la grille de sudoku.
*Dans un premier faire de moi même un sudoku 4x4 puis 9x9 afin de bien comprendre comment je dois rédiger le code pour que ,le jeu fonctioone que ce soit creer la grille ou faire les modification des cases vides et finalment définir les conditions de victoires.

Structure de données:
Plateau = tableau

Valeurs utilisées: 0; 1; 2; 3; 4; 5; 6; 7; 8; 9.

case vide : 0 



Fonctions:
affiche
est_valide

règles :

sur une même colonne et sur une même il ne peut il y avoir qu'une fois le même chiffre entre 1 et 9 

mon code actuel:

def affiche(sudoku):
    print("  12 34")
    num_ligne = 0
    for ligne in sudoku:
        if num_ligne %2 == 0:
            print("  ",end="")
            print("-"*6)
        num_ligne +=1
        num_el = 0
        print(chr(64+num_ligne) , end="")
        for element in ligne:
            if num_el % 2 == 0:
                print('|', end="")
            print (element, end="")
            num_el += 1
        print ("|")
    print("  ",end="")
    print("-"*6)
    


sudoku = [[2,0,0,1],
          [0,0,2,3],
          [0,2,3,4],
          [3,0,1,0]]

jeu_continue = True
while jeu_continue:
    affiche(sudoku)
    ...
    jeu_continue = est_termine(soduku)
