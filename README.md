#include <stdio.h>
#include <cs50.h>

int calculate_quarters(int cents);

int calculate_dimes(int cents);

int calculate_nickels(int cents);

int calculate_pennies(int cents);

int main(void)
{
    int cents;
    do
    {
        cents = get_int("Change owed: ");
    }
    while (cents < 0);

    int quarters = calculate_quarters(cents);

    cents = cents - (quarters * 25);
    
}







int calculate_quarters(int cents)
{
    // calculate how many quarters to give
    int quarters = 0;
    while (cents >= 25)
    {
        quarters++;
        cents = cents - 25;
    }
    return quarters;
}

int calculate_dimes(int cents)
{
    int dimes = 0;
    while (cents >= 10)
    {
        dimes++;
        dimes = dimes - 10;
    }
    return dimes;
}

int calculate_nickels(int cents)
{
    int nickels = 0;
    while (cents >= 5)
    {
        nickels++;
        nickels = nickels - 5;
    }
    return nickels;
}

int calculate_pennies(int cents)
{
    int pennies = 0;
    while (cents >= 1)
    {
        pennies++;
        pennies = pennies - 1;
    }
    return pennies;
}
