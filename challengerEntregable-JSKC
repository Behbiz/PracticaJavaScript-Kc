/* 
  si utilizáis algún import en vuestra solución, recordad que hay que indicarle a node 
  que estamos utilizando módulos. Para ello, debemos incluir el fichero package.json que 
  veis en este repositorio. En caso de que no os funcione, contactadme por discord.
*/
import { waitForDebugger } from "inspector";
import readline from "readline";

// configuramos la utilidad de node para que los datos se pidan y se muestren por consola.
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

const questions = `
1- Mostrar en formato de tabla todos los alumnos. 
2- Mostrar por consola la cantidad de alumnos que hay en clase.
3- Mostrar por consola todos los nombres de los alumnos.
4- Eliminar el último alumno de la clase.
5- Eliminar un alumno aleatoriamente de la clase.
6- Mostrar por consola todos los datos de los alumnos que son chicas.
7- Mostrar por consola el número de chicos y chicas que hay en la clase.
8- Mostrar true o false por consola si todos los alumnos de la clase son chicas.
9- Mostrar por consola los nombres de los alumnos que tengan entre 20 y 25 años.
10- Añadir un alumno nuevo con los siguientes datos:
  - nombre aleatorio.
  - edad aleatoria entre 20 y 50 años.
  - género aleatorio.
  - listado de calificaciones vacío.
11- Mostrar por consola el nombre de la persona más joven de la clase.
12- Mostrar por consola la edad media de todos los alumnos de la clase.
13- Mostrar por consola la edad media de las chicas de la clase.
14- Añadir nueva nota a los alumnos. Por cada alumno de la clase, tendremos que calcular una nota de forma aleatoria(número entre 0 y 10) y añadirla a su listado de notas.
15- Ordenar el array de alumnos alfabéticamente según su nombre.
`;
function askQuestion(allQuestions) {
  console.log(allQuestions);
  rl.question("Choose a number or press 0 to exit :", (answer) => {
    if (answer === "0") {
      console.log("Good bye");
      return;
    } else if (answer === "1") {
      showStudentInTableFormat();
    } else if (answer === "2") {
      showStudentsNumber();
    } else if (answer === "3") {
      showStudentsName();
    } else if (answer === "4") {
      deleteLastStudents();
    } else if (answer === "5") {
      deleteRandomName();
    } else if (answer === "6") {
      showFemaleStudent();
    } else if (answer === "7") {
      showMaleStudent();
    } else if (answer === "8") {
      showBooleansStudent();
    } else if (answer === "9") {
      showNameMilleniusStudent();
    } else if (answer === "10") {
      addStudent();
    } else if (answer === "11") {
      showNewStudent();
    } else if (answer === "12") {
      showAverageAge();
    } else if (answer === "13") {
      showAverageAgeFemale();
    } else if (answer === "14") {
      examScoresStudent();
    } else if (answer === "15") {
      alfabeticOrdenStudent();
    } else {
      console.log("Invalid answer: " + answer);
    }

    askQuestion(allQuestions);
  });
}
askQuestion(questions);

const students = [
  {
    age: 32,
    examScores: [],
    gender: "male",
    name: "edu",
  },
  {
    age: 29,
    examScores: [],
    gender: "female",
    name: "silvia",
  },
  {
    age: 30,
    examScores: [],
    gender: "male",
    name: "carlos",
  },
  {
    age: 59,
    examScores: [],
    gender: "female",
    name: "ana",
  },
  {
    age: 32,
    examScores: [],
    gender: "male",
    name: "pepe",
  },
  {
    age: 21,
    examScores: [],
    gender: "female",
    name: "isabel",
  },
  {
    age: 22,
    examScores: [],
    gender: "male",
    name: "victor",
  },
  {
    age: 21,
    examScores: [],
    gender: "female",
    name: "luisa",
  },
  {
    age: 32,
    examScores: [],
    gender: "male",
    name: "francisco",
  },
  {
    age: 21,
    examScores: [],
    gender: "female",
    name: "cecilia",
  },
  {
    age: 23,
    examScores: [],
    gender: "male",
    name: "leo",
  },
  {
    age: 20,
    examScores: [],
    gender: "female",
    name: "virginia",
  },
];

const availableMaleNames = [
  "pepe",
  "juan",
  "victor",
  "Leo",
  "francisco",
  "carlos",
];
const availableFemaleNames = [
  "cecilia",
  "ana",
  "luisa",
  "silvia",
  "isabel",
  "virginia",
];
const availableGenders = ["male", "female"];

