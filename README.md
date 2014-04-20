TrabalhoPS
==========

Trabalho de PS

struct dados{
  char palavra[10];
  char dif;
  char dic1[10], dic2[10], dic3[10]
}
typedef dados* Dados; 

// 15 palavras - facil
// 11 palavras - medio
// 9 palavras - dificil

// criando banco de dados

void Cria banco de dados(FILE *fp){
  // Ainda estou pensando como vai ser toda a função
    Dados *p;
    char pal[10], difi, dica1[10], dica2[10], dica3[10], c;
    int i=0, k=0, j=0, m=0, n=0;
    
    while(!foef(fp)){
      while(c != '\n'){
        fscanf(fp, "%c", &c); // Le a palavra do arquivo
        if(c == ' '){ // Vai sempre usar como referencia o caractere ' '
          k++;
          fscanf(fp, "%c", &c);// Nesse caso pulamos o ' ' porque ele nao sera armazenado
        }
        switch(k){
			case 0:// enquanto nao achar, vai adicionar a string palavra.
				dados.palavra[i] = c;
          		i++;
				break;
			case 1:// apos o 1 espaco temos a dificuldade do jogo
				dados.dif = c;
				break;
			case 2:// apos o 2 espaco temos a 1 dica do jogo
				dados.dic1[j] = c;
          		j++;
          		break;
          	case 3:// apos o 3 espaco temos a 2 dica do jogo
				dados.dic2[m] = c;
          		m++;
          		break;
          	case 4:// apos o 4 espaco temos a 3 dica do jogo
				dados.dic3[n] =c;
          		n++; // entao termina a linha
          		break;
          	default:
				printf("Ocorreu algum erro.\n");
				break;
        }
      }
    }
}
