#include <iostream>
#include <vector>

using namespace std;

int main(){

    vector<int> vet{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

    cout << "Primeiro gurreiro a receber espada" << endl;
    int init{};
    cin >> init;

    while(true) {
        if(vet.size() == 1) {
            cout << "vencedor " << vet[0] << endl; 
            break;
        }

        init++;
        if((unsigned)init == vet.size()) {
            init = 0;
        }

        for(int i = 0; (unsigned)i < vet.size(); i++) {
            cout << vet[i] << " ";
        }

        vet.erase(vet.begin() + init);

        if((unsigned)init == vet.size()) {
            init = 0;
        }
        cout << endl;
    }
} 