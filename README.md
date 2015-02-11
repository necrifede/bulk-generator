#Bulk Generator

## 
A lot of systems works with a lot of data. They need import or export these data. 

## Purposes
Generate big files taking as an entry a simple data like sequence of numbers.
The first goal is generate xml files

## How It Works
The 'Bulk Generator' accept as an entry a simple pattern form to be generated. inside it 
is necessary a sequence that will define the number of generation of the given pattern

### Examples
##### Simple Generation
###### Entry file content
    <my_xml>
      <label>
        <name>SomeName[1,2]</name>
      </label>
    </my_xml>

###### Output file content
    <my_xml>
      <label>
        <name>SomeName1</name>
        <name>SomeName2</name>
      </label>
    </my_xml>

##### Convinatory Generation
###### Entry file content
    <my_xml>
      <user>
        <name>SomeName[1,2]</name>
        <address>[a,b]</address>
      </user>
    </my_xml>
    
###### Output file content
    <my_xml>
      <user>
        <name>SomeName1</name>
        <address>a</address>
      </user>
      <user>
        <name>SomeName1</name>
        <address>b</address>
      </user>
      <user>
        <name>SomeName2</name>
        <address>a</address>
      </user>
      <user>
        <name>SomeName2</name>
        <address>b</address>
      </user>
    </my_xml>

## Design

It is divided in next modules

- File Reader
- File Parser (read variables)
- Convinator
- File Generator

