XML WSDL (Web Services Description Language)
============================================

**WSDL** (Web Services Description Language) is an XML-based language used to describe the functionality offered by a web service.  
It provides a formalized way for a web service to describe its operations, input/output messages, and the communication protocols it supports.

 Key Components of a WSDL Document:
--------------------------------------

1. **<definitions>**: The root element of a WSDL document, which contains all the other components.
   
2. **<types>**: Specifies the data types used by the web service. It often references XML Schema (XSD) to define complex types.
   
3. **<message>**: Describes the data being exchanged between the client and the web service. Each message consists of one or more parts, which define the data elements.
   
4. **<portType>**: Defines a set of operations that the web service supports. Each operation corresponds to a specific function the web service provides.
   
5. **<binding>**: Describes how the web service operations will be transmitted, specifying the protocol (e.g., SOAP, HTTP) and message format.
   
6. **<service>**: Specifies the endpoint URL where the web service can be accessed.

Example of a Simple WSDL:
----------------------------

```xml
<?xml version="1.0" encoding="UTF-8"?>
<definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
             xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema"
             targetNamespace="http://example.com/webservice">
             
  <types>
    <xsd:schema targetNamespace="http://example.com/webservice">
      <xsd:element name="getUser" type="xsd:int"/>
    </xsd:schema>
  </types>

  <message name="GetUserRequest">
    <part name="userId" element="xsd:int"/>
  </message>

  <message name="GetUserResponse">
    <part name="userDetails" element="xsd:string"/>
  </message>

  <portType name="UserService">
    <operation name="getUser">
      <input message="GetUserRequest"/>
      <output message="GetUserResponse"/>
    </operation>
  </portType>

  <binding name="UserServiceSOAP" type="tns:UserService">
    <soap:binding style="rpc" transport="http://schemas.xmlsoap.org/soap/http"/>
    <operation name="getUser">
      <soap:operation soapAction="http://example.com/getUser"/>
      <input>
        <soap:body use="encoded" namespace="http://example.com/webservice"/>
      </input>
      <output>
        <soap:body use="encoded" namespace="http://example.com/webservice"/>
      </output>
    </operation>
  </binding>

  <service name="UserService">
    <port name="UserServicePort" binding="tns:UserServiceSOAP">
      <soap:address location="http://example.com/webservice"/>
    </port>
  </service>

</definitions>
