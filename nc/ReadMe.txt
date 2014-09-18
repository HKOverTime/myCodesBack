MinGW  ª∑æ≥±‡“Î

gcc -c *.c

gcc getopt.o doexec.o netcat.o --output nc.exe -Wl,-L"%LIB_DIR%",-lkernel32,-luser32,-lwinmm,-lws2_32