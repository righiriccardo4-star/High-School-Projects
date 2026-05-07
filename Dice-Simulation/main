
#include <iostream>
#include <time.h>
#include <stdlib.h>
#define MAX_FACCE 20
#define MAX_DADI 5
#define MAX_LANCI 100
using namespace std;
void Numero_Facce(int &Facce);
int Dado(int Facce);
void Lancio(int Facce,int QuantitaDadi,int Lanci,int Valori[MAX_LANCI][MAX_DADI]);
void Probabilita(int Facce, int QuantitaDadi,int Lanci, int Num);
int main()
{
	int A, NumDadi, Num, NumLanci=1;
	char Scelta;
	srand(time(NULL));
	Numero_Facce(A);
	do
	{
		cout<<"Quanti dadi vuoi lanciare? ";
		cin>>NumDadi;
	} while((NumDadi<2)||(NumDadi>MAX_DADI));
	do
	{
		cout<<"Che numero vuoi che esca?";
		cin>>Num;
	} while((Num<1)||(Num>A));
	cout<<"Scegli un'opzione: "<<endl<< "a) calcola la probabilita' su un lancio di un singolo dado"<<endl<<
	    "b) calcola la probabilita'  su piùlanci di un singolo dado"<<endl<<"c) calcola la probabilita' che su un lancio di piu' dadi escano gli stessi numeri"<<endl<<
	    "d) calcola la probabilita'  che su più lanci di piu' dadi esca lo stesso numero piu' volte"<<endl;
	do
	{
		cin>>Scelta;
	} while((Scelta!='a')&&(Scelta!='b')&&(Scelta!='c')&&(Scelta!='d'));
	switch (Scelta)
	{
	case 'a':
	    NumDadi=1;
		Probabilita(A, NumDadi, NumLanci, Num);
		break;
	case 'b':
	    NumDadi=1;
	    do
	    {
	        cout<<"Quante volte vuoi lanciare il dado? ";
	        cin>>NumLanci;
	    }while((NumLanci<2)||(NumLanci>MAX_LANCI));
	    Probabilita(A, NumDadi, NumLanci, Num);
		break;
	case 'c':
    	Probabilita(A, NumDadi, NumLanci, Num);
		break;
	case 'd':
	    do
	    {
	        cout<<"Quante volte vuoi lanciare il dado? ";
	        cin>>NumLanci;
	    }while((NumLanci<2)||(NumLanci>MAX_LANCI));
	    Probabilita(A, NumDadi, NumLanci, Num);
		break;
	}
	return 0;
}
void Numero_Facce(int &Facce)
{
	do
	{
		cout<<"Quante facce ha il dado? ";
		cin>>Facce;
	} while((Facce<4)||(Facce>MAX_FACCE));
}
void Probabilita(int Facce, int QuantitaDadi,int Lanci, int Num)
{
    int Valore[MAX_LANCI][MAX_DADI], i, j, ContaCol=0, Vittorie=0, ProbAssoluta;
    float ProbRelativa;
    Lancio( Facce, QuantitaDadi, Lanci, Valore);
    for(i=0;i<Lanci;i++)
    {
        for(j=0;j<QuantitaDadi; j++)
        {
           if(Valore[i][j]==Num)
           {
               ContaCol++;
           }
        }
        if(ContaCol==QuantitaDadi)
        {
            Vittorie++;
        }
        ContaCol=0;
    }
    ProbAssoluta=Vittorie;
    ProbRelativa = (static_cast<float>(Vittorie) / Lanci) * 100;
    cout<<"La probabilita' assoluta e': "<<ProbAssoluta<<endl;
    cout<<"La probabilita' relativa e': "<<ProbRelativa<<"%"<<endl;
}
void Lancio(int Facce,int QuantitaDadi,int Lanci,int Valori[][MAX_DADI])
{
	int i, j;
	for(j=0; j<QuantitaDadi; j++)
	{
	    cout<<"Valore delle facce: ";
		for(i=0; i<Lanci; i++)
		{
			Valori[i][j]=Dado(Facce);
			cout<<Valori[i][j]<<"\t";
		}
		cout<<endl;
	}
}
int Dado(int Facce)
{
    int X;
    X=rand()%Facce+1;
    return X;
}
