#include <stdio.h>
#include <string>
#define N 10
using namespace std;
struct Libro
{
    string Isbn;
    int Pagine;
    float Costo;
};
void Ordinamento(Libro Insieme);
void Ricerca(Libro Insieme);
void OrdinamentoPagDec(Libro Insieme);
void Medio(Libro Insieme);
int main()
{
    Libro Insieme[N]=
    {
        {"746784",123,13.5};
        {"123456",345,36};
        {"654321",987,67};
        {"098765",981,54};
        {"098763",133,27};
        {"435267",177,14};
        {"112233",455,34};
        {"554673",853,79};
        {"887794",333,90};
        {"102938",999,11};
    };
    Medio(Libro Insieme);
    Ordinamento(Libro Insieme);
    Ricerca(Libro Insieme);
    OrdinamentoPag(Libro Insieme);
    return 0;
}
void Medio(Libro Insieme)
{
    int i;
    float Media[MAX];
    for(i=0,i<MAX, i++)
    {
        Media[i]=(Insieme[i].Pagine/Insieme[i].Costo);
        cout<<"Il costo medio per il libro numero "<<i<<" è: "<<Media[i];
    }
}
void Ordinamento(Libro Insieme)//ordino con bubble sort l'array di struct, in questo modo soddisfo la seconda richiesta e avendo i dati ordinati posso fare una ricerca binaria
{                           //(Considero in partenza un insieme senza ripetizioni avendo inserito i dati manualmente)
    int i=-1, j, Sup;
    bool Scambio;
    do
    {
        i++;
        Scambio=false;
        for(j=N-2;j<i;j--)
        {
            if(Insieme[j].Pagine==Insieme[j+1].Pagine)
            {
                Sup=Insieme[j];
                Insieme[j]=Insieme[j+1];
                Insieme[j+1]=Sup;
                Scambio=true;
            }
        }
    }while((Scambio)&&(i!=N-2))
    for(i=0; i<3; i++)
    {
        cout<<Insieme[j].Pagine;
    }
}
void Ricerca(Libro Insieme)
{
    int i=0;
    float X;
    cout<<"Inserisci un prezzo da cercare: ";
    do
    {
        cin>>X;    
    }while(X<=0);
    while((i!N-1)&&(Insieme[i].Costo!=X))
    {
        i++;
    }
    if(Insieme[i].Costo==X)
    {
        cout<<"Elemento trovato in posizione: "<<Metà;
    }else
    {
        cout<<"Elemento non trovato"<<endl;
    }
    
}
void OrdinamentoPagDec(Libro Insieme)//Avendo già l'insieme ordinato devo invertirli
{
    int i, Sup;
    for(i=0; i<MAX; i++)
    {
        Sup=Insieme[j].Pagine;
        Insieme[j].Pagine=Insieme[MAX-j].Pagine;
        Insieme[MAX-j].Pagine=Sup
        C
    }
}
