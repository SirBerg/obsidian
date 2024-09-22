<sub class="descriptionSection">19-09-2024 03:43:pm // #C // [[Programmierung]]</sub>
____
Aufgabe war es eigentlich, nur Klammerrechnung mit + und - zu implementieren, das programm hier kann auch auf mal und geteilt achten.
```cpp
#include <iostream>  
#include <stack>  
using namespace std;  
  
int doMathFromString(string userInputString) {  
    //this function ranks the operations and then does the math in a string of only numbers and operators, it expects every parenthesis to be removed from the string  
    string inputString = userInputString;  
    cout << "Doing math in string: " << inputString << endl;  
    int result = 0;  
  
    const string privilegedOperators[2] = {"*", "/"};  
    auto toDoStack = stack<string>();  
    int counter = 0;  
    int skipCounter = 0;  
    //loop over every character in the string and do the math  
    for(const char currChar : inputString) {  
  
        //we do this, so we can skip the next number in the string, because we've already used it (in the privileged math operations, for example)  
        if(skipCounter != 0) {  
            cout << "Skipping this char, as we've already used it in a privileged math operation" << endl;  
            skipCounter--;  
            counter++;  
            continue;  
        }  
        //convert the char to a string  
        const string currentChar = string(1, currChar);  
  
        if(currentChar == "+" || currentChar == "-") {  
            //we just add this to the stack, because we need to do the math in order of operations  
            toDoStack.push(currentChar);  
        }  
        else if(currentChar == "*" || currentChar == "/") {  
            //in this case, we do the math instantly, because we need to do the math in order of operations  
            //we take the number before the operator from the stack and the number after the operator from the string            //then we do the math and replace the number on top of the stack with the result            const int numberBeforeOperator = stoi(toDoStack.top());  
  
            //because we're doing this char by char, we need to check if the number after the operator has more than one digit  
            //we create a substring at the current position and loop over the string until we find an operator,            //and then we remove that number from the input string, so we don't use it again            string numberAfterOperator = "";  
            int counterNewNumber = 0;  
            for(const char newChar : inputString.substr(inputString.find(currentChar)+1)) {  
                const string newCharString = string(1, newChar);  
                if(newCharString == "+" || newCharString == "-" || newCharString == "*" || newCharString == "/") {  
                    break;  
                }  
                numberAfterOperator += newChar;  
                counterNewNumber++;  
            }  
  
            //we set the skipCounter to the length of the number we just found, so we don't use it again  
            cout << "Setting SkipCounter to: " << counterNewNumber << endl;  
            skipCounter = counterNewNumber;  
  
            //pop the first number that we just used to do math from the stack  
            toDoStack.pop();  
  
            //now we do the math  
            if(currentChar == "*") {  
                toDoStack.push(to_string(numberBeforeOperator * stoi(numberAfterOperator)));  
            } else {  
                toDoStack.push(to_string(numberBeforeOperator / stoi(numberAfterOperator)));  
            }  
  
            cout << "Result of privileged math operation: " << toDoStack.top() << endl;  
        }  
        else {  
            //this means we've found a number and need to add it to the stack  
            //check if the last number in the stack is a number, if it is, we need to append the current number to it  
            if(toDoStack.empty()) {  
                toDoStack.push(currentChar);  
                counter++;  
                continue;  
            }  
  
            if(toDoStack.top() == "+" || toDoStack.top() == "-" || toDoStack.top() == "*" || toDoStack.top() == "/") {  
                toDoStack.push(currentChar);  
            } else {  
                //if the last number in the stack is a number, we need to append the current number to it  
                toDoStack.top() += currentChar;  
            }  
        }  
        counter++;  
    }  
    //now we reverse the stack so we do the math in order of operations  
    auto reversedStack = stack<string>();  
    while(!toDoStack.empty()) {  
        reversedStack.push(toDoStack.top());  
        toDoStack.pop();  
    }  
  
    //corrects the stack so we can do the math in order of operations  
    if(reversedStack.top() != "-") {  
        reversedStack.push("+");  
    }  
  
    while(!reversedStack.empty()) {  
        if(reversedStack.top() == "+") {  
            //pop the operator from the stack  
            reversedStack.pop();  
  
            cout << "Adding " << reversedStack.top() << " to" << result << endl;  
            result += stoi(reversedStack.top());  
        } else if(reversedStack.top() == "-") {  
            //pop the operator from the stack  
            reversedStack.pop();  
  
            cout << "Subtracting " << reversedStack.top() << " from" << result << endl;  
            result -= stoi(reversedStack.top());  
        }  
  
        //after this, we can pop the number from the stack  
        reversedStack.pop();  
    }  
    cout << "Result of math operations: " << result << endl;  
    return result;  
}  
  
int parseString(string inputString) {  
    //this function cleans up the string and removes all the spaces and parenthesis  
    int counter = 0;  
    cout << "Got new string to parse: " << inputString << endl;  
    for(const char currChar : inputString) {  
  
        const string currentChar = string(1, currChar);  
        if(currentChar == "(") {  
            //this means we've found a parenthesis and need to do the math inside of it first  
            //we do this by following the string until we find the closing parenthesis and store the new string in a variable            //then we call the parseString function again with the new string to handle any new parenthesis in this one  
            string newString = "";  
            int parenthesisCounter = 0;  
            int charCounter = 0;  
            for(const char newChar : inputString.substr(counter+1)) {  
                const string newCharString = string(1, newChar);  
                if(newCharString == "(") {  
                    parenthesisCounter++;  
                } else if(newCharString == ")") {  
                    //we break here, because we've found the closing parenthesis of the current one that we want to pass on to the parseString function  
                    if(parenthesisCounter == 0) {  
                        break;  
                    } else {  
                        parenthesisCounter--;  
                    }  
                }  
                newString += newChar;  
                charCounter++;  
            }  
  
            //we call the parseString function again with the new string  
            //this is expected to be the result of the math operations inside of it, so we can then replace the parenthesis with the result            const int resultInteger = parseString(newString);  
            cout << "Result of parenthesis: " << resultInteger << endl;  
            //we replace the parenthesis with the result of the math operations inside of it  
            inputString.replace(counter, charCounter+2, to_string(resultInteger));  
            cout << "New string: " << inputString << endl;  
  
            continue;  
        }  
  
        if(currentChar == " ") {  
            //we skip spaces  
            continue;  
        }  
        //if none of the If statements hit, we don't need to do anythign  
        counter++;  
    }  
  
    cout << "String after parsing: " << inputString << endl;  
    //now we return the result of the math operations in the string  
    int result = doMathFromString(inputString);  
    return result;  
}  
  
int main() {  
    const string mathString = "(10+5*(20+2))/3+5";  
    int result = parseString(mathString);  
    cout << "The Final Result is:" << result << endl;  
    return 0;  
}
```