// 1- Mostrar en formato de tabla todos los alumnos.
const allStudentsArray = [...availableMaleNames, ...availableFemaleNames];
function showStudentInTableFormat() {
  console.table(allStudentsArray);
}
// 2- Mostrar por consola la cantidad de alumnos que hay en clase.
function showStudentsNumber() {
  console.log(allStudentsArray.length);
}

// 3- Mostrar por consola todos los nombres de los alumnos.
function showStudentsName() {
  console.log(...allStudentsArray);
}
// 4- Eliminar el último alumno de la clase.
const auxArrayLast = [...allStudentsArray];
function deleteLastStudents() {
  auxArrayLast.pop();
  console.log(...auxArrayLast);
}
// 5- Eliminar un alumno aleatoriamente de la clase.
const auxArrayRemove = [...allStudentsArray];
function deleteRandomName() {
  auxArrayRemove.splice(calculateRandomNumber(0, allStudentsArray.length));
  console.log(auxArrayRemove);
}
function calculateRandomNumber(min, max) {
  const randomNumber = Math.floor(Math.random() * (max - min)) + min;
  return randomNumber;
}
// 6- Mostrar por consola todos los datos de los alumnos que son chicas.
const femaleStudent = students.filter(
  (students) => students.gender === "female"
);
const maleStudent = students.filter((students) => students.gender === "male");

function showFemaleStudent() {
  console.log(femaleStudent);
}
// 7- Mostrar por consola el número de chicos y chicas que hay en la clase.
function showMaleStudent() {
  console.log(femaleStudent.length + maleStudent.length);
}
// 8- Mostrar true o false por consola si todos los alumnos de la clase son chicas.
function showBooleansStudent() {
  if (maleStudent.length > 0) {
    console.log(false);
  } else {
    console.log(true);
  }
}
// 9- Mostrar por consola los nombres de los alumnos que tengan entre 20 y 25 años.
function showNameMilleniusStudent() {
  const studentsName = students
    .filter((student) => student.age >= 20 && student.age <= 25)
    .map((student) => student.name);
  console.log(studentsName);
}
// 10- Añadir un alumno nuevo con los siguientes datos:nombre aleatorio.edad aleatoria entre 20 y 50 años.género aleatorio.listado de calificaciones vacío.
function addStudent() {
  const newStudent = {
    age: 32,
    examScores: [],
    gender: "male",
    name: "pepito",
  };
  students.push(newStudent);
  console.log(students);
}
//11- Mostrar por consola el nombre de la persona más joven de la clase.
function showNewStudent() {
  const minAge = students.reduce((a, b) => {
    if (b.age < a.age) a = b;
    return a;
  });
  console.log(minAge.name);
}
// 12- Mostrar por consola la edad media de todos los alumnos de la clase.
function sumAge(students) {
  let sum = 0;
  for (const student of students) {
    sum += student.age;
  }
  return sum;
}
function showAverageAge() {
  console.log(sumAge(students) / students.length);
}

// 13- Mostrar por consola la edad media de las chicas de la clase.
function showAverageAgeFemale() {
  console.log(sumAge(femaleStudent) / femaleStudent.length);
}

// 14- Añadir nueva nota a los alumnos. Por cada alumno de la clase, tendremos que calcular una nota de forma aleatoria(número entre 0 y 10) y añadirla a su listado de notas.
function examScoresStudent() {
  students.forEach((student) => {
    student.examScores.push(calculateRandomNumber(0, 10));
  });
  console.log(students);
}
// 15- Ordenar el array de alumnos alfabéticamente según su nombre.
function alfabeticOrdenStudent() {
  const sortedStudents = students.sort((a, b) => a.name.localeCompare(b.name));
  console.log(sortedStudents);
}

/*Requisitos opcionales
Os recomiendo encarecidamente que los intentéis, no son difíciles!*/

// 16- Mostrar por consola el alumno de la clase con las mejores notas.El alumno con mejores notas es aquel cuyo sumatorio de todas sus notas es el valor más alto de todos.

// 17- Mostrar por consola la nota media más alta de la clase y el nombre del alumno al que pertenece.

// 18- Añadir un punto extra a cada nota existente de todos los alumnos. Recordad que la nota máxima posible es 10. Si los alumnos aún no tienen registrada ninguna nota, les pondremos un 10.
