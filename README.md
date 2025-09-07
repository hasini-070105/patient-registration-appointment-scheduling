# patient-registration-appointment-scheduling
We should get the patients  registered in our hospital if not we can get them  registered. Then we can give them appointments  according to the availability of the respective doctor by  taking some basic inputs such as patients ID, date on  which they wanted the appointment and so on.Upon  that we can view our appointment.

#include<stdio.h>
 int i=0;
 typedef struct {
 char name[10];
 int age;
 char gender[11];
 long phno;
 char date[10];
 char time[6];
 }patient;
 patient pnt[10];
 void register patient(){
 if (i>9){
 printf(“maximum no of patients had registered\n”);
 }
 else{
 printf(“enter your details.”);
 printf(“\n name (within 10 letters):”);
 scanf(“%s”,pnt[i].name);
printf(“Age:”);
 scanf(“%d”,&pnt[i].age);
 printf(“Gender:”);
 scanf(%s,pnt[i].gender);
 printf(“contact no:”);
 scanf(“%s”,pnt[i].phno);
 printf(“you have succesfully registered.your patient ID is %d.\n,i+1);
 }
 i++;
 }
 int show_patient_details(int i){
 printf(“\n Name :%s”,pnt[i].name);
 printf(\n Age:%d”,pnt[i].age);
 printf(“\n gender :%s”,pnt[i].gender);
 printf(“\n contact no:%s”,pnt[i].phno);
 return 0;
 }
int appointment (int i ){
 printf(“Date(eg.02-10-2024):”);
 scanf(“%s”,pnt[i].date);
 printf(“time(eg.9:30am):”);
 scanf(“%s”,pnt[i].time);
 printf(“your appointment has done”);
 return 0;
 }
 int show_appointment_details(int i){
 printf(“\n Date:%s”,pnt[i].date);
 printf(“\n Time:%s”,pnt[i].time);
 }
 void ser(int service){
 int id;
 switch(service){
 case 1:  registerpatient();
 break;
 case 2 :printf(“did you had registered?(if yes enter 1
 else 0):”);
int regstatus;
 scanf(“%d”,&regstatus);
 if(regstatus==0){
 registerpatient();
 }
 printf(“enter your patientID:”);
 scanf(“%d”,&id);
 appointment(id-1);
 break;
 case 3 :printf(“enter your patientID:”);
 scanf(“%d”,&id);
 show_patient_details(id-1);
 break;
 case 4 :printf("enter your patientID:”);
 scanf(“%d”,&id);
 show_appointment_details(id-1);
 break;
 }
 }
int main(){
 printf(“welcome to ABCD hospitals :”);
 printf(“\n  available sevices:”);
 printf(“\n 1.Patient registration”);
 printf(“\n 2.Appointment for doctor consult.”);
 printf(“\n 3.view patient details.”);
 printf(“\n 4.view appointment details.”);
 int a=1;
 while(a!=0){
 int service;
 printf(“\n Enter the corresponding number for the service,you
 want:”);
 scanf(“%d”,&service);
 ser(service);
 printf(“\n Do you want any other service(if yes press 1 else 0):”);
 scanf(“%d”,&a);
 }
 printf(“ Thanks for visiting ABCD hospitals.\n”);
 return 0;
 
