#include <iostream>
using namespace std;
//Variable
double Balance=1000;
int Deposit=0;
double Withdraw=0;
int Password=0000;
int Choice;
int Exit;
//end of variable

//function to display the menu of ATM
void display()
{
    //main screen
cout<<"********Menu********"<<endl;
cout<<"                             "<<endl;
cout<<"1:Balance"<<"\t"<<"2:Withdraw"<<endl;
cout<<"                             "<<endl;
cout<<"3:Deposit"<<"\t"<<"4:Exit"<<endl;
cout<<"                             "<<endl;
cout<<"************************"<<endl;
}
void process()
{
    cout<<"Enter Your Password"<<endl;
    cin>>Password;
    do{
    if(Password==0000)
      {
        cout<<"Enter Your Choice : "<<endl;
        cin>>Choice;


        switch(Choice)
        {
        case 1:
            cout<<"Your Balance is : "<<Balance<<endl;
            break;
        case 2:
            cout<<"Your Current Balance is : "<<Balance<<endl;
            cout<<"Enter Your Deposit :"<<endl;
            cin>>Deposit;
            Balance+=Deposit;
            cout<<"Your New Balance is : "<<Balance<<endl;
            break;
        case 3:
            cout<<"Note! Your Balance is : "<<Balance<<endl;
            cout<<"Enter Your Amount"<<endl;
            cin>>Withdraw;
            if (Balance>=Withdraw)
            {
            Balance-=Withdraw;
            cout<<"Your New Balance is : "<<Balance<<endl;
            }
            else
            {
            cout<<"Sorry Your Balance is not enough"<<endl;
            }
            break;
        case 4:
            cout<<"Thank You"<<endl;
            break;
    }//end of switch
    }
    else
    {
        char Option;
        cout<<"Your Password is Incorrect ,Do You Want To Try Again ? Enter [Y] for Yes or [N]for No."<<endl;
        cin>>Option;
        if(Option=='Y'||Option=='y')
        {
            cout<<"Enter Your Password"<<endl;
            cin>>Password;
        }
        else
        {
            break;
        }
    }//end of if

    }while(Choice<4);
}//end of process
int main()
{
    display();
    process();
    return 0;
}
