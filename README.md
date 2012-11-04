**GDSerializeHelper is a Serializer for Photon,which is a Cross-Platform Network Engine.**

To serialize the data into the Hashtable type,which is supported by Photon:
	SerializeHelper.Serialize(data);

To deserialize the Hashtable type data,which is serialized by GDSerializeHelper,into source type:
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

Notice:
Currently,GDSerializeHelper supports commonly used data types,including class,Array and List.
Considering the size of data packet, GDSerializeHelper only serialize the public properties of class. 



