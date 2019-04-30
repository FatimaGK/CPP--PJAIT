# CPP--PJAIT
C++ Taks from pjait
//task 9 
example 1
#include <iostream>
#include <cmath>

class Point {
	double x, y;
public:
	Point() {
		x = 0;
		y = 0;
	}
	Point(double s) {
		x = s;
		y = s;
	}
	Point(double x, double y) {
		this->x = x;
		this->y = y;
	}

	double getX() const {
		return x;
	}
	double getY() const {
		return y;
	}
	Point& setX(double xx) {
		x = xx;
		return *this;
	}
	Point& setY(double yy) {
		y = yy;
		return *this;
	}
	Point& transX(double dx) {
		x = x + dx;
		return *this;
	}
	Point& transY(double dy) {
		y = y + dy;
		return*this;
	}
	Point& transXY(double dx, double dy) {
		x = x + dx;
		y = y+ dy;
		return *this;

	}
	static double dist(const Point& p, const Point& q) {
		//distance??
		const double dx = p.x - q.x;
		const double dy = p.y - q.y;
	
		return sqrt(dx*dx + dy * dy);
	}
};

int main() {
	Point p;
	Point q(1);
	Point r(1, 2);
	p.transXY(5, 6);
	q.transX(-1).transY(-1).transXY(2, 2);
	r.setX(10).transY(-8);
	std::cout << Point::dist(p, q) << std::endl;
	std::cout << Point::dist(p, r) << std::endl;
	system("pause");
}
