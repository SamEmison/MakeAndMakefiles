#**
#* @file Makefile
#* @author Sam Emison
#* @date 2024-09-19
#* @brief Makefile
#* 
#* Makefile for the Employees files that were provided
#*

CC = g++ # The compiler
TARGET = employee # Makes employee the executable
CFLAGS = -c -Wall -Wextra # Compile with all errors and warnings

# Object Files
OBJS = main.o Employee.o Officer.o Supervisor.o 


all: $(TARGET)

# Links object files to create the executable
$(TARGET): $(OBJS)
	$(CC) $(OBJS) -o $(TARGET)


# Compiles main.o from source
main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) main.cpp


# Compiles Employee.o from source
Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp


# Compiles Officer.o from source
Officer.o: Officer.cpp Officer.h Employee.h
	$(CC) $(CFLAGS) Officer.cpp


# Compiles Supervisor.o from source
Supervisor.o: Supervisor.cpp Supervisor.h Employee.h
	$(CC) $(CFLAGS) Supervisor.cpp



clean: # Should remove all objects, Emacs backups and the target
	rm -f **.o *~ $(TARGET)
