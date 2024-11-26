const ifj = @import("ifj24.zig");

// Function to compute the factorial of a number using a while loop
pub fn factorial(n: i32) i32 {
    var result: i32 = 1;
    var counter: i32 = n;

    while (counter > 1) {
        result = result * counter;
        counter = counter - 1;
    }

    return result;
}

// Function to count occurrences of a character in a string
pub fn countOccurrences(s: []u8, targetChar: []u8) i32 {
    const len = ifj.length(s);
    var count: i32 = 0;
    var i: i32 = 0;

    while (i < len) {
        const charSlice = ifj.substring(s, i, i + 1);
        var   charSlice1 = ifj.string("");
        if(charSlice)|a|{
            charSlice1 = a;
        }        else{
            ifj.write("ERROR\n");
            return 0;
        }
        if (ifj.strcmp(charSlice1, targetChar) == 0) {
            count = count + 1;
        } else {
            // No action needed for mismatched character
        }
        i = i + 1;
    }

    return count;
}

// Function to generate a complex string based on input and conditions
pub fn complexStringManipulation(input: []u8) []u8 {
    const len = ifj.length(input);
    var output = ifj.string("");

    if (len > 10) {
        const reversed = reverseString(input);
        output = ifj.concat(ifj.string("Reversed: "), reversed);
    } else {
        output = ifj.concat(ifj.string("Original: "), input);
    }

    return output;
}

// Helper function to reverse a string
pub fn reverseString(s: []u8) []u8 {
    const len = ifj.length(s);
    var reversed = ifj.string("");
    var i: i32 = len - 1;

    while (i >= 0) {
        const charSlice = ifj.substring(s, i, i + 1);
        var   charSlice1 = ifj.string("");
        if(charSlice)|a|{
            charSlice1 = a;
        }
        else{
            ifj.write("ERROR\n");
            return ifj.string("ERROR\n");
        }
        reversed = ifj.concat(reversed, charSlice1);
        i = i - 1;
    }

    return reversed;
}

// Main logic function
pub fn mainLogic() void {
    // Input string
    const inputStr = ifj.string("Helloo, Zig World!");
    const charToFind = ifj.string("o");

    // Count occurrences of 'o' in the string
    const occurrences = countOccurrences(inputStr, charToFind);

    if (occurrences > 0) {
        const output = ifj.concat(
            ifj.string("Occurrences of 'o': "), ifj.concat(
            ifj.string("should be : 3\n"), ifj.string("Calculated: ")) 
        );
        ifj.write(output);
        ifj.write(occurrences);
        ifj.write("\n");
        
    } else {
        ifj.write(ifj.string("No occurrences found."));
    }

    // Perform factorial computation
    const factorialResult = factorial(5); // Example with 5
    ifj.write(ifj.concat(ifj.string("Factorial of 5: "), ifj.concat(ifj.string("120"), ifj.string(", calculated: "))));
    ifj.write(factorialResult);
    ifj.write("\n");
    // Manipulate string based on its length
    const manipulatedStr = complexStringManipulation(inputStr);
    ifj.write(manipulatedStr);
}

// Main function
pub fn main() void {
    mainLogic();
    ifj.write("\n");
}
