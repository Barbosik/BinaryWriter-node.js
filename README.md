# BinaryWriter-node.js

![Language](https://img.shields.io/badge/language-node.js-yellow.svg)
![License](https://img.shields.io/badge/license-APACHE2-blue.svg)

Fast and easy tools for binary serialization in node.js

##Usage

```
var BinaryWriter = require('./BinaryWriter.js');
var BinaryReader = require('./BinaryReader.js');

var writer = new BinaryWriter();
writer.writeUInt32(123);
writer.writeInt16(456);
writer.writeUInt8(10);
writer.writeFloat(7.5);
writer.writeDouble(7.7);
writer.writeStringZeroUtf8("Hello world");
writer.writeStringZeroUnicode("Hello world");

var buffer = writer.toBuffer();

var reader = new BinaryReader(buffer);
console.log(reader.readUInt32());
console.log(reader.readInt16());
console.log(reader.readUInt8());
console.log(reader.readFloat());
console.log(reader.readDouble());
console.log(reader.readStringZeroUtf8());
console.log(reader.readStringZeroUnicode());
```

Fast, easy and clean :)

Please let me know if there is any more fastest way for BinaryWriter implementation.
