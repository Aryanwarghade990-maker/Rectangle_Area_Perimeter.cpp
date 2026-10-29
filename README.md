# Rectangle_Area_Perimeter.cpp 
#include <iostream>
using namespace std;

class Rectangle {
private:
    float length;
    float breadth;

public:
    // Member function defined inside class
    void setDimensions(float l, float b) {
        length = l;
        breadth = b;
    }
    
    // Member function declared inside class
    float calculateArea();
    float calculatePerimeter();
    void display();
};

// Member function defined outside class using scope resolution operator
float Rectangle::calculateArea() {
    return length * breadth;
}

float Rectangle::calculatePerimeter() {
    return 2 * (length + breadth);
}

void Rectangle::display() {
    cout << "Length: " << length << endl;
    cout << "Breadth: " << breadth << endl;
    cout << "Area: " << calculateArea() << endl;
    cout << "Perimeter: " << calculatePerimeter() << endl;
}

int main() {
    Rectangle rect;
    float l, b;
    
    cout << "Enter length and breadth of rectangle: ";
    cin >> l >> b;
    
    rect.setDimensions(l, b);
    rect.display();
    
    return 0;
}
