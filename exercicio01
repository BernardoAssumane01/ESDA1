#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <string.h>

//DEFINICAO DE VARIAVEL PARA O NUMERO MAXIMO DE JOGADORES
#define NRJOG_MAX 10
		
//DEFINICAO DA ESTRUTURA DOS JOGADORES 
		typedef struct{
		    int cod_jog;
		    int Nrgolos;
		    int NrJogadores;
		    int ativo;
		    char nome_jogador[50];
		    char apelido[50];
		    char In_Contrato[15];
		    char Fim_Contrato[15];
		    
		}JOGADOR;
		
//DEFINICAO DA ESTRUTURA DAS ESQUIPAS
		typedef struct{
			int codEquipa;
		    char nome[50];
		   	JOGADOR t[15];
			    
		}EQUIPA;
		
//DEFINICAO DO MENU INICIAL DO PROGRAMA
		void menu(){
		    
			int esc;
		    
			system("cls");
		    
			do{
		    	printf("Escolha: \n");
		        printf("\n1 - Registar Equipa");
				printf("\n2 - Registar Jogador");
				printf("\n3 - Eliminar Jogador");
				printf("\n4 - Verificar Resultado");
				printf("\n5 - Sair\n");
		        scanf("%d", &esc);
		        
				switch(esc){
			        case 1:
			            RegistarEquipa();
			            break;
			        
			        case 2:
			            RegistarJogador();
			            break;
			        
			        case 3:
			        	//Por terminar;
			        	break;
			        
			        case 4:
			        	VerificarResultado();
			        	break;
			        
			        case 5:
			        	exit(0);
			        	break;
			        
		   	 	    default:
			            printf("ESCOLHA INVALIDA!");
			            break;
			            }
			            
		    	}while(esc != 0);
		}
		
//INICIO DA FUNCAO QUE PERMITIRA FAZER O REGISTO DOS JOGADORES
		void RegistarJogador(JOGADOR dados){
		    	
				char nomeJogador[50];
		    	char apelido[50];
				int esc, k;
		    	
				system("cls");
				
				do{
					
				system("cls");
				
				printf("Digite o numero do jogador:\n");
					
				for(k=0; k<2; k++){
					scanf("%d",&dados.NrJogadores);	 		 
					printf("Digite o codigo do jogador: \n");
					scanf("%d",&dados.cod_jog);
					printf("Nome do jogador:\n");
					scanf("%s",&nomeJogador);
					setbuf(stdin,NULL);
					printf("Apelido:\n");
					scanf("%s",&apelido);
					setbuf(stdin,NULL);
				 	printf("Digite a data de inicio do contrato:\n");
					scanf("%s",&dados.In_Contrato);
					printf("Digite a data do fim do contrato:\n"); 
					scanf("%s",&dados.Fim_Contrato);
					printf("Digite o numero de golos:\n");
					scanf("%d",&dados.Nrgolos);
					
				}
				
				printf("1 - Continuar\n0 - Sair\n");
				scanf("%d",&esc);
				
				}while(esc != 0);
		}
//FIM DA FUNCAO 
		
//DEFINICAO DA FUNCAO PARA FAZER O REGISTO DAS EQUIPAS
		void RegistarEquipa(EQUIPA dados1){
			    
				int esc;
			    
			    system("cls");
			    
				do{
				     printf("Digite o nome da equipa:\n");
				     scanf("%s",&dados1.nome);
				     setbuf(stdin,NULL);
				     printf("Digite o codigo da equipa:\n");
				     scanf("%d",&dados1.codEquipa);
				     printf("1 - Continuar \n0 -  Sair e ir ao menu inicial\n");
				     scanf("%d",&esc);
				     
			    }while(esc != 0);
			    FILE *file = fopen("texto.txt","a");
			    if(file != NULL){
					   	fprintf(file,"%d %s\n",dados1.codEquipa,dados1.nome);
						printf("Registo Feito.");
				}
				fclose(file);
		}
//FIM DA FUNCAO
		
		
//DEFINICAO DA FUNCAO DE VERIFICACAO DOS RESULTADOS 
		void VerificarResultado(){
				
				char var;
			   	EQUIPA equipa2;
			    FILE *ficheiro;
				ficheiro=fopen("texto.txt","r");
		
				printf("Nome: \n");
			    var = fscanf(ficheiro,"%d %s\n",&equipa2.codEquipa,equipa2.nome); 
				while(var != EOF){
						printf("%d %s\n",equipa2.codEquipa,equipa2.nome);
						var = fscanf(ficheiro,"%d %s\n",&equipa2.codEquipa,equipa2.nome); 
				}		
				fclose(ficheiro);
		}
//FIM DA FUNCAO
		
//INICIO DA FUNCAO PRINCIPAL
		int main(){
			
		     menu();
		
		    return 0;
		}
//FIM DA FUNCAO PRINCIPAL E DO PROGRAMA
