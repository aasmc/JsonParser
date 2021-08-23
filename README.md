# Simple Json Parser

Accepts any input stream with json text and parses it by creating a root Json::Document.

```c++
const auto document = Json::Load(std::cin);    
```

To obtain a root node of the Json call

```c++
const auto &rootDoc = document.GetRoot();
```

From a Json node you can obtain:

#### Map

```c++
const auto &inputMap = rootDoc.AsMap();
```

#### Array

```c++
const auto &inputArr = rootDoc.AsArray();
```

#### bool

```c++
const auto &inputBool = rootDoc.AsBool();
```

#### double

```c++
const auto &inputDouble = rootDoc.AsDouble();
```

#### int

```c++
const auto inputInt = rootDoc.AsInt();
```

#### string

```c++
const auto &inputString = rootDoc.AsString();
```

To get a node at certain key in a Json::Dict (std::map<std::string, Json::Node>) call

```c++
auto node = inputMap.at("key");
```

You can print the Json::Document by calling:

```c++
    const auto doc = Json::Load(std::cin);
    Print(doc);
```