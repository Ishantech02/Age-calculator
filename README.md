# Age-calculator
javascript age calculator
CODE for age calculator
function calculateAge(birthdateString) {
    let today = new Date();
    let birthDate = new Date(birthdateString);
    let age = today.getFullYear() - birthDate.getFullYear();
    let monthDiff = today.getMonth() - birthDate.getMonth();

    if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < birthDate.getDate())) {
        age--;
    }
    return age;
}

let birthInput = prompt("Enter your birthdate (YYYY-MM-DD):");
let age = calculateAge(birthInput);
alert(`You are ${age} years old.`);
