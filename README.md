# laborator9-10
https://classroom.google.com/u/0/c/Mjc5NDIwMzk5NzUz/a/MjczNzUwNTU1MTE1/details

#include <iostream>
#include <string>
#include <conio.h>
using namespace std;
int Guess;
int Total;

class Question
{
private:
	string Question_Text;
	string Answer1;
	string Answer2;
	string Answer3;

	int CorrectAnswer;
	int QuestionScore;

public:
	void setValues(string, string, string, string, int, int);
	void askQuestion();
};

void Question::setValues (string intrebarea, string raspuns1, string raspuns2, string raspuns3, int corect, int punct)
	{
	Question_Text=intrebarea;
	Answer1=raspuns1;
	Answer2=raspuns2;
	Answer3=raspuns3;
	CorrectAnswer=corect;
	QuestionScore=punct;
	}

void Question::askQuestion()
	{
		cout<<endl;
		cout<<Question_Text<<endl;
		cout<<"1. "<<Answer1<<endl;
		cout<<"2. "<<Answer2<<endl;
		cout<<"3. "<<Answer3<<endl;
		cout<<endl<<"Raspunsul tau este: ";
		cin>>Guess;
		if (Guess==CorrectAnswer)
		{
			cout<<endl<<"Raspuns corect."<<endl;
			Total=Total+QuestionScore;
		}
		else
		{
			cout<<endl;
			cout<<"Raspuns incorect. Raspunsul corect este "<<CorrectAnswer<<"."<<endl;
		}
	}

int main()
{
	cout<<"Test la management"<<endl;

	string Nume, Prenume, Specializare;
	int An;
	cout<<"Numele: ";
	cin>>Nume;
	cout<<"Prenumele: ";
	cin>>Prenume;
	cout<<"Specializarea(de forma IE/AF/CIG etc.): ";
	cin>>Specializare;
	cout<<"Anul de studiu (de forma 1/2/3): ";
	cin>>An;
	cout<<endl;

	Question intrebarea1;
	Question intrebarea2;
	Question intrebarea3;
	Question intrebarea4;
	Question intrebarea5;
	Question intrebarea6;
	Question intrebarea7;
	Question intrebarea8;
	Question intrebarea9;
	Question intrebarea10;

	intrebarea1.setValues("Competentele esentiale a clturii organizationala este reprezentata de: ",
		"valori",
		"limbaj",
		"simboluri",
		1,
		1);

	intrebarea2.setValues("Rolurile managementului sunt grupate in urmatoarele categorii",
		"rolul propagatorului,rol informational,rol de antreprenor",
		"roluri interpersonale,roluri informational,roluri decizionale",
		"rol decizional,rol de intermediar, rol informational",
		2,
		1);

	intrebarea3.setValues("Cine sunt reprezentantii managementului stiintific?",
		"Max Weber si Abraham Maslow ",
		"F. W. Taylor si Henry Gantt",
		"Herbert Simon, Alvin Toffler si Peter F. Drucker",
		2,
		1);

	intrebarea4.setValues("Timpul consumat cu sedinte de catre managerii de mijloc se estimeaza a fi de:",
		"60-85% din timpul de lucru",
		"50-75% din timpul de lucru",
		"50-80% din timpul de lucru",
		3,
		1);

	intrebarea5.setValues("Intre teoriile recente ale managementului nu se numara:",
		"managementul siintific",
		"managementul total",
		"managementul non-tipic",
		1,
		1);

	intrebarea6.setValues("In cazul deciziei in conditii de risc: ",
		"niciuna din variantele de mai jos",
		"exista un singur rezultat pentru fiecare alternativa aleasa",
		"exista mai ulte rezultate posibile pentru fiecare alternativa",
		3,
		1);

	intrebarea7.setValues("Distinctia dintre bine si rau si actiunea ce deriva in raport cu ceea ce este conform (fundamentat pe un cod social) este esenta: ",
		"eticii",
		"moralei",
		"legii",
		2,
		1);

	intrebarea8.setValues("Obiectivele organizationale pot fi clasificate astfel: ",
		"tangibile si intangibile",
		"masurabile si mai greu de cuantificat",
		"ambele variante sunt corecte",
		3,
		1);

	intrebarea9.setValues("Cercetarea este un element al domeniului: ",
		"tehnic",
		"economic",
		"social",
		1,
		1);

	intrebarea9.setValues("Care din urmatoarele aspecte nu genereaza diferente culturale:",
		"atitudinea fata de timp",
		"relatiile interumane",
		"relatiile internationale",
		2,
		1);

	intrebarea1.askQuestion();
	intrebarea2.askQuestion();
	intrebarea3.askQuestion();
	intrebarea4.askQuestion();
	intrebarea5.askQuestion();
	intrebarea6.askQuestion();
	intrebarea7.askQuestion();
	intrebarea8.askQuestion();
	intrebarea9.askQuestion();
	intrebarea9.askQuestion();
	cout<<endl;
	cout<<endl;

	cout<<"ai raspuns corect la "<<Total-1<<" intrebari si ai nota "<<Total<<endl;
	cout<<endl;
	if (Total>=5)
		cout<<"Felicitari! Ai trecut!";
	else
		cout<<"Nu ai promovat! Mai mult noroc data viitoare!";
	_getch();
	return 0;
}



