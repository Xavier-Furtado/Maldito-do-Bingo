#include <iostream>
using namespace std;

int main() {
    string palavra;
    cout << "Digite a palavra secreta: ";
    cin >> palavra;
  
    string escondida(palavra.size(), '_'); 
    int erros = 0;

    while (erros < 6 && escondida != palavra) {
        cout << "Palavra: " << escondida << "\nLetra: ";
        char letra;
        cin >> letra;

        bool acertou = false;
        for (int i = 0; i < palavra.size(); i++) {
            if (palavra[i] == letra) {
                escondida[i] = letra;
                acertou = true;
            }
        }

        if (!acertou) erros++;
    }

    cout << (escondida == palavra ? "Parabéns! " : "Perdeste! ") << "A palavra era: " << palavra << endl;
}
