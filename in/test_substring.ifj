const ifj = @import("ifj24.zig");

pub fn main() void {
    const str1 = ifj.string("Hello");
    const str2 = ifj.string("");
    const result = ifj.substring(str1, 4, 2); // Returns null, as i > j.
    const result2 = ifj.substring(str2, 0, 1);    // Returns null, empty slice.
    if(result)|a|{
        ifj.write("Not null\n");
        ifj.write(a);
    }
    else{ifj.write("Good");}
    if(result2)|a|{
        ifj.write("Not null\n");
        ifj.write(a);
    }
    else{ifj.write("Good");}

}
