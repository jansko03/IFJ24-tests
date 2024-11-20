// Program 1: Vypocet faktorialu (iterativne)
// Hlavni telo programu
const ifj = @import("ifj24.zig");
pub fn main() void {
    ifj.write("Zadejte cislo pro vypocet faktorialu\n");
    const a = ifj.readi32();
    if (a) |val| {
        if (val < 0) {
            ifj.write("Faktorial ");
            ifj.write(val);
            ifj.write(" nelze spocitat\n");
        } else {
            var d: f64 = ifj.i2f(val);
            var vysl: f64 = 1.0;
            while (d > 0) {
                vysl = vysl * d;
                d = d - 1.0;
            }
            ifj.write("Vysledek: ");
            ifj.write(vysl);
            ifj.write(" = ");
            const vysl_i32 = ifj.f2i(vysl);
            ifj.write(vysl_i32);
            ifj.write("\n");
        }
    } else { // a == null
        ifj.write("Faktorial pro null nelze spocitat\n");
    }
}
