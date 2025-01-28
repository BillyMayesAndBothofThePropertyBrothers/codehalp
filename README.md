#include <cs50.h>
#include <stdio.h>
#include <math.h>

float calculate_quarters(float cents);

float calculate_dimes(float cents);

float calculate_nickels(float cents);

float calculate_pennies(float pennies);

int main(void)
{
    float cents;
    do
    {
        cents = get_float("Change owed: ");
    }
    while (cents > 0 || cents <= 99);

    float quarters = calculate_quarters(cents);

    float dimes = calculate_dimes(cents);

    float nickels = calculate_nickels(cents);

    float pennies = calculate_pennies(cents);

    float coins = quarters + dimes + nickels + pennies;
}













float calculate_quarters(float cents)
{
    float quarters = floor(cents / 25);

    cents -= quarters * 25;

    return quarters;
}

float calculate_dimes(float cents)
{
    float dimes = floor(cents / 10);

    cents -=dimes * 10;

    return dimes;
}

float calculate_nickels(float cents)
{
    float nickels = floor(cents / 5);

    cents -=nickels * 5;

    return nickels;
}

float calculate_pennies(float cents)
{
    float pennies = floor(cents / 1);

    cents -=pennies * 1;

    return pennies;
}
