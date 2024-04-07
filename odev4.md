const fs = require("fs");

const addFunction = () => {
  fs.writeFile("employees.json", "{"name": "Emil", "yas": 0.5}", "utf-8", (err) => {
    console.log(err);
  });
  console.log("emil dunyaya geldi");
};

const updateFunction = () => {
  fs.appendFile(
    "employees.json",
    "\n {"name": "Emil", "yas": 2.5} ",
    "utf-8",
    (err) => {
      if (err) {
        console.log(err);
      }
    }
  );
  console.log("emilin dvijeniyasi yenilendi ");
};


const readFunction=()=>{
    fs.readFile('employees.json','utf-8',(err,data)=>{
    console.log(data)
    })
}

const removeFunction = () => {
  fs.unlink("employees.json", (err) => {
    console.log(err);
  });

  console.log("emil dunyadan silindi");
};
