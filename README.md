const express = require('express')
const app = express()
const port = 3000

const bodyParser = require('body-parser');

const app = express();
const PORT = 3000;

app.use(bodyParser.json());

const productos = [
  { id: 1, nombre: 'Producto 1', precio: 20.5 },
  { id: 2, nombre: 'Producto 2', precio: 15.75 },
  { id: 3, nombre: 'Producto 3', precio: 10.0 },
];

app.get('/', (req, res) => {
  res.send(productos)
})

app.listen(port, () => {
  console.log(Example app listening on port ${port})
})
