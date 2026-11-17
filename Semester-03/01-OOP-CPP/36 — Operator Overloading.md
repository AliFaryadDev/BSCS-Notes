# Operaror Overloading
> **Subject: OOP** | **Language: C++**
## 📄 Important Point
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Complete Working Flow](#complete-working-flow)
- [Complete Program](#complete-program)
- [Output](#output)
- [Conclusion](#conclusion)

## Introduction
Operator overloading is an important feature of C++ that allows existing operators to work with user-defined data types. It enables operators to perform specific operations on objects of a class. 💻
## Definition
  > Operator overloading is a feature of C++ that allows programmers to give additional meanings to existing operators so they can perform operations on objects of user-defined data types.
## Purpose
  It makes code clear and readable.
## Syntax
```cpp
  return_type operator symbol (parameter) {
  // Logic
  }
```
## Example
```cpp
  Number operator+(Number obj) {
    // Add two objects
  }
  ```
## Working
### Step 1: Object Creation
<br>

**Code**
  
```cpp
  int main() {
    Box b1, b2, sum;
  }                  
    
```
<br>

**Diagram**



  ```mermaid
     flowchart TD
     A["Box Class"] -->
     B["Box b1"]
     A["Box Class"] -->
     C["Box b2"]
     A["Box Class"] -->
     D["Box sum"]
```
<br>

**Code Mapping**
```mermaid
flowchart LR
    A["Box"] --> B["Class Name"]
    C["b1"] --> D["Object 1"]
    E["b2"] --> F["Object 2"]
    G["sum"] --> H["Object 3"]
 ```
<br>

**💡 Takeaway**
  > One class can be used to create multiple objects.

### Step 2: Assigning Values to Objects
<br>

**code**
```cpp
b1.item = 10;
b2.item = 20;
```
<br>

**Diagram**
```mermaid
flowchart TD
    A["Box b1"] --> B["item = 10"]
    C["Box b2"] --> D["item = 20"]

    B --> E["Values stored in objects"]
    D --> E
  ```
  <br>
  
**Code Mapping**
  ```mermaid
flowchart TD
    A["Box b1, b2"] --> B["Box"]
    A --> C["b1, b2"]

    B --> D["Class / User-defined Data Type"]
    C --> E["Objects / Instances"]

    F["b1.value = 10"] --> G["b1 = Object"]
    F --> H[". = Member Access Operator"]
    F --> I["value = Data Member"]
    F --> J["10 = Assigned Value"]
  ```
  <br>
  
**💡 Takeaway**
  > Each object maintains its own copy of data members, which can be initialized or modified independently using the dot (.) operator.
### Step 3: Operator Function Execution
<br>

**Code**


```cpp
Box operator+(Box obj) {
    Box temp;
    temp.value = value + obj.value;
    return temp;
}
```
<br>

**Diagram**
```mermaid
   flowchart TD
    A["operator+() Function"] --> B["Receives an object parameter: obj"]
    B --> C["Creates a temporary object: temp"]
    C --> D["Prepares to perform addition"]

  ```
<br>

**Code Mapping**
```mermaid
flowchart TD
    A["Box operator+(Box obj)"] --> B["Box"]
    A --> C["operator+"]
    A --> D["(Box obj)"]

    B --> E["Return Type"]
    C --> F["Overloaded Operator Function"]
    D --> G["Parameter: obj (Object)"]

    H["Box temp;"] --> I["Creates a temporary object"]
    J["return temp;"] --> K["Returns the temporary object"]
  ```
  <br>

  **💡 Takeaway**
  >The operator function receives an object as a parameter, creates a temporary object, and returns it after performing the operation.
### Step 4: Performing Addition
<br>

**Code**
```cpp
temp.value = value + obj.value;
```
<br>

**Diagram**
```mermaid
flowchart TD
    A["value = 10"] --> C["Addition (+)"]
    B["obj.value = 20"] --> C
    C --> D["10 + 20 = 30"]
    D --> E["temp.value = 30"]
  ```
<br>

**Code Mapping**
```mermaid
flowchart TD
    A["temp.value = value + obj.value"] --> B["value"]
    A --> C["obj.value"]
    A --> D["temp.value"]

    B --> E["b1 object's data member"]
    C --> F["Passed object's data member"]
    D --> G["Stores the addition result"]
  ```
  <br>

**💡 Takeaway**
  >The operator function adds the data member values of both objects and stores the result in the temporary object.
### Step 5: Returning the result
<br>

**Code**
```cpp 
return temp;
```
<br>

**Diagram**
```mermaid
flowchart TD
    A["Temporary Object: temp"] --> B["value = 30"]
    B --> C["return temp"]
    C --> D["Object returned from operator+()"]
  ```

<br>

**Code Mapping**
```mermaid
flowchart TD
    A["return temp"] --> B["return"]
    A --> C["temp"]

    B --> D["Returns an object"]
    C --> E["Temporary object"]
    E --> F["Contains value = 30"]
   ```
   <br>

**Takeaway 💡**
   >The operator function returns the temporary object containing the addition result.

### Step 6: Storing the Returned Object in sum
<br>

**Code**
```cpp
sum = b1 + b2;
```
<br>

**Diagram**
```mermaid
flowchart TD
    A["b1.value = 10"] --> C["operator+()"]
    B["b2.value = 20"] --> C
    C --> D["temp.value = 30"]
    D --> E["return temp"]
    E --> F["sum = returned object"]
    F --> G["sum.value = 30"]
  ```
  <br>

**Code Mapping**
  ```mermaid
  flowchart TD
    A["sum = b1 + b2"] --> B["sum"]
    A --> C["b1 + b2"]

    B --> D["Receiving Object"]
    C --> E["Calls overloaded operator+()"]
    E --> F["Returns temporary object"]
    F --> G["Assigns returned object to sum"]
   ```
   <br>

**💡Takeaway**
   > The returned object is assigned to sum, which now contains value = 30.
### Step 7: Displaying the Result
<br>

**Code**
```cpp
cout << "Sum = " << sum.value;
```
<br>

**Diagram**
```mermaid
flowchart TD
    A["sum Object"] --> B["value = 30"]
    B --> C["cout << sum.value"]
    C --> D["Output: Sum = 30"]
  ```

  <br>

  **Code Mapping**
 ```mermaid 
  flowchart TD
    A["cout << Sum = << sum.value"] --> B["cout"]
    A --> C["sum.value"]
    B --> D["Displays output"]
    C --> E["Accesses value of sum object"]
    E --> F["value = 30"]
  ```
  <br>

  **💡 Takeaway**
  > The cout statement displays the result stored in the sum object.

## Complete Working Flow

<br>

**Diagram**
```mermaid
flowchart TD
    A["Start: main()"] --> B["Create Objects<br/>Box b1, b2, sum"]
    B --> C["Assign Values<br/>b1.value = 10<br/>b2.value = 20"]
    C --> D["Call Operator Function<br/>sum = b1 + b2"]
    D --> E["Pass b2 to obj"]
    E --> F["Create Temporary Object<br/>Box temp"]
    F --> G["Perform Addition<br/>value + obj.value"]
    G --> H["10 + 20 = 30"]
    H --> I["Store Result<br/>temp.value = 30"]
    I --> J["Return temp Object"]
    J --> K["Assign Returned Object<br/>sum = temp"]
    K --> L["Display sum.value"]
    L --> M["Output: Sum = 30"]
    M --> N["End"]
  ```
  
## Complete Program
```cpp
  #include <iostream>
using namespace std;

class Box {
public:
    int value;

    Box operator+(Box obj) {
        Box temp;
        temp.value = value + obj.value;
        return temp;
    }
};

int main() {
    Box b1, b2, sum;

    b1.value = 10;
    b2.value = 20;

    sum = b1 + b2;

    cout << "Sum = " << sum.value;

    return 0;
}
 ```
## Output
> Sum = 30

<br>

## Conclusion
Operator overloading allows existing C++ operators to work with user-defined data types. It makes objects easier to use by defining how operators behave with them.

<br>
<br>


---

> **Muhammad Ali** — *BSCS (Computer Science)*  
> *"Learn with Purpose. Build with Knowledge."*

