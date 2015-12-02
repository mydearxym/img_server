web端发送格式(POST)： 
```js
{
  type: 'cropped'
  src:"data:image/png;base64,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......."
}
```


node.js 端示意

```javascript
var fs = require('fs')

function decodeBase64Image(dataString) {
  var matches = dataString.match(/^data:([A-Za-z-+\/]+);base64,(.+)$/),
    response = {};

  if (matches.length !== 3) {
    return new Error('Invalid input string');
  }

  response.type = matches[1];
  response.data = new Buffer(matches[2], 'base64');

  return response;
}

module.exports = {

  fuck: function(req, res){
    // console.log("inside testfunc: ", req.body.img);
    var imageBuffer = decodeBase64Image(req.body.img)
    console.log(imageBuffer)
    fs.writeFile('mydearxym.jpg', imageBuffer.data, function(err) {
      console.error(err)
    })
    return res.json({data: '...'});  // 返回上传到阿里云后的地址，并且删除本地文件
  },


}


```
