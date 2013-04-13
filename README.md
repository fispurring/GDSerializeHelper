It can serialize the data into the Hashtable type and deserialize the Hashtable type data into source type.

To serialize:

	SerializeHelper.Serialize(data);

To deserialize:

	SerializeHeler.Deserialize(data) as SourceType
  
**Notice:**  

Currently,GDSerializeHelper supports commonly used data types,including class,Array and List.  

Considering the size of data packet, GDSerializeHelper only serialize the public properties of class. 



