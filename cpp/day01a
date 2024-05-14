#include <iostream>
#include <string>
#include <vector>
#include <fstream>

using namespace std;

vector<string> ReadFile(const string& FILEname) {
    ifstream FILE(FILEname); 
    vector<string> lines; 

    if (FILE.is_open()) { 
        string linha;
        while (getline(FILE, linha)) { 
            lines.push_back(linha); 
        }
        FILE.close(); 
    } else {
        cerr << "Erro ao abrir o arquivo." << endl; 
    }

    return lines;
}

int firstnum(string line) {
    auto it = line.begin();
    int a;

    while(it != line.end()){
        if(isdigit(*it)){
            a = *it;
            return a - '0';
        }
        it++;
    }
    return 0;
}

int lastnum(string line) {
    auto it = line.rbegin();
    int a;

    while(it != line.rend()){
        if(isdigit(*it)){
            a = *it - '0';
            return a;
        }
        it++;
    }
    return 0;
}


int main(){
    string FILEname = "/home/alfredo/AdventOfCode/2023codes/cpp/input01.txt";

    vector<string> text;    
    text = ReadFile(FILEname);

    int sum = 0;
    int a = 0, b = 0;
    for(string s: text){
        a = firstnum(s);
        b = lastnum(s);
        sum += 10*a + b;
    }

    cout << sum << "\n";

    return 0;
}
