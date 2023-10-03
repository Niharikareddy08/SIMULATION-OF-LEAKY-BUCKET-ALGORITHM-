#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<GL/glut.h>
#include <time.h>
#include<math.h>
void drawtext();
void no_overflow();
void overflow();
void drawoverflow();
void delay(unsigned int mseconds)
{
	clock_t goal = mseconds + clock();
	while (goal > clock())
		;
}
void drawPoint(int x, int y)
{
	glPointSize(25.0);
	
	glBegin(GL_POINTS);
	glVertex2i(x, y);
	glEnd();
}
void translatePoint(int px, int py, int tx, int ty)
{
	
	int fx = px, fy = py;
	for(int i=0;i<50;i++){
		glClear(GL_COLOR_BUFFER_BIT);
		no_overflow();
		// update
		px = px - tx;
		py = py - ty;

		// check overflow to keep point in screen
		if (px > 500 || px < 0 || py > 500 || py < 0) {
			px = fx;
			py = fy;
		}
glColor3f(0.0f, 0.0f, 1.0f);
		drawPoint(px, py); // drawing the point

		glFlush();
		// creating a delay
		// so that the point can be noticed
		delay(40000);
	}
}

void translatePoints(int px, int py, int tx, int ty)
{
drawoverflow();
	int fx = px, fy = py;
	for(int i=0;i<15;i++){
		glClear(GL_COLOR_BUFFER_BIT);
		overflow();
		// update
		px = px - tx;
		py = py - ty;

		// check overflow to keep point in screen
		if (px > 500 || px < 0 || py > 500 || py < 0) {
			px = fx;
			py = fy;
		}
		glColor3f(1.0f, 0.0f, 0.0f);
		drawPoint(px, py); // drawing the point

		glFlush();
		// creating a delay
		// so that the point can be noticed
		delay(40000);
	}
}
void bytes(int i)
{
	char fb[]="4 Bytes outputted";
	glRasterPos2f(80.0,210.0-i);
	for(i=0;fb[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fb[i]);
}
void bytes_success(int i)
{
char fs[]="Bucket output successful";
	glRasterPos2f(80.0,170.0-i);
	for(i=0;fs[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fs[i]);
}

void drawtext()
{
  int i;
	glColor3f(0.0,0.0,0.0);
	char d[]="Data rate is 7    5    4";
	glRasterPos2f(70.0,270.0);
	for(i=0;d[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,d[i]);

	char f[]="Bucket size:8";
	glRasterPos2f(70.0,250.0);
	for(i=0;f[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,f[i]);

	char fr[]="output rate:4";
	glRasterPos2f(70.0,230.0);
	for(i=0;fr[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fr[i]);
	bytes(0);
	char fl[]="Last 3 bytes sent";
	glRasterPos2f(80.0,190.0);
	for(i=0;fl[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fl[i]);
	bytes_success(0);
	bytes(60);
char fy[]="Last 1 byte sent";
	glRasterPos2f(80.0,130.0);
	for(i=0;fy[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fy[i]);
		bytes_success(60);
		bytes(120);
		bytes_success(100);
		char fd[]="No.of packets sent=5";
	glRasterPos2f(80.0,50.0);
	for(i=0;fd[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fd[i]);
}

void drawoverflow()
{
  int i;
	glColor3f(0.0,0.0,0.0);
	char d[]="Data rate is 10  4";
	glRasterPos2f(70.0,270.0);
	for(i=0;d[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,d[i]);

	char f[]="Bucket size:8";
	glRasterPos2f(70.0,250.0);
	for(i=0;f[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,f[i]);

	char fr[]="output rate:4";
	glRasterPos2f(70.0,230.0);
	for(i=0;fr[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fr[i]);
	char fl[]="Packet overflow";
	glRasterPos2f(70.0,210.0);
	for(i=0;fl[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fl[i]);
		
	char fb[]="4 Bytes outputted";
	glRasterPos2f(70.0,190.0);
	for(i=0;fb[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,fb[i]);
	char dd[]="No.of packets sent=1";
	glRasterPos2f(70.0,170.0);
	for(i=0;dd[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,dd[i]);
		}
	
void no_overflow()
{
glClear(GL_COLOR_BUFFER_BIT);
	glPointSize(3.0);
	glColor3f(0.3,0.0,0.0);
	glLineWidth(3);
	
	

	//tap in algo.
	glColor3f(0.3,0.1,0.2);
	glBegin(GL_LINE_STRIP);	
	glVertex2i(294,365);
	glVertex2i(294,394);
	glVertex2i(295,395);
	glVertex2i(295,400);
	glVertex2i(275,400);
	glVertex2i(275,415);
	glVertex2i(285,415);
	glVertex2i(285,420);
	glVertex2i(280,450);
	glVertex2i(245,450);
	glVertex2i(240,425);
	glVertex2i(240,420);
	glVertex2i(250,420);
	glVertex2i(250,400);
	glVertex2i(230,400);
	glVertex2i(230,380);
	glVertex2i(250,380);
	glVertex2i(250,375);
	glVertex2i(275,375);
	glVertex2i(275,380);
	glVertex2i(280,380);
	glVertex2i(280,365);
	//glVertex2i(194,165);
	glEnd();
	
	//tap down
	glBegin(GL_LINE_LOOP);
	glVertex2i(294,365);
	glVertex2i(294,360);
	glVertex2i(280,360);
	glVertex2i(280,365);
	glEnd();
	

	
	
	//bucket word
	glColor3f(0.0,0.0,0.0);
	char vb[]="Bucket";
	glRasterPos2f(320.0,230.0);
	for(int j=0;vb[j]!='\0';j++)
	glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vb[j]);
	
	//bucket
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(258,250);
	glVertex2i(270,200);
	glVertex2i(300,200);
	glVertex2i(310,250);
	glEnd();
	
	//break
	glPointSize(10.0);
	glBegin(GL_POINTS);
	glColor3f(0.8,1.0,0.8);
	glVertex2i(285,200);
	glEnd();
	
	
	//network word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char vn[]="Network";
	glRasterPos2f(350.0,60.0);
	for(int j=0;vn[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vn[j]);
	
	//Network
	glColor3f(0.3,0.0,0.0);
	glBegin(GL_LINE_STRIP);
	glVertex2i(340,70);
	glVertex2i(320,100);
	glVertex2i(260,100);
	glVertex2i(240,60);
	glVertex2i(300,35);
	glVertex2i(340,70);
	glVertex2i(260,100);
	glVertex2i(300,35);
	glVertex2i(320,100);
	glVertex2i(240,60);
	glVertex2i(340,70);
	glEnd();
	//host word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char v[]="Host";
	glRasterPos2f(170.0,400.0);
	for(int j=0;v[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,v[j]);
	//computer word
	char vc[]="Computer";
	glRasterPos2f(170.0,380.0);
	for(int j=0;vc[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vc[j]);
	//glColor3f(0.0,0.0,0.0);
	glBegin(GL_LINE_LOOP);
	glVertex2i(228,450);
	glVertex2i(228,350);
	glVertex2i(160,350);
	glVertex2i(160,450);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(223,440);
	glVertex2i(223,360);
	glVertex2i(165,360);
	glVertex2i(165,440);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(194,350);
	glVertex2i(184,335);
	glVertex2i(204,335);
	glEnd();
	
	drawtext();
	glFlush();
	
}
void overflow()
{
glClear(GL_COLOR_BUFFER_BIT);
	glPointSize(3.0);
	glColor3f(0.3,0.0,0.0);
	glLineWidth(3);
	
	

	//tap in algo.
	glColor3f(0.3,0.1,0.2);
	glBegin(GL_LINE_STRIP);	
	glVertex2i(294,365);
	glVertex2i(294,394);
	glVertex2i(295,395);
	glVertex2i(295,400);
	glVertex2i(275,400);
	glVertex2i(275,415);
	glVertex2i(285,415);
	glVertex2i(285,420);
	glVertex2i(280,450);
	glVertex2i(245,450);
	glVertex2i(240,425);
	glVertex2i(240,420);
	glVertex2i(250,420);
	glVertex2i(250,400);
	glVertex2i(230,400);
	glVertex2i(230,380);
	glVertex2i(250,380);
	glVertex2i(250,375);
	glVertex2i(275,375);
	glVertex2i(275,380);
	glVertex2i(280,380);
	glVertex2i(280,365);
	//glVertex2i(194,165);
	glEnd();
	
	//tap down
	glBegin(GL_LINE_LOOP);
	glVertex2i(294,365);
	glVertex2i(294,360);
	glVertex2i(280,360);
	glVertex2i(280,365);
	glEnd();
	

	
	
	//bucket word
	glColor3f(0.0,0.0,0.0);
	char vb[]="Bucket";
	glRasterPos2f(320.0,230.0);
	for(int j=0;vb[j]!='\0';j++)
	glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vb[j]);
	
	//bucket
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(258,250);
	glVertex2i(270,200);
	glVertex2i(300,200);
	glVertex2i(310,250);
	glEnd();
	
	//break
	glPointSize(10.0);
	glBegin(GL_POINTS);
	glColor3f(0.8,1.0,0.8);
	glVertex2i(285,200);
	glEnd();
	
	
	//network word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char vn[]="Network";
	glRasterPos2f(350.0,60.0);
	for(int j=0;vn[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vn[j]);
	
	//Network
	glColor3f(0.3,0.0,0.0);
	glBegin(GL_LINE_STRIP);
	glVertex2i(340,70);
	glVertex2i(320,100);
	glVertex2i(260,100);
	glVertex2i(240,60);
	glVertex2i(300,35);
	glVertex2i(340,70);
	glVertex2i(260,100);
	glVertex2i(300,35);
	glVertex2i(320,100);
	glVertex2i(240,60);
	glVertex2i(340,70);
	glEnd();
	//host word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char v[]="Host";
	glRasterPos2f(170.0,400.0);
	for(int j=0;v[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,v[j]);
	//computer word
	char vc[]="Computer";
	glRasterPos2f(170.0,380.0);
	for(int j=0;vc[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vc[j]);
	//glColor3f(0.0,0.0,0.0);
	glBegin(GL_LINE_LOOP);
	glVertex2i(228,450);
	glVertex2i(228,350);
	glVertex2i(160,350);
	glVertex2i(160,450);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(223,440);
	glVertex2i(223,360);
	glVertex2i(165,360);
	glVertex2i(165,440);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(194,350);
	glVertex2i(184,335);
	glVertex2i(204,335);
	glEnd();
	
	drawoverflow();
	glFlush();
	
}
void display1()//Algorithm
{

	glClear(GL_COLOR_BUFFER_BIT);
	glPointSize(3.0);
	glColor3f(0.3,0.0,0.0);
	glLineWidth(3);
	glBegin(GL_LINE_STRIP);
	{
	glVertex2i(15,270);
	glVertex2i(150,270);
	glVertex2i(150,10);
	glVertex2i(15,10);
	glVertex2i(15,270);
	glEnd();
	}
	//tap side pic
	glColor3f(0.3,0.1,0.2);
	glBegin(GL_LINE_STRIP);	
	glVertex2i(94,165);
	glVertex2i(94,194);
	glVertex2i(95,195);
	glVertex2i(95,200);
	glVertex2i(75,200);
	glVertex2i(75,215);
	glVertex2i(85,215);
	glVertex2i(85,220);
	glVertex2i(80,250);
	glVertex2i(45,250);
	glVertex2i(40,225);
	glVertex2i(40,220);
	glVertex2i(50,220);
	glVertex2i(50,200);
	glVertex2i(30,200);
	glVertex2i(30,180);
	glVertex2i(50,180);
	glVertex2i(50,175);
	glVertex2i(75,175);
	glVertex2i(75,180);
	glVertex2i(80,180);
	glVertex2i(80,165);
	//glVertex2i(194,165);
	glEnd();
	
	//tap down side
	glBegin(GL_LINE_LOOP);
	glVertex2i(94,165);
	glVertex2i(94,160);
	glVertex2i(80,160);
	glVertex2i(80,165);
	glEnd();
	//water drop 1
	for(int i=0;i<50;i+=10)
	{
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(86,158-i);
	glVertex2i(85,150-i);
	glVertex2i(85,145-i);
	glVertex2i(87,145-i);
	glVertex2i(87,150-i);
	glEnd();
	i=i+5;

	}
	for(int i=0;i<40;i+=10)
	{
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(56,88-i);
	glVertex2i(55,80-i);
	glVertex2i(55,75-i);
	glVertex2i(57,75-i);
	glVertex2i(57,80-i);
	glEnd();
	i=i+5;

	}
	for(int i=0;i<30;i+=10)
	{
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(86,48-i);
	glVertex2i(85,40-i);
	glVertex2i(85,35-i);
	glVertex2i(87,35-i);
	glVertex2i(87,40-i);
	glEnd();
	i=i+5;

	}	
	//bucket side
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(58,90);
	glVertex2i(70,50);
	glVertex2i(100,50);
	glVertex2i(110,90);
	glEnd();
	
       //BUCKET HOLE
       glPointSize(10.0);
	glBegin(GL_POINTS);
	glColor3f(0.8,1.0,0.8);
	glVertex2i(85,50);
	glEnd();
       
       //tap in algo.
	glColor3f(0.3,0.1,0.2);
	glBegin(GL_LINE_STRIP);	
	glVertex2i(294,365);
	glVertex2i(294,394);
	glVertex2i(295,395);
	glVertex2i(295,400);
	glVertex2i(275,400);
	glVertex2i(275,415);
	glVertex2i(285,415);
	glVertex2i(285,420);
	glVertex2i(280,450);
	glVertex2i(245,450);
	glVertex2i(240,425);
	glVertex2i(240,420);
	glVertex2i(250,420);
	glVertex2i(250,400);
	glVertex2i(230,400);
	glVertex2i(230,380);
	glVertex2i(250,380);
	glVertex2i(250,375);
	glVertex2i(275,375);
	glVertex2i(275,380);
	glVertex2i(280,380);
	glVertex2i(280,365);
	//glVertex2i(194,165);
	glEnd();
	
	//tap down
	glBegin(GL_LINE_LOOP);
	glVertex2i(294,365);
	glVertex2i(294,360);
	glVertex2i(280,360);
	glVertex2i(280,365);
	glEnd();
	
	//1STdroplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,351);
	glVertex2i(294,337);
	glVertex2i(280,337);
	glVertex2i(280,351);
	glEnd();
	
	//line
	glBegin(GL_LINE_STRIP);
	glColor3f(0.0,0.0,0.0);
	glVertex2i(295,344);
	glVertex2i(340,311);
	glVertex2i(295,304);
	glEnd();
	
	//2nd droplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,311);
	glVertex2i(294,297);
	glVertex2i(280,297);
	glVertex2i(280,311);
	glEnd();
	
	//line
	glBegin(GL_LINES);
	glColor3f(0.0,0.0,0.0);
	glVertex2i(295,284);
	glVertex2i(340,311);
	glEnd();
	
	//unregulated flow
	glColor3f(0.0,0.0,0.0);
	char vu[]="unregulated flow";
	glRasterPos2f(341.0,310.0);
	for(int j=0;vu[j]!='\0';j++)
	glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vu[j]);
	
	//3rd droplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,291);
	glVertex2i(294,277);
	glVertex2i(280,277);
	glVertex2i(280,291);
	glEnd();
	
	
	//bucket word
	glColor3f(0.0,0.0,0.0);
	char vb[]="Bucket holding packets";
	glRasterPos2f(320.0,230.0);
	for(int j=0;vb[j]!='\0';j++)
	glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vb[j]);
	//bucket
	glBegin(GL_POLYGON);
	glColor3f(0.0,0.0,1.0);
	glVertex2i(258,250);
	glVertex2i(270,200);
	glVertex2i(300,200);
	glVertex2i(310,250);
	glEnd();
	
	//break
	glPointSize(10.0);
	glBegin(GL_POINTS);
	glColor3f(0.8,1.0,0.8);
	glVertex2i(285,200);
	glEnd();
	
	//1st droplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,166);
	glVertex2i(294,180);
	glVertex2i(280,180);
	glVertex2i(280,166);
	glEnd();
	
	//line
	glBegin(GL_LINE_STRIP);
	glColor3f(0.0,0.0,0.0);
	glVertex2i(295,173);
	glVertex2i(340,153);
	glVertex2i(295,153);
	glEnd();
	
	//2nd droplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,146);
	glVertex2i(294,160);
	glVertex2i(280,160);
	glVertex2i(280,146);
	glEnd();
	
	//line
	glBegin(GL_LINES);
	glColor3f(0.0,0.0,0.0);
	glVertex2i(295,133);
	glVertex2i(340,153);
	glEnd();
	
	//regulated flow
	glColor3f(0.0,0.0,0.0);
	char vr[]="regulated flow";
	glRasterPos2f(341.0,153.0);
	for(int j=0;vr[j]!='\0';j++)
	glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vr[j]);
	
	//3rd droplets
	glBegin(GL_POLYGON);
	glColor3f(0.4,1.0,0.4);
	glVertex2i(294,126);
	glVertex2i(294,140);
	glVertex2i(280,140);
	glVertex2i(280,126);
	glEnd();
	
	//network word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char vn[]="Network";
	glRasterPos2f(350.0,60.0);
	for(int j=0;vn[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vn[j]);
	//Network
	glColor3f(0.3,0.0,0.0);
	glBegin(GL_LINE_STRIP);
	glVertex2i(340,70);
	glVertex2i(320,100);
	glVertex2i(260,100);
	glVertex2i(240,60);
	glVertex2i(300,35);
	glVertex2i(340,70);
	glVertex2i(260,100);
	glVertex2i(300,35);
	glVertex2i(320,100);
	glVertex2i(240,60);
	glVertex2i(340,70);
	glEnd();
	//host word
	glColor3f(0.0,0.0,0.0);
	//int j;
	char v[]="Host";
	glRasterPos2f(170.0,400.0);
	for(int j=0;v[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,v[j]);
	//computer word
	char vc[]="Computer";
	glRasterPos2f(170.0,380.0);
	for(int j=0;vc[j]!='\0';j++)
							glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18,vc[j]);
	//glColor3f(0.0,0.0,0.0);
	glBegin(GL_LINE_LOOP);
	glVertex2i(228,450);
	glVertex2i(228,350);
	glVertex2i(160,350);
	glVertex2i(160,450);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(223,440);
	glVertex2i(223,360);
	glVertex2i(165,360);
	glVertex2i(165,440);
	glEnd();
	glBegin(GL_LINE_LOOP);
	glVertex2i(194,350);
	glVertex2i(184,335);
	glVertex2i(204,335);
	glEnd();
	glFlush();
}
void display2(int i)
{
if(i==0)
{

no_overflow();
translatePoint(287,344,0,4);	
}
else
{
overflow();
translatePoints(287,344,-2,6);	
}
}

void display()//Main Page
{
	int i;
	glClear(GL_COLOR_BUFFER_BIT);
	glColor3f(0.4,0.1,0.0);
	char f[]="CAMBRIDGE INSTITUTE OF TECHNOLOGY";
	glRasterPos2f(200.0,400.0);
	for(i=0;f[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,f[i]);

	glColor3f(0.4,0.1,0.0);
	char g[]="DEPARTMENT OF  COMPUTER SCIENCE AND ENGINEERING";
	glRasterPos2f(180.0,370.0);
	for(i=0;g[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,g[i]);

	glColor3f(0.4,0.1,0.7);
	char h[]="A MINI PROJECT ON:";
	glRasterPos2f(220.0,330.0);
	for(i=0;h[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,h[i]);

	glColor3f(0.4,0.1,0.7);
	char e[]="LEAKY BUCKET ALGORITHM";
	glRasterPos2f(210.0,300.0);
	for(i=0;e[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,e[i]);
glColor3f(0.5,0.0,0.7);
	char tby[]="BY";
	glRasterPos2f(250.0,270.0);
	for(i=0;tby[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,tby[i]);

	glColor3f(0.7,0.0,0.3);
	char t[]="G Srividya";
	glRasterPos2f(200.0,250.0);
	for(i=0;t[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,t[i]);

	glColor3f(0.7,0.0,0.3);
	char s[]="1CD18CS039";
	glRasterPos2f(270.0,250.0);
	for(i=0;s[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,s[i]);

	glColor3f(0.7,0.0,0.3);
	char u[]="M R Navaneetha";
	glRasterPos2f(200.0,230.0);
	for(i=0;u[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,u[i]);

	glColor3f(0.7,0.0,0.3);
	char v[]="1CD19CS404";
	glRasterPos2f(270.0,230.0);
	for(i=0;v[i]!='\0';i++)
		glutBitmapCharacter(GLUT_BITMAP_TIMES_ROMAN_24,v[i]);

}


void demo_menu(int id)
{
	//op=id;
	switch(id)	
	{
		case 1: display1();
			break;
		case 2:display2(0);
			break;
		case 3:display2(1);
			break;
		case 4:exit(0);
			break;
	}
	glutPostRedisplay();
}

void myinit()
{
	glClearColor(0.8,1.0,0.8,0.0);
	glMatrixMode(GL_PROJECTION);
	//load identity
	glLoadIdentity();
	gluOrtho2D(0.0,500.0,0.0,500.0);
	//why model view
	glMatrixMode(GL_MODELVIEW);
	//which below line
	glutPostRedisplay();
}

void main(int argc,char **argv)
{
	
	glutInit(&argc,argv);
	glutInitDisplayMode(GLUT_SINGLE|GLUT_RGB);
	glutInitWindowSize(500,500);
	glutInitWindowPosition(0,0);
	glutCreateWindow("Leaky Bucket");
	glutCreateMenu(demo_menu);
	glutAddMenuEntry("Algorithm",1);
	glutAddMenuEntry("no overflow",2);
	glutAddMenuEntry("overflow",3);
	glutAddMenuEntry("Exit",4);
	glutAttachMenu(GLUT_RIGHT_BUTTON);
	glutDisplayFunc(display);
	glClearColor(0.0,0.0,0.0,0.0);
	myinit();
	glutMainLoop();
}
