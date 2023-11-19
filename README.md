# Number-guessing-Game

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main(){
    int number , guess , attempts = 0;
    int maxAttempts = 10;
    int score = 10;

    srand ((time));
    number = rand()%100 + 1;

    printf("\nWelcome to guess the number! \n");
    printf("\nI have chosen a number between 1 and 100.\n");

    while(attempts<maxAttempts){
        printf("\nAttempts remaining: %d\n",maxAttempts-attempts);
        printf("\nEnter your guess : ");
        scanf("%d",&guess);
        attempts++;

        if(guess>number){
            printf("Too high! \n");
        }
        else if(guess<number){
            printf("Too low! \n");
        }
        else{
            printf("\nCongratulations! You guessed the number in %d attempts.\n",attempts);
            printf("\nYour score : %d out of 10 \n",score);

            return 0;
    }
    score --;
    }

    printf("\nOut of attempts! The number was %d\n",number);
    printf("\nYour score : 0 out of 10\n");

    return 0;
 }
