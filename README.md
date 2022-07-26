# Data-Modelling
Write a set of DDD entity and value-object classes in C# to 

Value Objects are no identiy and as well as immutable.

pubic class Name
{
	public string First { get; }
}


Name obj1 = new Name('Suresh');
// console.write(obj1.First) -- Suresh
Name obj2 = new Name('Manish');
// console.write(obj1.First) -- Manish
set obj2=obj1;
obj2.First='vinoth'
// console.write(obj1.First) -- Vinoth
  
When object changes its ref. memorty and its wont changes their value. Hence, this attribut should not use us 
for identify purpose.

When entity should be uniquelty identify the attributes and should be in proper struture. lets take exmple for stud information. 

// Entity
public class Person
{
    public int Id { get; set; }
    public string Name { get; set; }
    public Address Address { get; set; }
}
 
// Value Object,
public class Address
{
    public string City { get; set; }
    public string ZipCode { get; set; }
}

In above ex:
Don’t introduce separate tables for value objects, just inline them into the parent entity table. 
and moreover entieies have identiy and Value object does not. Also, entities have a histroty and valeue objects 0 lifespan and make sure always prefer value objects over entities in your domain model.
