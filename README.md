// Check if a number is armstrong number
pub fn is_armstrong_number(num: u32) -> bool {
let mut digits = Vec::new();
let mut len = 0;
let mut n = num;

while n != 0 {
len = len + 1;
digits.push(n % 10);
n = n / 10;
}

num == digits.iter().fold(0, |acc, d| acc + d.pow(len))
}
