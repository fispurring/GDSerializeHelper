**What's GDSerializeHelper?**  
GDSerializeHelper is a Serializer for Photon which is a Cross-Platform Network Engine.It can serialize the data into the Hashtable type supported by Photon and deserialize the Hashtable type data serialized by GDSerializeHelper into source type. The data serialized by GDSerializeHelper is small,which is much more smaller than the data serialized by BinaryFormatter.  

To serialize:

	SerializeHelper.Serialize(data);

To deserialize:

	SerializeHeler.Deserialize(data) as SourceType

Complete Example:  

	class MyClass
	{
		public int A {get;set;}
		public int B {get;set;}
		public int C {get;set;}
	}

	Hashtable SerializeMyClass(MyClass myClass)
	{
		return SerializeHelper.Serialize(myClass);
	}

	MyClass DeserializeMyClass(Hashtable data)
	{
		return SerializeHelper.Deserialize(data) as MyClass;
	}
  
  
**Notice:**  

Currently,GDSerializeHelper supports commonly used data types,including class,Array and List.  

Considering the size of data packet, GDSerializeHelper only serialize the public properties of class. 



