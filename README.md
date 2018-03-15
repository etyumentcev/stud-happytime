# stud-happytime

#pragma once
#include <string> 
using namespace std;
class Fuzzy
{
	string name;
	int colour;
	Coordinates XY; // класс-наследник, с координатами пушистика, хранит в себе местоположения платформ, монстров и пиццы.
	int life;
	Monster evil; // класс-наследник, с монстрами , хранит в себе булевые переменные , связанные с координатами монстриков
	//  когда пушистик попадает на координату с монстриком , то булевая переменная берет значение истина , и ведется 
	// и введется счетчик сколько раз булевая перменная была истиная, отнимает жизнь у пушистика
public:
	
	Fuzzy (Fuzzy const & other); 
	Fuzzy operator=(Fuzzy const & other); 
	Coordinates XY *  Going(); // движение по платформам, исользуется координата, на которой в данный момент пушистик
	int Life(Coordinates XY *); // смотрит какая координата, сверяет с булевой переменной и в случае истины отнимает жизнь
	int Pizza(Coordinates XY *); // смотрит какая координата, сверяет с булевой переменной и увеличивает кол-во пицц
	virtual ~Fuzzy();
};

