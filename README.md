# digital-clock
This code is a simple program that continuously prints the current time in the format HH:MM:SS. Let's go through the code step by step:

1. The code includes the necessary header files: `stdio.h`, `time.h`, `unistd.h`, and `stdlib.h`. These headers provide the required functions and definitions for the program.

2. The `main()` function is the entry point of the program.

3. The variables `hour`, `minute`, and `second` are declared and initialized to 0. These variables will store the current time.

4. The program enters an infinite `while` loop using `while(1)`, which means the loop will continue indefinitely until the program is interrupted.

5. Inside the loop, the `system("clear")` function is called to clear the output screen. This is done to create a continuously updating display of the time without cluttering the console.

6. The current time is printed using the `printf()` function. The format specifier `%02d` ensures that each value is printed with at least two digits, padded with leading zeros if necessary.

7. The `fflush(stdout)` function is used to flush the output buffer and ensure that the time is immediately displayed on the screen.

8. The `second` variable is incremented by 1 to represent the passage of time.

9. The `if` statements check if `second` has reached 60. If it has, it means a minute has passed, so `minute` is incremented by 1, and `second` is reset to 0.

10. Similarly, the next `if` statement checks if `minute` has reached 60, indicating an hour has passed. In that case, `hour` is incremented by 1, and `minute` is reset to 0.

11. The last `if` statement checks if `hour` has reached 24, which means a full day has passed. In this case, `hour`, `minute`, and `second` are all reset to 0 to start counting from the beginning of the next day.

12. After all the time calculations, the program pauses for 1 second using the `sleep(1)` function from the `unistd.h` header. This ensures that the time displayed is updated every second.

13. The program continues to loop indefinitely, continuously updating and displaying the current time.

Note: The `system("clear")` function used in this code is specific to Unix-like systems. If you're using a Windows system, you can replace it with `system("cls")` to clear the screen.
