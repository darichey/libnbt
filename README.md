#libnbt
A small library for reading the Named Binary Tag (NBT) format.

##Quick Start
Currently, this library supports the reading of uncompressed NBT files, gzip compressed NBT files, and .mca files. The following example exhibits the reading of each file.
```
// Reading an uncompressed nbt file
TagCompound uncompressed = LibNBT.readFromNBTFile(new File("uncompressed.nbt"), false);
TagByte tagByte = (TagByte) uncompressed.get("byte"); // Reading a tag called "byte" from the compound.

// Reading a compressed nbt file
TagCompound compressed = LibNBT.readFromNBTFile(new File("compressed.nbt"), true);
TagByte tagByte = (TagByte) compressed.get("byte"); // Reading a tag called "byte" from the compound.

// Reading a .mca region file
List<TagCompound> tags = LibNBT.readFromMCAFile(new File("r.0.0.mca"));
```

##Notes
The writing of NBT files is not currently supported by this library.
