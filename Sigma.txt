#include <iostream>
#include <sstream>
#include <string>
#include <iomanip>
using namespace std;
string stringdata;
struct SensorData {
string id = "385635";
int error_code = 9;
int hours = 2;
int minutes = 30;
int seconds = 12;
float altitude= 120.8276;
float longitude = -7.795580;
float latitude = 110.369492;
};
SensorData sensor;
void sensordata(){
    stringstream sensordata;
	(sensordata<<sensor.id<< setprecision(7)<<";"<<sensor.error_code<<";"<<sensor.hours<<";"<<sensor.minutes<<";"
	<<sensor.seconds<<";"<<sensor.altitude<<";");
    sensordata<<setprecision(6)<<fixed<<sensor.longitude<<";"<<sensor.latitude<<";";
    stringdata = sensordata.str();
}
int main (){
    sensordata();
	cout<<"concatenate string: string = "<<"\""<<stringdata<<"\""<<endl;
    system("pause");
    return 0;
} 