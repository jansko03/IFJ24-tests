const ifj = @import("ifj24.zig");

pub fn main() void {
    const a = ifj.readstr();
    var a_without_null = ifj.string("");
    if(a) |b|{
        a_without_null = b;
    }
    else{}
    ifj.write(a);
    ifj.write("\n");
    const str_after = ifj.string("--after");
    const str_before = ifj.string("before--");
    
    const len_after = ifj.length(str_after);
    ifj.write(ifj.concat(ifj.string("Sring and length: "), str_after));
    ifj.write(len_after);
    ifj.write("\n");

    var cc = ifj.concat(ifj.concat(str_before, a_without_null), str_after);
    ifj.write(cc);
    ifj.write("\n");

    cc = ifj.concat(ifj.string(""), ifj.string(""));
    ifj.write(cc);
    ifj.write(ifj.length(cc));
    ifj.write("\n");

    const test: []u8 = ifj.string("abcdef");
    const sub = ifj.substring(test, 1, 3);
    if(sub) |sub_without_null|{
        ifj.write(ifj.concat(sub_without_null, ifj.string("\n")));
    }
    else{}

    ifj.write("abeceda: ");
    
    var i = 65;
    while(90 >= i){
        const j = i;
        ifj.write(ifj.chr(j));
        i = i+      1;
    }
    ifj.write("\n");

    const a_len = ifj.length(a_without_null);
    var j = 0;
    while(a_len > j){
        ifj.write(ifj.ord(a_without_null, j));
        ifj.write("\n");
        j = j + 1;
    }
}