const http= require('http')


const server= http.createServer((req,res)=>{
    console.log('resquest applied')

    const url= req.url;

    if (url==='/about') {
        res.writeHead(200,{ "Content-Type": "text/html" })
        res.write('<h2>hakkimda </h2>')
    }else if (url==='/contact') {
        res.writeHead(200,{ "Content-Type": "text/html" })
        res.write('<h2>contact</h2>')
    }else if (url==='/') {
        res.writeHead(200,{ "Content-Type": "text/html" })
        res.write('<h2>merhaba hos geldiniz </h2>')
    }else{
        res.writeHead(404,{ "Content-Type": "text/html" })
        res.write('<h2>404 sayfa bulunamadi</h2>')
    }
    console.log(url);
    

    res.end();
})

const port=5000

server.listen(port,()=>{
    console.log('server basariyla baslatildi');
})
