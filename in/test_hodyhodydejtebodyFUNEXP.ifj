const ifj = @import("ifj24.zig");

pub fn factorial(n: i32) i32 {
    if (n <= 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}

pub fn sumOfFirstN(n: i32) i32 {
    if (n <= 0) {
        return 0;
    } else {
        return n + sumOfFirstN(n - 1);
    }
}

pub fn complexMathOperations(start: i32) i32 {
    var total: i32 = start;
    var i: i32 = 0;

    while (i < 1000) {
        total = total - 2;  
        total = total + 5;  
        i = i + 1;
    }

    return total;
}

pub fn complexStringOperations() []u8 {
    const base = "HODY HODY DEJTE BODY KDYZ NEDATE PLNY POCET DEJTE ASPON NA ZAPOCET. ";
    var result = ifj.string(base);

    var i: i32 = 0;
    while (i < 1000) {
        result = ifj.concat(result, ifj.string(base));
        i = i + 1;
    }

    return result;
}

pub fn nestedFunctionCalls(n: i32) i32 {
    if (n <= 0) {
        return 1;
    } else {
        return nestedFunctionCalls(n - 1) * n;
    }
}

pub fn main() void {

    const factResult = factorial(10);
    ifj.write(factResult);


    const sumResult = sumOfFirstN(100); 
    ifj.write(sumResult);


    const mathResult = complexMathOperations(100);
    ifj.write(mathResult);


    const strResult = complexStringOperations();
    ifj.write(strResult);


    const nestedResult = nestedFunctionCalls(10); // Go deeper to test the recursion depth
    ifj.write(nestedResult);
}
