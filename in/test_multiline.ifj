const ifj = @import("ifj24.zig");

pub fn main()void{
    const a = ifj.string(
        \\first line
        \\ second line
                     \\third line
            \\\n <- this shouldn't be newline
        \\\x25 <- nor this number
        \\\" \" " \\ aaa
        \\
                                                                                                \\
    );
    const b = ifj.string("Normal string\n");
    const c = ifj.concat(a,b);
    ifj.write(c);
}