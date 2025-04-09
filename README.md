#include <iostream>
using namespace std;

int main() {
    string palavra = "computador";
    string escondida(palavra.length(), '_');
    int erros = 0;

    while (erros < 6 && escondida != palavra) {
        cout << "Palavra: " << escondida << endl;
        cout << "Letra: ";
        char letra;
        cin >> letra;

        bool certo = false;
        for (int i = 0; i < palavra.size(); i++) {
            if (palavra[i] == letra) {
                escondida[i] = letra;
                certo = true;
            }
        }

        if (!certo) {
            erros++;
            cout << "Errado! Tentativas restantes: " << 6 - erros << endl;
        }
    }

    if (escondida == palavra)
        cout << "Parabéns! A palavra era: " << palavra << endl;
    else
        cout << "Perdeste! A palavra era: " << palavra << endl;

    return 0;
}
