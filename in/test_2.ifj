// Program 2: Vypocet faktorialu (rekurzivne)
const ifj = @import("ifj24.zig");
// Hlavni funkce
pub fn main() void {
    ifj.write("Zadejte cislo pro vypocet faktorialu: ");
    const inp = ifj.readi32();
    if (inp) |INP| {
        if (INP < 0) {
            ifj.write("Faktorial nelze spocitat!\n");
        } else {
            const vysl = factorial(INP);
            ifj.write("Vysledek: ");
            ifj.write(vysl);
        }
    } else {
        ifj.write("Chyba pri nacitani celeho cisla!\n");
    }
}

// Pomocna funkce pro dekrementaci celeho cisla o zadane cislo
pub fn decrement(n: i32, m: i32) i32 {
    return n - m;
}

// Definice funkce pro vypocet hodnoty faktorialu
pub fn factorial(n: i32) i32 {
    var result: i32 = 0 - 1;
    if (n < 2) {
        result = 1;
    } else {
        const decremented_n = decrement(n, 1);
        const temp_result = factorial(decremented_n);
        result = n * temp_result;
    }
    return result;
}
