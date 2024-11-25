

const ifj = @import("ifj24.zig");

pub fn main() void {
    const str1 = ifj.string("Hello");
    const str2 = ifj.string("");
    const minus1 = 0 - 1;
    const result = ifj.ord(str1, minus1); // Returns 0, index is negative.
    const result2 = ifj.ord(str2, 0);     // Returns 0, empty slice.

    if(result == 0){ifj.write("Good");}else{ifj.write("Bad");}
    if(result2 == 0){ifj.write("Good");}else{ifj.write("Bad");}

}   