//Using Functions to calculate growth rate and est population after each year
//author: dharma
//23/09/2022

#include <iostream>
using namespace std;

int growthRate (int birth, int death) //defining the function growthRate
{
    return birth-death; //return the value
}

float estimatedPopulation (int population, int birth, int death, int n) // define the function
{
    float z = population + (birth * population)/100 - (death * population)/100; // calculate formula
    return z;

}

int main()

{
    int population, birth, death,n; // declare the input values
    cout << "Enter population, birth rate, death rate and n:" << endl;
    cin >> population >> birth >> death >> n;

    if (population < 2 || birth < 0 || death < 0)
        {
            cout << "Invalid input" << endl;
        }

    else
    {
        cout << "Growth rate: " << growthRate (birth, death) << endl;
        cout << "Estimate Population: " << estimatedPopulation (population, birth, death, n) << endl;
    }

    return 0;
}
