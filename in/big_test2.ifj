const ifj = @import("ifj24.zig");

// Main program entry point
pub fn main() void {
    ifj.write("Starting complex program with nullable handling, recursion, and nested conditions.\n");

    // Complex usage of nullable values with nested conditionals
    const a: ?i32 = null;
    const b: ?i32 = 10;
    const c: ?i32 = 5;

    if (a) |value| {
        ifj.write("Nullable a is not null: ");
        ifj.write(value);
        ifj.write("\n");
    } else {
        if (b) |value| {
            ifj.write("Nullable a is null, but b is not null: ");
            ifj.write(value);
            ifj.write("\n");
        } else {
            if (c) |value| {
                ifj.write("Nullable a and b are null, but c is not null: ");
                ifj.write(value);
                ifj.write("\n");
            } else {
                ifj.write("All nullable values are null.\n");
            }
        }
    }

    // Function call with multiple nullable parameters
    const sum = nullable_sum(a, b);
    ifj.write("Sum of a and b: ");
    ifj.write(sum);
    ifj.write("\n");

    // Nested conditional to check for non-nullable conditions
    const x: i32 = 20;
    const y: i32 = 15;

    if (x > y) {
        ifj.write("x is greater than y\n");
        
        // Check if x is even using subtraction instead of modulo
        var half_x = x - 2 * (x / 2);  // Mimics x % 2 == 0 by using integer division
        if (half_x == 0) {
            ifj.write("x is even\n");
        } else {
            ifj.write("x is odd\n");
        }
        half_x = 0;
    } else {
        ifj.write("x is not greater than y\n");
        
        // Check if y is even using subtraction instead of modulo
        var half_y = y - 2 * (y / 2);  // Mimics y % 2 == 0 by using integer division
        if (half_y == 0) {
            ifj.write("y is even\n");
        } else {
            ifj.write("y is odd\n");
        }
        half_y = 0;
    }

    // While loop for reading inputs and performing a sum
    var total_sum: i32 = 0;
    var continue_input: i32 = 1;
    ifj.write("Enter numbers to sum (0 to stop):\n");

    while (continue_input != 0) {
        const input = ifj.readi32();
        if (input) |num| {
            if (num == 0) {
                continue_input = 0;
            } else {
                total_sum = total_sum + num;
            }
        } else {
            ifj.write("Invalid input, try again.\n");
        }
    }

    ifj.write("Total sum: ");
    ifj.write(total_sum);
    ifj.write("\n");
    ifj.write("Enter hello : ");
    // Handling strings and their comparison
    const input_str = ifj.readstr();
    const expected_str = ifj.string("hello");

    if (input_str) |str| {
        const result = ifj.strcmp(str, expected_str);
        if (result == 0) {
            ifj.write("Correct string entered!\n");
        } else {
            ifj.write("Incorrect string, exiting program.\n");
            return;
        }
    } else {
        ifj.write("No string input, exiting program.\n");
        return;
    }

    // Test completed
    ifj.write("Program completed successfully.\n");
}

// Function that takes nullable parameters and returns their sum
pub fn nullable_sum(a: ?i32, b: ?i32) i32 {
    var sum: i32 = 0;
    if (a) |value| {
        sum = sum + value;
    }else{}
    if (b) |value| {
        sum = sum + value;
    }else{}
    return sum;
}
