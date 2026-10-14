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
//6
