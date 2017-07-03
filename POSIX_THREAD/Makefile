
#  make measure  -- build measure.c for the target
#  make          -- build the simulation version of thermostat.c
#  make TARGET=1 -- build the target version of thermostat.c
#  make devices	 -- build the simulated devices program

#  Note that the only target whose build changes with the TARGET symbol
#  is thermostat.o.  Everything else builds in the appropriate environment


all:alarm
#which compiler
CC =gcc

#optionals for development
CFLAGS = -Wall -g

alarm.o: alarm.c 
	$(CC) $(CFLAGS) -c alarm.c

alarm: alarm.o errors.h
	$(CC) -o $@ $^

alarm_fork.o: alarm_fork.c
	$(CC) $(CFLAGS) -c alarm_fork.c
	
alarm_fork: alarm_fork.o errors.h
	$(CC) -o $@ $^
	
alarm_thread.o: alarm_thread.c
	$(CC) $(CFLAGS) -c alarm_thread.c
	
alarm_thread: alarm_thread.o errors.h
	$(CC) -o $@ $^  -lpthread  #Using the -lpthread option  causes the pthread library to be linked 
	
mutex_static.o: mutex_static.c
	$(CC) $(CFLAGS) -c mutex_static.c
	
mutex_static: mutex_static.o errors.h
	$(CC) -o $@ $^
	
	
alarm_mutex.o: alarm_mutex.c
	$(CC) $(CFLAGS) -c alarm_mutex.c
	
alarm_mutex: alarm_mutex.o errors.h
	$(CC) -o $@ $^  -lpthread  #Using the -lpthread option  causes the pthread library to be linked 
	