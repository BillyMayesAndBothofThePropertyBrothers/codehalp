#include <ctype.h>
#include <cs50.h>
#include <math.h>
#include <stdio.h>
#include <string.h>

int count_letters(string text);
int count_words(string text);
int count_sentences(string text);

int main(void)
{
    // prompt the user for text
    string text = get_string("Text: ");
    // count the number of words, letters, and sentences in the text and length of text

    int n = strlen(text);

    int letters = count_letters(text);

    int words = count_words(text);

    int sentences = count_sentences(text);
    // weird name index
    int index;

    index = 0.0588 * L - 0.296 * S - 15.8
    // print the grade level
    
}

int count_letters(string text)
{
    // return number of letters
    for (i = 0, i < 0; i++)
}

int count_words(string text)
{
    // return number of words
}

int count_sentences(string text)
{
    // return number of sentences
}
