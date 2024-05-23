#include <stdio.h>
#include <stdlib.h>

#define RIGHE 7
#define COL 6

// prototipi
int colonna(int mat[RIGHE][COL]);

int main(void) {
  int i, j, M[RIGHE][COL];
  int c;
  for (i = 0; i < RIGHE; i++)
    for (j = 0; j < COL; j++)
      scanf("%d", &M[i][j]);

  c = colonna(M);
  printf("%d", c);

  return 0;
}

/* la funzione restituisce l'indice della prima colonna con il maggior numero di
 * 1 consecutivi, -1 se non esiste */

int colonna(int mat[RIGHE][COL]) {
  int i, j, flag = 0;
  int numUniPrec = 0, numUni = 0, colMax = 0;

  for (i = 0; i < RIGHE; i++) {
    for (j = 0; j < COL; j++) {
      if (mat[i][j] == 1) {
        numUni++;
        flag = 1;
      }
    }
    numUniPrec = numUni;
    numUni = 0;

    if (numUni >= numUniPrec) {
      colMax = j;
    }
  }

  if (flag == 0) {
    return -1;
  }

  return colMax;
}
