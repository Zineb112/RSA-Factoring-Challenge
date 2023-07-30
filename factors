#!/usr/bin/python3
import sys


def factorize(number):
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return i, number // i
        return None, None


def main():
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        return

    input_file = sys.argv[1]
    try:
        with open(input_file, "r") as file:
            for line in file:
                number = int(line.strip())
                p, q = factorize(number)
                if p and q:
                    print(f"{number}={p}*{q}")

    except FileNotFoundError:
        print(f"Error: File '{input_file}' not found.")
    except ValueError:
        print("Error: Invalid number in the input file.")
    except Exception as e:
        print(f"An error occurred: {e}")


if __name__ == "__main__":
    main()
