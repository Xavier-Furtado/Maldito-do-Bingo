#include <iostream>

using namespace std;

int main() {
    string s1 = "";  // Uma string vazia
    string s2 = "Olá, mundo!";  // Uma string com conteúdo
    
    if (s1.empty()) {  // Verifica se s1 está vazia
        cout << "s1 está vazia!" << endl;
    }
    
    if (!s2.empty()) {  // Verifica se s2 NÃO está vazia
        cout << "s2 contém: " << s2 << endl;
    }

    return 0;
}
