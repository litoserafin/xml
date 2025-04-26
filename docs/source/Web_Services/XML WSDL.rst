XML WSDL (Web Services Description Language)
=============================================

**WSDL** (Web Services Description Language) is an **XML-based** format used to **describe** the operations, messages, and protocols a **web service** offers.  
It acts like a **contract** between the service provider and consumers, making integration clear and structured.

---

Key Components of a WSDL Document
---------------------------------

1. **<definitions>**:  
   - The root element of a WSDL document.  
   - Contains namespaces and all service descriptions.

2. **<types>**:  
   - Defines the data types (schemas) the web service uses.  
   - Usually based on **XSD** (XML Schema Definition).

3. **<message>**:  
   - Describes the input and output messages used by operations.  
   - Each message can have multiple **parts** (parameters).

4. **<portType>**:  
   - Defines a **set of operations** that the service supports.  
   - Each operation specifies input and output messages.

5. **<binding>**:  
   - Specifies the **communication protocol** (e.g., SOAP, HTTP) and **data format** details.

6. **<service>**:  
   - Defines the **endpoint address** (URL) where the service can be accessed.

---

Simple Example of a WSDL
------------------------

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8"?>
   <definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
                xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"
                xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                xmlns:tns="http://example.com/webservice"
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
         <input message="tns:GetUserRequest"/>
         <output message="tns:GetUserResponse"/>
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

---

Why Use WSDL?
-------------

✅ **Standardization**: Clearly defines service operations and data types.  
✅ **Automation**: Allows automatic generation of client/server code using tools.  
✅ **Interoperability**: Facilitates communication between systems built on different technologies.  
✅ **Formal Contract**: Reduces integration errors by strictly defining expected requests and responses.

---

📌 **Tip**: In real-world projects,
