const ifj = @import("ifj24.zig");

pub fn main() void {
  const y = ifj.readi32();
  if(y) |b|{
    ifj.write(y);
    ifj.write("\n");
    const a = 5 / b;
    ifj.write(a);
    ifj.write("\n");
  }
  else{}
}