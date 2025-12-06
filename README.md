#include<stdio.h>
int main()
{
    int category;
    float units,Meter_Charge,Electricity_Charge,Total_bill;
    float GST,Fuel_Surcharge,govt_subsity;
    char Meter_number[100];
    float bill;
    printf("Enter Meter number : ");
    scanf("%s",Meter_number);
    printf("Categories : \n1.Commercial.\n2.Agriculture.\n3.Home.\n4.Urban.\n5.Rural.\nEnter category no : ");
    scanf("%d",&category);
    if(category==1)
    {
        printf("Commercial\n");
        printf("units(>0) : ");
        scanf("%f",&units);
        if(units<=0)
        {
            printf("Invalid units consumption\nEnter valid units > 0");
            return 0;
        }
        if(units>0&&units<=100)
        {
            bill=7*units;
        }
        else
        if(units<=200&&units>101)
        {
            bill=(7*100)+(units-100)*8;
        }
        else
        if(units<=300&&units>200)
        {
            bill=(7*100)+(8*100)+(units-200)*9;
        }
        else
        if(units>300)
        {
            bill=(7*100)+(8*100)+(9*100)+(units-300)*10;
        }
    }
    else
    if(category==2)
    {
        printf("Agriculture\n");
        printf("units(>0) : ");
        scanf("%f",&units);
        if(units<=0)
        {
            printf("Invalid units consumption\nEnter the units > 0");
            return 0;
        }
        if(units>0&&units<=100)
        {
            bill=1*units;
        }
        else
        if(units>100&&units<=200)
        {
            bill=(1*100)+(units-100)*1.5;
        }
        else
        if(units>200&&units<=300)
        {
            bill=(1*100)+(1.5*100)+(units-200)*2;
        }
        else
        if(units>300)
        {
            bill=(1*100)+(1.5*100)+(2*100)+(units-300)*3;
        }
    }
    else
    if(category==3)
    {
        printf("Home\n");
        printf("units(>0) : ");
        scanf("%f",&units);
        if(units<=0)
        {
            printf("Invalid units consumption \nEnter valid units>0");
            return 0;
        }
    if(units>0&&units<=100)
    {
        bill=3*units;
    }
    else
    if(units>=101&&units<=200)
    {
        bill=(3*100)+(units-100)*5;
    }
    else
    if(units>=201&&units<=300)
    {
        bill=(3*100)+(5*100)+(units-200)*6.5;
    }
    else
    if(units>=301&&units<=500)
    {
        bill=(3*100)+(5*100)+(6.5*100)+(units-300)*8;
    }
    else
    if(units>500)
    {
        bill=(3*100)+(5*100)+(6.5*100)+(8*200)+(units-500)*10;
    }
    }
    else
    if(category==4)
    {
        printf("Urban\n");
        printf("units(>0) : ");
        scanf("%f",&units);
        if(units<=0)
        {
            printf("Invalid Units consumption \n Enter valid units>0");
            return 0;
        }
        if(units>0&&units<=100)
        {
            bill=3*units;
        }
        else
        if(units>100&&units<=200)
        {
            bill=(3*100)+(units-100)*4;
        }
        else
        if(units>200&&units<=300)
        {
            bill=(3*100)+(4*100)+(units-200)*5;
        }
        else
        if(units>300)
        {
            bill=(3*100)+(4*100)+(5*100)+(units-300)*6;
        }
    }
    else
    if(category==5)
    {
        printf("Rural\n");
        printf("units(>0) : ");
        scanf("%f",&units);
        if(units<=0)
        {
            printf("Invalid units consumption \nEnter valid units>0");
            return 0;
        }
        if(units>0&&units<=100)
        {
            bill=2*units;
        }
        else
        if(units>100&&units<=200)
        {
            bill=(2*100)+(units-100)*3;
        }
        else
        if(units>200&&units<=500)
        {
            bill=(2*100)+(3*100)+(units-200)*5;
        }
        else
        if(units>500)
        {
            bill=(2*100)+(3*100)+(5*100)+(units-300)*7;
        }
    }
    else
    {
        printf("\nInvalid category\nPlease Select Valid Category.\n");
        return 0;
      
    }
    if(units>0&&units<150)
    {
        govt_subsity=0;
    }
     else
     {
         govt_subsity=150;
     }
    printf("Total energy charges = %.2f",bill);
    Meter_Charge=50;
    Electricity_Charge=0.30;
    Fuel_Surcharge=0.20;
    GST=0.8;
    Total_bill=bill+Meter_Charge+Electricity_Charge+Fuel_Surcharge-govt_subsity+GST;
    
    printf("       \n\t\n\t\tELECTRICIY BILL\n");
    printf("______________________________________________________\n");
    printf("Meter number          = %s\n",Meter_number);
    printf("Units                 = %.2f\n",units);
    printf("Energy charges        = %.2f\n",bill);
    printf("Meter charges         = %.2f\n",Meter_Charge);
    printf("Electricity charge    = %.2f\n",Electricity_Charge);
    printf("GST                   = %.2f\n",GST);
    printf("Fuel Surcharge        = %.2f\n",Fuel_Surcharge);
    printf("Government Subsity(-) = %.2f\n",govt_subsity);
    printf("Total bill            = %.2f\n",Total_bill);
    printf("______________________________________________________\n");
    printf("Current Date = %s\n",__DATE__);
    printf("Due Date     = Seven days from the current date\n");
    printf("If not paid before due date\n");
    printf("Late fee=100\n");

    return 0;
}
   
