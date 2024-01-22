---
# Title, summary, and page position.
linktitle: Coding guidelines
summary: Learn the coding styles and good coding practices for contributing code to CemrgApp.
weight: 2
icon: book
icon_pack: fas

# Page metadata.
title: Coding Style and Good Practices
date: '2018-09-09T00:00:00Z'
type: book # Do not modify.
---


Programming style, also known as code style, is a set of rules or guidelines used when writing the source code for a computer program. It is often claimed that following a particular programming style will help programmers read and understand source code, and help with preventing unwanted errors.

CemrgApp expects our beloved contributors to adhere to the following style when coding for the platform.

# Whitespaces and Indentation

Blank lines should be used to separate logical groupings of code. Be consistent with choice of tabs or spaces for indenting. Aim for best readability. Primary importance is that code is easy to read and logically follow:

* Opening curly braces should go on the same line as the corresponding statement.
* A single space should be used between most reserved words, identifiers and symbols.
* Minimum of one blank lines should be used to separate functions and other blocks of code.
* Keep line lengths to 80 characters or less where appropriate.
* Adjust tab sizing to four spaces.
* BE CONSISTENT!

# Commenting

Comments improve program readability. As with naming conventions, it is important to use correct English spelling. Be consistent with your use of commenting syntax, for example:

* // This is a line comment.
* /* This is a block comment for more than one line. */
* Start each file with a comment at the top describing its contents.
* Start each class with an accompanying comment that describes what it is for.
* Variable names should be descriptive enough not to require commenting.
* Only comment tricky, non-obvious, interesting or important parts.

# Cheat Sheet

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

**Reference:** Based on Monash University programming style guidelines.