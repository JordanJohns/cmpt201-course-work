#define _POSIX_C_SOURCE 200809L
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
  char *input;
  size_t buffer_size = 32;
  size_t characters;

  input = (char *)malloc(buffer_size * sizeof(char));

  char *values[5];
  int i = 0;
  int running = 1;

  while (running) {
    printf("Enter input: ");
    characters = getline(&input, &buffer_size, stdin);

    values[i] = strdup(input);
    if (strcmp(values[i], "print\n") == 0) {
      running = 0;
    }

    i += 1;
    if (i > 4) {
      i = 0;
    }
  }

  for (int x = 0; x < 5; x++) {
    if (values[i] != NULL) {
      printf("%s", values[i]);
    }
    i += 1;
    if (i > 4) {
      i = 0;
    }
  }

  free(input);
  return 0;
}
