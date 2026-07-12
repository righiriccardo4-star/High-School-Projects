#include <iostream>
#include <string>

#define N 10
using namespace std;

struct Libro {
    string Isbn;
    int Pagine;
    float Costo;
};

// Prototipi corretti (passaggio dell'array)
void OrdinamentoPagCrescente(Libro Insieme[]);
void RicercaPerCosto(Libro Insieme[]);
void OrdinamentoPagDecrescente(Libro Insieme[]);
void CalcolaCostoMedio(Libro Insieme[]);

int main() {
    // Correzione virgole e inizializzazione
    Libro Insieme[N] = {
        {"746784", 123, 13.5},
        {"123456", 345, 36.0},
        {"654321", 987, 67.0},
        {"098765", 981, 54.0},
        {"098763", 133, 27.0},
        {"435267", 177, 14.0},
        {"112233", 455, 34.0},
        {"554673", 853, 79.0},
        {"887794", 333, 90.0},
        {"102938", 999, 11.0}
    };

    cout << "--- 1. Costo Medio per Pagina ---" << endl;
    CalcolaCostoMedio(Insieme);

    cout << "\n--- 2. Primi 3 Libri (Ordine Crescente Pagine) ---" << endl;
    OrdinamentoPagCrescente(Insieme);

    cout << "\n--- 3. Ricerca per Costo ---" << endl;
    RicercaPerCosto(Insieme);

    cout << "\n--- 4. Ordinamento Decrescente Pagine ---" << endl;
    OrdinamentoPagDecrescente(Insieme);

    return 0;
}

void CalcolaCostoMedio(Libro Insieme[]) {
    for(int i = 0; i < N; i++) {
        // Costo per pagina = Costo totale / Numero pagine
        float costoPagina = Insieme[i].Costo / Insieme[i].Pagine;
        cout << "Libro ISBN " << Insieme[i].Isbn << " - Costo/Pagina: " << costoPagina << " Euro" << endl;
    }
}

void OrdinamentoPagCrescente(Libro Insieme[]) {
    int i, j;
    Libro temp;
    bool scambio;
    
    // Bubble Sort
    for (i = 0; i < N - 1; i++) {
        scambio = false;
        for (j = 0; j < N - i - 1; j++) {
            if (Insieme[j].Pagine > Insieme[j+1].Pagine) {
                temp = Insieme[j];
                Insieme[j] = Insieme[j+1];
                Insieme[j+1] = temp;
                scambio = true;
            }
        }
        if (!scambio) break;
    }

    for(i = 0; i < 3; i++) {
        cout << "ISBN: " << Insieme[i].Isbn << " | Pagine: " << Insieme[i].Pagine << endl;
    }
}

void RicercaPerCosto(Libro Insieme[]) {
    float x;
    bool trovato = false;
    cout << "Inserisci il prezzo esatto da cercare: ";
    cin >> x;

    for(int i = 0; i < N; i++) {
        if(Insieme[i].Costo == x) {
            cout << "Libro trovato! ISBN: " << Insieme[i].Isbn << " in posizione " << i << endl;
            trovato = true;
        }
    }
    if(!trovato) cout << "Nessun libro trovato con questo costo." << endl;
}

void OrdinamentoPagDecrescente(Libro Insieme[]) {
    int i;
    Libro temp;
    // Inversione semplice dell'array (già ordinato crescente)
    for(i = 0; i < N / 2; i++) {
        temp = Insieme[i];
        Insieme[i] = Insieme[N - 1 - i];
        Insieme[N - 1 - i] = temp;
    }
    
    cout << "Database riordinato decrescente (primi 2 risultati):" << endl;
    for(i = 0; i < 2; i++) {
        cout << "ISBN: " << Insieme[i].Isbn << " | Pagine: " << Insieme[i].Pagine << endl;
    }
}
