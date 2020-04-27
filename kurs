#include <locale>
#include <iostream>
#include <fstream>
#include "reys.h"
#include<iterator>
#include <vector>

using namespace std;



void mainMenu() {
    {
        
        string InputReysDetails = { "InputReysDetails.txt" };
        string OutputReysDetails = { "OutputReysDetails.txt" };
        int MainMenuButton;
        
        do {
            cout
                << "(0) - Выйти из программы.\n"
                << "(1) - Ввести данные о конкретном рейсе.\n"
                << "(2) - Редактировать данные о кокретном рейсе.\n"
                << "(3) - Удалить данные о конкретном рейсе.\n"
                << "(4) - Вывести данные о всех доступных рейсах.\n"
                << "(5) - Информационное табло со списком всех рейсов.\n"
                << "(6) - Показать информацию об общем количестве зарезериврованных мест и общей суммы проданных билетов"
                << endl;
            readMenuItem<int>(MainMenuButton);

            if (MainMenuButton == 1) {
                ofstream fout;

                fout.open(InputReysDetails, ofstream::app);
                if (!fout.is_open()) {
                    cout << "Ошибка открытия файла для записи" << endl;
                }
                else {
                    static int count = 1;
                    cout << "Введите данные о рейсе 1)Номер  2)Количество свободных мест 3)Время оправления 4)Пункт назначения" << endl;
                    Reys reys1;
                    reys1.SetReysID();
                    reys1.SetNumberAviableSeats();
                    reys1.SetReysTime();
                    reys1.SetReysPlaceToGo();
                    fout << "Рейс № " << count << ":" << endl;
                    fout << "Номер рейса:" << reys1.GetReysID() << endl;
                    fout << "Количество свободных мест:" << reys1.GetNumberAvaibleSeats() << endl;
                    fout << "Время отправки рейса:" << reys1.GetReysTime() << endl;
                    fout << "Пункт назначения:" << reys1.GetReysPlaceToGo() << endl;
                    fout << " " << endl;
                    count++;
                }
                fout.close();
            }
            if (MainMenuButton == 2) {
                int button1;
                int ItemToBeDeleted=0;
                ifstream fin;
                fin.open(InputReysDetails, ofstream::app);
                if (!fin.is_open()) {
                    cout << "Ошибка открытия файла для записи" << endl;
                }
                else {
                    string str;
                    string empt="  ";
                    vector <string>reys (120);
                    while (getline(fin, str)) {
                       
                        for (int i = 0; i < 100; i++) {
                            reys[i] = str;
                            cout << reys[i] << endl;

                        }
                    }
                    cout << "Введите номер рейса,данные которого вы хотите отредактировать" << endl;
                    readMenuItem<int>(button1);
                    
                }
                
             
            }
            if (MainMenuButton == 3) {
                int IDNumberDel;
                cout << "Введите номер рейса,который хотите удалить." << endl;
                readMenuItem<int>(IDNumberDel);

            }
            if (MainMenuButton == 4) {
                int IDNumberPrinted;
                cout << "Введите номер рейса,данные которого нужно вывести." << endl;
                readMenuItem<int>(IDNumberPrinted);
            }
            if (MainMenuButton == 5) {

            }
            if (MainMenuButton == 6) {

            }
            else {
                cout << "Введите номер пункта,который нужно выполнить." << endl;
            }

        } while (MainMenuButton != 0);
    }
}

int main()
{
    setlocale(LC_ALL, "Rus");
    
    mainMenu();

    
    
    
   
}
