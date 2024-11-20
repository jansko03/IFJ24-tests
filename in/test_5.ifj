// Ukazka prace s retezci a vestavenymi funkcemi 
const ifj = @import("ifj24.zig");

pub fn main() void {
  const s1 : []u8 = ifj.string( 
    \\Toto 
    \\ je 
    \\
    \\ nejaky 
                        \\ text  // ve viceradkovem retezcovem literalu nelze mit komentar
    ); // ukoncujici uvozovky ovlivnuji implicitni odsazeni vnitrnich radku retezce
  ifj.write(s1);
}

