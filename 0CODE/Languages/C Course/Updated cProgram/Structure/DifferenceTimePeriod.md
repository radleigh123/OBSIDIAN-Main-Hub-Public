```C
// Program to calculate difference between two time periods
#include<stdio.h>
struct Time{
    int seconds, minutes, hours;
};

void differenceTimePeriod(struct Time t1, 
                          struct Time t2,
                          struct Time *diff);

int main(){
    struct Time startTime, stopTime, diff;

    printf("Enter the start time.\n");
    printf("Enter hours, minutes, and seconds: ");
    scanf("%d %d %d", &startTime.hours,
                      &startTime.minutes,
                      &startTime.seconds);
    
    printf("Enter the stop time.\n");
    printf("Enter hours, minutes, and seconds: ");
    scanf("%d %d %d", &stopTime.hours,
                      &stopTime.minutes,
                      &stopTime.seconds);

    // difference between start and stop Time
    differenceTimePeriod(startTime, stopTime, &diff);
    printf("\nTime Difference: %d:%d:%d - ", startTime.hours,
                                             startTime.minutes,
                                             startTime.seconds);
    printf("%d:%d:%d ", stopTime.hours,
                        stopTime.minutes,
                        stopTime.seconds);
    printf("= %d:%d:%d\n", diff.hours,
                           diff.minutes,
                           diff.seconds);

    return 0;
}

// Computes difference between time periods
void differenceTimePeriod(struct Time start, 
                          struct Time stop, 
                          struct Time *diff){
    while (stop.seconds > start.seconds){
        --start.minutes;
        start.seconds += 60;
    }
    diff->seconds = start.seconds - stop.seconds;
    while (stop.minutes > start.minutes){
        --start.hours;
        start.minutes += 60;
    }
    diff->minutes = start.minutes - stop.minutes;
    diff->hours = start.hours - stop.hours;
}
```