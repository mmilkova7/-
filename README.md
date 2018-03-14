#include<iostream>
#include<cmath>
using namespace std;
class Point
{
private:
  float x;
  float y;
public:
  void setX(float a)
  {
   x=a;
  }
  float getX()
{
  return x;
}
  void setY(float a)
  {
   y=a;
  }
  float getY()
{
  return y;
}
  void info()
{
  cout << "x" << x << "y" << y << endl;
}
float dist (Point p)
{
  float d=sqrt((x-p.getX())*(x-p.getX())+(y-p.getY())*(y-p.getY()));
  return d;
}
};
int main()
{
  Point p1,p2;
  p1.setX(20);
  p1.setY(3.2);
  p1.info();
  p2.setX(14);
  p2.setY(2.3);
  p2.info();
  float r=p1.dist(p2);
  cout << "Dist=" << r << endl;
}
