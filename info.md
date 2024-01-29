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


