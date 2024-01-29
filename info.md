<!-- Задача 1: Задайте двумерный массив символов (тип char [,]). Создать строку из символов этого массива. -->

int main()
{
  
 char *STR[10];
 char **s;
 char buf[80];
 int n = 0;
  int max_number_of_strings = 10;  
  for (s = STR; n < max_number_of_strings  &&*gets(buf) != '\0'; n++, s++) {
  *s = (char*)malloc(strlen(buf) + 1);
  strcpy(*s, buf);
 }
 printf("---------------------\n");
  for (s = STR; s < STR + n; s++)
  puts(*s);

  return 0;
}

Задача 2: Задайте строку, содержащую латинские буквы в обоих регистрах. Сформируйте строку, в которой все заглавные буквы заменены на строчные.

void task(char word[100])
{
    for (int i = 0;i < strlen(word);++i)
    {
        if ('A' <= word[i] && word[i] <= 'Z')
            word[i] = word[i] - 'A' + 'a';
        else if ('a' <= word[i] && word[i] <= 'z')
        {
            word[i] = word[i] - 'a' + 'A';
        }
    }
}

void main()
{
    char word[100];
    cin >> word;
    task(word);
    cout << word;
}
