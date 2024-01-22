---
title: Takeaways
linktitle: Takeaways
type: book
date: '2019-05-05T00:00:00+01:00'

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

* Use **camelCase** style for identifiers, parameter names.
* Use opening **braces on the same line** as the corresponding statement.
* Use **single space** between most reserved words, identifiers and symbols.
* Use **single blank line** between methods.
* Use **braces** for if/else/loop branches, even when there is a single statement.
* Use **4 spaces** or **4 spaced tabs** for indentation showing block structure.
* Use **doc comments** for class explanation.
* Use internal **comments** where necessary to clarify intent of code.

# A Correctly Styled Example

```
/**
 * Explanation of class usage.
 * This is a doc comment for the explanation of the class.
 * 
 * @author Your Name
 */
class AnExampleWithGUI {

    //This is needed for all Qt objects that should have a Qt meta-object
    Q_OBJECT

public:

    static const std::string VIEW_ID;
    virtual void CreateQtPartControl(QWidget *parent);

private:

    void ExampleFunction(int paramName);
}
```
```
void AnExampleWithGUI::ExampleFunction(int paramName) {
    
    //Opening braces go on the same line, separated by a single space
    if (paramName == 0) {
        std::cout << "We love CemrgApp!" << std::endl;
    } else {
        std::cout << "We still love CemrgApp!" << std::endl;
    }

    //Very important comment
    vtkSmartPointer<vtkPolyData> sensibleParamName;
}
```

# A Poorly Styled Example
```
void AClass::Function1(int abc)
{if(abc==0){std::cout<<"We don't love CemrgApp!"<<std::endl;}
  vtkSmartPointer<vtkPolyData> var2;
}
```