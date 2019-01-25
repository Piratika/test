const triangle = (leg1, leg2, hypotenuse) => {
  return (leg1 > 0 && leg2 > 0 && hypotenuse > 0) && hypotenuse ** 2 == leg1 ** 2 + leg2 ** 2;
}

console.log(triangle(3,4,5));
console.log(triangle(1,4,5));
console.log(triangle(3,4,-5));

const repeat = (str = '', n = 2) => {
  if (n == 0) return '';
  return str + repeat(str, n - 1);
}

console.log(repeat('str', 4));
console.log(repeat('at', 2));

const room = (student, desk) => {
  if (student == desk * 2) return 'все отлично';
  return (student - desk * 2 > 0) ? `не хватает ${student - desk * 2} парт` : `лишних ${desk * 2 - student} парт`;
}

console.log(room(4,2));
console.log(room(7,2));
console.log(room(7,6));

const grading = (grade) => {
  if (grade <= 0 && grade > 10) return 'нет таких';
  switch (grade) {
    case 1:
    case 2: return 'Unsatisfactory'; break;
    case 3:
    case 4: return 'Satisfactory'; break;
    case 5: return 'Almost good'; break;
    case 6: return 'Good'; break;
    case 7: return 'Very good'; break;
    case 8: return 'Almost excellent'; break;
    case 9: return 'Excellent'; break;
    case 10: return 'Brilliant'; break;
  }
}

console.log(grading(1));
console.log(grading(4));
console.log(grading(5));

const expectZero = () => {
  var isItZero;
  do {
    isItZero = prompt('Введите число');
  } while (isItZero != 0)
  return;
}

const expect100 = () => {
  var sum = 0;
  var i = 0;
  while (sum < 100) {
  	i++;
    sum += +prompt('Введите число');
  }
  console.log(sum);
  return i;
}

// 7 задача

const isPrime = (num) => {
  if (num <= 0) return 'Неа';
  var priming = true;
  for (let i = 2; i < num / 2; i++) {
    if (num % i == 0) {
      priming = false;
      break;
    }
  }
  return priming;
}

console.log(isPrime(15));

// 8 задача

const monthSeason = (month) => {
  if (month <= 0 && month > 12) return 'нет таких';
  switch (month) {
    case 1:
    case 2: 
    case 12: return 'зима'; break;
    case 3:
    case 4:
    case 5: return 'весна'; break;
    case 6:
    case 7:
    case 8: return 'лето'; break;
    case 9:
    case 10:
    case 11: return 'осень'; break;
  }
}

console.log(monthSeason(1));
console.log(monthSeason(4));
console.log(monthSeason(5));

// 9 задача

const from99To10 = () => {
  for (let i = 99; i >= 10; i--) {
    if (i % 10 == 7 || i % 7 == 0) console.log(i);
  }
}

from99To10();
