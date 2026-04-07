# project-2

const form = document.querySelector('form');

form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parentInt(document.querySelector('#height').value);
  const weight = parentInt(document.querySelector('#weight').value);
  const results = parentInt(document.querySelector('#results');

  if(height="" || height < 0 || isNaN(height) ){
    results.innerHTML = `Please give the valid height${height}`
  }else  if(weight="" || weight < 0 || isNaN(weight) ){
    results.innerHTML = `Please give the valid weight${weight}`
  }else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);

      // show the result
    results.innerHTML = `<span>${bmi}</span>`
  }
});
