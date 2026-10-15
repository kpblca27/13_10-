//1
function fillArray(length, value){
    return new Array(length).fill(value);
}
console.log(fillArray(10, "Germes"));

// 2
function sort123(arr) {
    return [...arr].sort(function(a, b) { 
        return a - b; });
}
function sort321(arr) {
    return [...arr].sort(function(a, b) { 
        return b - a; });
}
const nums = [10, -5, 2, 0, 33];
// либо с добавлением promt чтобы вводить числа с клавиатуры
// let text = promt("введите числа через запятую:");
// const nums = text.split(",").map(Number)
console.log(sort123(nums));
console.log(sort321(nums));

//3
const appointment = {
   Name: "Шишкин Ш",
   doctorName: "Шуев У",
   date: "06.07.2027",
   time: "12am",
   cabinetik: "02_67"
};
function buildMessage(appointment) {
return (`Имя: ${appointment.Name}
Имя врача: ${appointment.doctorName}
Дата приема: ${appointment.date}
Время приема: ${appointment.time}
Кабинет: ${appointment.cabinetik}`)
}
console.log(buildMessage(appointment));

//4
 async function hashStr(str) {
    var buf = await crypto.subtle.digest("SHA-256", new TextEncoder().encode(str));
    return Array.from(new Uint8Array(buf)).map(b => b.toString(16).padStart(2, "0")).join("");
}

hashStr("aBrakadabra").then(function(res) {
    console.log("", res); });
    
//5
     function uuid(isAuthourized){
           return  (isAuthourized&&crypto.randomUUID) ? crypto.randomUUID() : null;
        }
        console.log(uuid(true));

//
//9
function rev(str) {
    let res = '';
    for (let i = str.length - 1; i >= 0; i--) {
        res = res + str[i];
    }
    return res;
}

//10
function isPal(str) {
    let clean = str.toLowerCase().replace(/[^а-яёa-z0-9]/g, '');
    let reversed = clean.split('').reverse().join('');
    return clean === reversed;
}
console.log(isPal("А роза упала на лапу Азора"));
