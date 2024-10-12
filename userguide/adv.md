# Advanced Usage

## Interpreted API (1.1)
Here is a brief introduction of how to use FridaCodeManagers inbuild interpreted API to take over control over your projects build process

### Sytax
The Syntax is simular to XML. So you use tags like `<tag>content</tag>`. It also has placeholders like `<placeholder>` which gives your script access to information stored in the APP or information provided by `libfcm`.

### Classes
The parser parses classes. like..
```
# Main Class

<api>

    ... sub classes ...

</api>
```
As you can see api is the main class.

### Getting Started
Youll first have to create a class called "version" to tell the API interpreter of FridaCodeManager for what version it should parse, this is to avoid issues in the future when we changed the API a bit.
Do it like...
```
<api>
    <version>1.1</version>

    ... sub classes ...
</api>
```
After the version class you can add more subclasses the 1.1 version supports.