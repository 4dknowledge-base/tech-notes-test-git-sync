# test lesson git sync

```4d
[WorkOrder]startTime:=[WorkOrder]startTime+$delay
While([WorkOrder] startTime>=?24:00:00?)
   [WorkOrder]startTime:=[WorkOrder]startTime-?24:00:00?
   [WorkOrder]startDate:=[WorkOrder]startDate+1
End while
```

cc

```4d
ORDER BY([Visit]; [Visit]arrivalDate; >; [Visit]arrivalTime; >)

QUERY([Visit]; [Visit]arrivalDate>=$monday; *) QUERY([Visit]; [Visit]arrivalTime>=?08:30:00?; *) QUERY([Visit]; [Visit]arrivalDate