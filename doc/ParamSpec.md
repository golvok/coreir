

//4 tiers of parameter types
ParamTypeT1 = "Bool"
        | ["BitVector" <N>]
        | "String"
        | "Int" //Is this any different than BitVector<32>
        | "Float" //should this be included?

ParamTypeT2 = "CoreIRType"
        | "Module"
        | //"Generator" //This would be a super cool extra feature

ParamTypeT3 = "json" //Arbitrary Json

ParamTypeT4 = ["json-schema", jsonschema]

ParamType = ParamTypeT1
          | ParamTypeT2
          | ParamTypeT3
          | ParamTypeT4

Params = {<field>:ParamType,...}


ValueT1 = <true|false>
        | <number>
        | <string>
        | [<numbits>, <radix>, <value-string>]

ValueT2 = CoreIRType
        | [Namespaces, <module-name>]


CoreIRType = "BitIn" 
           | "Bit" 
           | ["Array", <N>, Type] 
           | ["Record", [[<key>,Type],... ] 

Namespaces = [<namespace>, <subnamespace>, ...]

Values = {<field>:Value,...}


