Select XML Nodes by Name
------

```C#
string xmlString = @"
  <Employees>
    <Employee>
        <FirstName>John</FirstName>
        <LastName>Smith</LastName>
    </Employee>
    <Employee>
        <FirstName>Patrick</FirstName>
        <LastName>Clark</LastName>
    </Employee>
    <Employee>
        <FirstName>Jack</FirstName>
        <LastName>Russell</LastName>
    </Employee>
    <Employee>
        <FirstName>Lillian</FirstName>
        <LastName>Parker</LastName>
    </Employee>
  </Employees>
";

var xml = new XmlDocument();
xml.LoadXml(xmlString);

XmlNodeList employees = xml.SelectNodes("/Employees/Employee");

foreach (XmlNode employee in employees)
{
  string firstName = employee["FirstName"].InnerText;
  string lastName = employee["LastName"].InnerText;
  
  Console.WriteLine($"Employee name: {firstName} {lastName}");
}
```

Select XML Nodes by Attribute value
------

```C#
string xmlString = @"
  <Employees>
    <Employee type='Developer'>
        <FirstName>John</FirstName>
        <LastName>Smith</LastName>
    </Employee>
    <Employee type='Developer'>
        <FirstName>Patrick</FirstName>
        <LastName>Clark</LastName>
    </Employee>
    <Employee type='Manager'>
        <FirstName>Jack</FirstName>
        <LastName>Russell</LastName>
    </Employee>
    <Employee type='Developer'>
        <FirstName>Lillian</FirstName>
        <LastName>Parker</LastName>
    </Employee>
  </Employees>
";


var xml = new XmlDocument();
xml.LoadXml(myXmlString);

XmlNodeList employees = xml.SelectNodes("/Employees/Employee[@type='Developer']");

foreach (XmlNode employee in employees)
{
  string firstName = employee["FirstName"].InnerText;
  string lastName = employee["LastName"].InnerText;
  
  Console.WriteLine($"Employee name: {firstName} {lastName}");
}
```
