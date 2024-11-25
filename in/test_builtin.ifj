const ifj = @import("ifj24.zig");

pub fn main() void {
    // Example of `ifj.readstr`
    ifj.write("Enter a string: ");
    const inputStr: ?[]u8 = ifj.readstr();
    if (inputStr)|str| {
        ifj.write("You entered the string: ");
        ifj.write(str);
        ifj.write("\n");
    } else {
        ifj.write("Error: Invalid string input.\n");
    }

    // Example of `ifj.readi32`
    ifj.write("Enter an integer: ");
    const inputInt: ?i32 = ifj.readi32();
    if (inputInt)|intVal| {
        ifj.write("You entered the integer: ");
        ifj.write(intVal);
        ifj.write("\n");

        // Example of `ifj.i2f`
        const intToFloat: f64 = ifj.i2f(intVal);
        ifj.write("Converted integer to float: ");
        ifj.write(intToFloat);
        ifj.write("\n");
    } else {
        ifj.write("Error: Invalid integer input.\n");
    }

    // Example of `ifj.readf64`
    ifj.write("Enter a floating-point number: ");
    const inputFloat: ?f64 = ifj.readf64();
    if (inputFloat)|floatVal| {
        ifj.write("You entered the float: ");
        ifj.write(floatVal);
        ifj.write("\n");

        // Example of `ifj.f2i`
        const floatToInt: i32 = ifj.f2i(floatVal);
        ifj.write("Converted float to integer: ");
        ifj.write(floatToInt);
        ifj.write("\n");
    } else {
        ifj.write("Error: Invalid floating-point input.\n");
    }

    // Example of `ifj.string`, `ifj.length`, and `ifj.concat`
    const str1: []u8 = ifj.string("Hello");
    const str2: []u8 = ifj.string(", World!");
    const concatenated: []u8 = ifj.concat(str1, str2);
    ifj.write("Concatenated string: ");
    ifj.write(concatenated);
    ifj.write("\n");
    ifj.write("Length of concatenated string: ");
    const len = ifj.length(concatenated);
    ifj.write(len);
    ifj.write("\n");

    // Example of `ifj.substring`
    const subStr: ?[]u8 = ifj.substring(concatenated, 0, 5);
    if (subStr)|sub| {
        ifj.write("Substring (first 5 chars): ");
        ifj.write(sub);
        ifj.write("\n");
    } else {
        ifj.write("Error: Invalid substring operation.\n");
    }

    // Example of `ifj.strcmp`
    const comparisonResult: i32 = ifj.strcmp(str1, str2);
    ifj.write("String comparison result (str1 vs str2): ");
    ifj.write(comparisonResult);
    ifj.write("\n");

    // Example of `ifj.ord`
    const ordValue: i32 = ifj.ord(concatenated, 1); // Get ASCII of the 2nd character
    ifj.write("Ordinal value of 2nd character in concatenated string: ");
    ifj.write(ordValue);
    ifj.write("\n");

    // Example of `ifj.chr`
    const charFromOrd: []u8 = ifj.chr(ordValue);
    ifj.write("Character created from ordinal value: ");
    ifj.write(charFromOrd);
    ifj.write("\n");
}
