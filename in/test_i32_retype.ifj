const ifj = @import("ifj24.zig");



pub fn main() void{
    const a : i32 = 5;
    var   b : ?f64 = ifj.readf64();
    if(b)|B|{
        const ab : f64 = a + B;
        ifj.write(ab);
    }
    else{
        b = 5.2;
    }
}