# CP1WhiteProject

int main()
     {
     int quizCounters,r,r1,countingQuiz,i,n;
     float countingScores;
     char options;
     char playername[20];
     mainhome:
     system("cls");
 
     printf("\n\t\t****************************************");
 
     printf("\n\t\t\t   WELCOME TO QUIZ GAME");
 
     printf("\n\t\t****************************************");
     printf("\n\t\t****************************************");
     printf("\n\t\t   CARLOS HILADO MEMORIAL STATE COLLEGE") ;
     printf("\n\t\t****************************************");
     printf("\n\t\t****************************************");
     printf("\n\t\t Enter 1 to start the game");
     printf("\n\t\t Enter 2 to view the highest score  ");
     printf("\n\t\t Enter 3 to reset score");
     printf("\n\t\t Enter 4 for help            ");
     printf("\n\t\t Enter 5 to quit             ");
     printf("\n\t\t****************************************\n\n");
     options=toupper(getch());
     if (options=='2')
{
show_record();
goto mainhome;
}
     else if (options=='3')
{
help();getch();
goto mainhome;
}
else if (options=='4')
{reset_score();
getch();
goto mainhome;}
else if (options=='5')
exit(1);
    else if(options=='1')
    {
     system("cls");

Record Window

void show_record()
    {system("cls");
char name[20];
float scr;
FILE *f;
f=fopen("score.txt","r");
fscanf(f,"%s%f",&name,&scr);
printf("\n\n\t\t*************************************************************");
printf("\n\n\t\t %s has secured the Highest Score %0.2f",name,scr);
printf("\n\n\t\t*************************************************************");
fclose(f);
getch();}

Reset score window

void reset_score()
    {system("cls");
    float sc;
char nm[20];
FILE *f;
f=fopen("score.txt","r+");
fscanf(f,"%s%f",&nm,&sc);
sc=0;
fprintf(f,"%s,%.2f",nm,sc);
    fclose(f);}
