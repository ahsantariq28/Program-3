# Program-3
#include <unistd.h>
int pipe(int fildes[2]);
#define maxline 80
main()
{
int n, fd[2];
char line[maxline];
pipe(fd);
if (fork()>0) {
close(fd[0]);
write(fd[1], "Hello\n", 6);
}
else {
close(fd[1]);
n = read(fd[0], line, maxline);
write(1, line, n);
}
}
