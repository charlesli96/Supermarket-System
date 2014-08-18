 //FINAL PROJECT
//AUGUST 8,2014
// SUPERMARKET TRANSACTION INVENTORY PROGRAM
// A REAL LIFE PROGRAM INSPIRED FROM MY UNCLE'S BUSINESS. IT HAS THE FEATURES OF LISTING INVENTORY AND TRANSACTION SUMMARY, ADD/ EDIT SUMMARY, ADD/ EDIT TRANSACTION, PRINT RECEIPT, AND CHANGE PASSWORD OF THE PROGRAM.
// I LEARNED THAT PUTTING COMMENTS ON PROGRAM CODES WILL HELP YOU TROUBLESHOOT THE PROBLEM. ALSO DOING THE FLOWCHART BEFORE THE CODING BENEFITS A LOT TO THE PROCESS OF CREATING THE PROGRAM.
//SUBMITTED BY CHARLES LI
//SUBMITTED TO ENGR. MELVIN CABATUAN


#include<iostream>
#include<stdlib.h>
#include<string.h>
#include <cstdlib>// for sleep
#include <algorithm>//for getline
#include <iomanip>
#include <time.h>// receipt time and date
using namespace std;

main()
{
      string pw,npw="2014",nnpw;
      int pwctrl=0;
      char choice, c, editchoice, dchoice, adiscount;
      string item[50]={"Nestle Full Cream Milk 1L","Coca-Cola Coke 1L","Monami Candy (50pcs/pack)","Selecta 3-in-1 Ice Cream 1Tab","Yakult Milk (5bottles/set)"};
      int itemnum[50]={0,1,2,3,4};
      int itemquantity[50]={10,10,10,10,10};
      float itemprice[50]={300,45,30,150,50};
      int ciadd=5;
      int trow, tcolumn=4;
      int editnum, editquantity; 
      string edititem;
      int sitemnum[50];
      int sitemquantity[50];
      float sitemprice[50];
      int sitem, difsitemquantity;
      float pricetotal, cash , change, vat , wovat, tvat=0, twovat=0, discount, editprice, tdiscount=0 ;
      int tsitemnum[50];
      int tsitemquantity[50];
      float tsitemprice[50];
      float transactiontotal=0;
      
      for(int k=0; k<ciadd; k++)//clean default value
                      
                      {
                              tsitemnum[k] = 0;
                              tsitemquantity[k]=0;
                              tsitemprice[k]=0;
                              }
                              
                              
      home: //for password error
      cout<<"Enter Password:";
      cin>>pw;
      cout<<"\n";
      if(pw==npw) //check pasword 
      {              //check password open yes
          cout<<" Access granted \n";  
          _sleep(500);// wait 1 second
          system("cls");
          cout<<"loading... \n";
          _sleep(500); // wait 1 second 
          
          
          menu:
          system("cls");
          //cout<<"Welcome to Lucky Arrow Express Supermarket\n";
          cout<<"     __    ____  ____  _____  _    _    ____  _  _  ____  ____  ____  ___  ___ \n";
          cout<<"    /__\\  (  _ \\(  _ \\(  _  )( \\/\\/ )  ( ___)( \\/ )(  _ \\(  _ \\( ___)/ __)/ __) ";
          cout<<"   /(__)\\  )   / )   / )(_)(  )    (    )__)  )  (  )___/ )   / )__) \\__ \\\\__ \\ ";
          cout<<"  (__)(__)(_)\\_)(_)\\_)(_____)(__/\\__)  (____)(_/\\_)(__)  (_)\\_)(____)(___/(___/ \n";
          cout<<"     ___  __  __  ____  ____  ____  __  __    __    ____  _  _  ____  ____       ";
          cout<<"   / __)(  )(  )(  _ \\( ___)(  _ \\(  \\/  )  /__\\  (  _ \\( )/ )( ___)(_  _)     ";
          cout<<"    \\__ \\ )(__)(  )___/ )__)  )   / )    (  /(__)\\  )   / )  (  )__)   )(       ";
          cout<<"    (___/(______)(__)  (____)(_)\\_)(_/\\/\\_)(__)(__)(_)\\_)(_)\\_)(____) (__)      \n\n ";
          cout<<" \t \t ********************************************** \n";
          cout<<" \t \t ********************************************** \n";
          cout<<" \t \t **                 Menu:                    ** \n";
          cout<<" \t \t **       A   Inventory  Summary             ** \n";                                        
          cout<<" \t \t **       B   Transaction Summary            ** \n";
          cout<<" \t \t **       C   Add / Edit Inventory           ** \n";
          cout<<" \t \t **       D   Create Transaction             ** \n";
          cout<<" \t \t **       E   Change Password                ** \n";
          cout<<" \t \t **       F   Exit                           ** \n";    
          cout<<" \t \t ********************************************** \n";
          cout<<" \t \t ********************************************** \n\n\n";
          enter:
          cout<<" \t \t \t Enter choice: ";
          cin>> choice; 
          
         
          
          switch(choice)
          {// switch start
                 case 'A':
                 case 'a':
                      system("cls");
                      cout << "Inventory Summary:" << endl;
	
	                  //printing border
	                  cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  //printing inventory
	                  cout << setfill(' ') << setw(1) << "|" << setw(10) << left << "Item No." << setw(1) << "|" << setw(10) << left << "Quantity" << setw(1) << "|"  << setw(40) << left << "Item" << setw(1) << "|" << setw(10)<< left <<"Price" << setw (1) <<"|" << endl;
	                  //printing border
	                  cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
	                  for (int i=0; i<ciadd; i++)
	                  {
                      //printing inventory
	                  cout << setfill(' ') << setw(1) << "|" << setw(10) << left << i+1 << setw(1) << "|" << setw(10) << left << itemquantity[i] << setw(1) << "|"  << setw(40) << left << item[i] << setw(1) << "|" << setw(10)<< left <<itemprice[i] << setw (1) <<"|" << endl;
	                  //printing border
	                  cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  }
	                  system("pause");
	                  goto menu;
                      break; // EndCase A inventory summary
                      
                 case 'B': 
                 case 'b': 
                            
                            system("cls");
                            cout << "Transaction Summary:" << endl;
	
                            //printing border
	                            cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                            //printing inventory
	                            cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << left << "Item No." << setw(1) << "|" << setw(10) << left << "Quantity" << setw(1) << "|"  << setw(40) << left << "Item" << setw(1) << "|" << setw(10)<< left <<"Price" << setw (1) <<"|" << endl;
	                            //printing border
                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
                                
                                for (int y=0; y<ciadd; y++)
                                {   //open printing
                                
                                    if (tsitemquantity[y]!=0)
                                    {// if printing open 
                                    //printing inventory
	                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << left << y+1 << setw(1) << "|" << setw(10) << left << tsitemquantity[y] << setw(1) << "|"  << setw(40) << left << item[y] << setw(1) << "|" << setw(10)<< right <<tsitemprice[y] << setw (1) <<"|" << endl;
	                                //printing border
	                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                                                                                 
                                    }//if close printing
                                    
                                }// close printing
                                twovat=transactiontotal*0.88;
                                tvat=transactiontotal*0.12;
                                    
                                
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Amount of Sales with VAT" << setw(1) << "|" << setw(10) << right<< transactiontotal << setw (1) <<"|" << endl;
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" 10% discount given" << setw(1) << "|" << setw(10) << right <<tdiscount << setw (1) <<"|" << endl;
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Total sales with discount" << setw(1) << "|" << setw(10) << right <<transactiontotal- tdiscount << setw (1) <<"|" << endl;                                
                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
                                 
                      system("pause");
	                  goto menu;
    
                 
                      break; // EndCase B transaction summary

                 case 'C': 
                 case 'c': 
                           system("cls");
                           cmenu:
                           cout<<"  \n \t \t \t Add or Edit Inventory: \n \t \t \t A. Add new product \n \t \t \t B. Edit existing Product \n \t \t \t C. Back to Menu \n \n " ;
                           cout<<"\t \t \t Enter choice:";
                           cin>>c; 
                           switch (c)
                           {         //add or edit open
                           case 'a':
                           case 'A':
                                     
                                     cout<<"\n \n \t \t \t Enter New Item:";
                                     cin.ignore();
                                     getline(cin, item[ciadd]);
                                    
                                     cout<<"\n \n \t \t \t Enter quantity of "<<item[ciadd]<<":";
                                     cin>>itemquantity[ciadd];
                                    
                                     cout<<"\n \n \t \t \t Enter the price of "<<item[ciadd]<<":";
                                     cin>>itemprice[ciadd];
                                     itemnum[ciadd]=ciadd;
                                     
                                     cout<<"\n \n  Item No. "<< itemnum[ciadd]+1<<" \t Quantity: "<<itemquantity[ciadd]<<"\t Description: "<< item[ciadd]<<" \t Price: P "<< (float)itemprice[ciadd]<<"\n"; 
                                     cout<<"\n \n \t \t  ...New Entry Saved... \n \n ";
                                     _sleep(600);
                                     
                              tsitemnum[ciadd] = 0;
                              tsitemquantity[ciadd]=0;
                              tsitemprice[ciadd]=0;
                              
                                     ciadd=ciadd+1;
                                     
                                     goto cmenu;
                                     break;   // add 
                           case 'b':
                           case 'B':
                                     cedit: 
                                     system("cls");
                                     cout << "Inventory Summary:" << endl;
	
  	                                 //printing border
	                                 cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                                 //printing inventory
	                                 cout << setfill(' ') << setw(1) << "|" << setw(10) << left << "Item No." << setw(1) << "|" << setw(10) << left << "Quantity" << setw(1) << "|"  << setw(40) << left << "Item" << setw(1) << "|" << setw(10)<< left <<"Price" << setw (1) <<"|" << endl;
	                                 //printing border
	                                 cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
	                                 for (int i=0; i<ciadd; i++)
	                                 {
                                     //printing inventory
	                                 cout << setfill(' ') << setw(1) << "|" << setw(10) << left << i+1 << setw(1) << "|" << setw(10) << left << itemquantity[i] << setw(1) << "|"  << setw(40) << left << item[i] << setw(1) << "|" << setw(10)<< left <<itemprice[i] << setw (1) <<"|" << endl;
	                                 //printing border
	                                 cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                                 }              
  	                  
                                     cout<<"\n \n \t \t Enter Item No. you want to edit: ";
                                     cin>>editnum;
                                     cout<<"\n \n \t \t \t Press A - to edit Item Name \n \n \t \t \t Press B - to edit Item Quantity \n \n \t \t \t Press C - to edit Item Price \n \n ";
                                     cout<<"\n \n \t \t \t Your choice: ";
                                     cin>>editchoice; 
                                     
                                                      switch (editchoice)
                                                      { //open edit choice
                                                       case 'a':
                                                       case 'A':
                                                                cout <<"\n \n \t \t Enter new Item Name for Item No. "<< editnum<< " : ";
                                                                cin.ignore();
                                                                getline(cin, edititem);
                                                                
                                                                item[editnum-1]=edititem;
                                                                cout<<"\n \n \t \t \t  ...Changes Saved... \n \n ";
                                                                _sleep(500);
                                     
                                                                system("cls");
                                                                goto cmenu;
                                                                break;       
                                                                         
                                                       case 'b':
                                                       case 'B':
                                                       
                                                                cout <<"\n \n \t \t Enter new Item Quantity for Item No. "<< editnum<< " : ";
                                                                cin>>editquantity;
                                                                
                                                                itemquantity[editnum-1]=editquantity;
                                                                cout<<"\n \n \t \t \t  ...New Entry Saved... \n \n ";
                                                                _sleep(500);
                                                                system("cls");
                                                                goto cmenu;
                                                                break;       
                                                                
                                                       case 'c':
                                                       case 'C':    
                                                                cout <<" \n \n \t \t Enter new Item Price for Item No. "<< editnum<< " : " ;
                                                                cin>>editprice;
                                                                
                                                                itemprice[editnum-1]=editprice;
                                                                cout<<"\n \n \t \t \t  ...New Entry Saved... \n \n ";
                                                                _sleep(500);
                                                                system("cls");
                                                                goto cmenu;
                                                                break;           
                                                                    
                                                                                                                               
                                                       default: 
                                                                cout<<"Invalid input \n";
                                                                system("cls");
                                                                goto cedit;  
                                                             }// close edit choice 
                                     
                                     goto cmenu;
                                     break;   // edit
                           case 'c':
                           case 'C':
                                     goto menu;
                                     break;
                           default:
                                   cout<<"\n\n \t \t \t Invalid selection \n\n";
                                   system("cls");
                                   goto cmenu;
                           }         //add or edit close
                           
                      break; // EndCase C add/ edit inventory
       
                 case 'D': 
                 case 'd': 
                      for(int k=0; k<ciadd; k++)//clean default value
                      
                      {
                              sitemnum[k] = 0;
                              sitemquantity[k]=0;
                              sitemprice[k]=0;
                              }
                      pricetotal=0;
                      dmenu:
                      system("cls");     
                      
                      cout<<"\n \t \t Press A to add transaction \n \t \t Press B to edit transaction  \n \t \t press C to end transaction and print receipt \n";
                      cin>>dchoice;
                      system("cls");
                      switch (dchoice)
                       {// dchoice open switch
                       case 'a':
                       case 'A':
                            //printing border
	                        cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                        //printing inventory
	                        cout << setfill(' ') << setw(1) << "|" << setw(10) << left << "Item No." << setw(1) << "|" << setw(10) << left << "Quantity" << setw(1) << "|"  << setw(40) << left << "Item" << setw(1) << "|" << setw(10)<< left <<"Price" << setw (1) <<"|" << endl;
	                        //printing border
                            cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
	                        for (int i=0; i<ciadd; i++)
	                        {
                                //printing inventory
	                            cout << setfill(' ') << setw(1) << "|" << setw(10) << left << i+1 << setw(1) << "|" << setw(10) << left << itemquantity[i] << setw(1) << "|"  << setw(40) << left << item[i] << setw(1) << "|" << setw(10)<< left <<itemprice[i] << setw (1) <<"|" << endl;
	                            //printing border
	                            cout << setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                        }               
                            dbmenu:
                            cout<<"\n Enter the item no. of the product you want to purchase :";            
                            cin>>sitem;
                            
                            if (itemquantity[sitem-1]==0)
                            {
                               if(item[sitem-1]=="")
                               {cout<<"\n Product doesn't exist \n";}
                               else
                               {cout<<" \n Out of stock!, Please choose other products \n";}
                            _sleep(2000);
                            goto dbmenu;
                            break;
                            }
                            else if (itemquantity[sitem-1]>0)
                            {
                            dquantity:
                                      cout<<"\n Enter quantity:";
                                      cin>>sitemquantity[sitem-1];
                                      if (sitemquantity[sitem-1]>itemquantity[sitem-1])
                                      {
                                      cout<<" \n Sorry, we only have "<<itemquantity[sitem-1]<< " available. \n"; 
                                      goto dquantity;
                                      break;
                                      }
                                      else if(sitemquantity[sitem-1]<=itemquantity[sitem-1]) 
                                      {
                                      sitemprice[sitem-1]=itemprice[sitem-1]*sitemquantity[sitem-1];
                                      itemquantity[sitem-1]=itemquantity[sitem-1]-sitemquantity[sitem-1];
                                      cout<<"Recorded \n";
                                      cout<<"Item no. "<< sitem << "\t"<<sitemquantity[sitem-1]<<"   "<<item[sitem-1]<<" @"<<itemprice[sitem-1]<<" each   P "<<sitemprice[sitem-1]<<" \n";
                                      
                                      pricetotal= (float)sitemprice[sitem-1]+ pricetotal;
                                      sitemnum[sitem-1]=sitem;
                                      
                           _sleep(600);
                           goto dmenu;
                           break;     
                           }
                           }
                       case 'b':
                       case 'B':
                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
                                
                                for (int k=0; k<ciadd; k++)
                                {   //open printing
                                
                                    if (sitemnum[k]!=0)
                                    {// if printing open 
                                    //printing inventory
	                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << left << k+1 << setw(1) << "|" << setw(10) << left << sitemquantity[k] << setw(1) << "|"  << setw(40) << left << item[k] << setw(1) << "|" << setw(10)<< right <<sitemprice[k] << setw (1) <<"|" << endl;
	                                //printing border
	                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                                                                                 
                                    }//if close printing
                                    
                                }// close printing
                                
                                cout<<"\n \n \t \t Enter Item No. in the transaction you want to edit: "<<endl;
                                cin>>sitem;
                                
                                 if (sitemquantity[sitem-1]==0 || sitem==0)
                                {cout<<"There is nothing to edit here."<<endl;
                                _sleep(600);
                                goto dmenu;
                                }
                                else
                                {
                                difsitemquantity=sitemquantity[sitem-1];
                                cout <<"\n \n \t \t Enter new Item Quantity for Item No. "<< sitem<< " : ";
                                cin>>sitemquantity[sitem-1];
                                sitemprice[sitem-1]=itemprice[sitem-1]*sitemquantity[sitem-1];
                                difsitemquantity=-difsitemquantity+sitemquantity[sitem-1];
                                itemquantity[sitem-1]=itemquantity[sitem-1]-difsitemquantity;
                                pricetotal=0;
                                for(int z=0; z<ciadd; z++)//clean default value
                      
                                {
                                
                                pricetotal=pricetotal+sitemprice[z];
                                              }
                                                      
                                cout<<"\n \n \t \t \t  ...Change Saved... \n \n ";
                                }
                              
                                _sleep(500);
                                system("cls");
                                goto dmenu;
                                break;       
                                                                

                                
                       case 'c':
                       case 'C':
                           
                           
                                cout<<"Are you a loyalty card or senior citizen cardholder? (y - yes ; n - no)"<<endl;
                                discounted:
                                cin>>adiscount;
                                
                                switch (adiscount)
                                {
                                case'Y':
                                case'y':
                                        discount=pricetotal*0.1;
                                        tdiscount=discount+tdiscount;// summary of transaction
                                        break;
                                        
                                case 'n':
                                case 'N':
                                         discount=0;
                                         break;
                                default:
                                        cout<<"Invalid input \n";
                                        goto discounted;
                                        break;
                                       }
                                       
                                       
                                payment:
                                cout<<"Enter Cash payment:";
                                cin>>cash;
                                
                                if (cash<pricetotal)
                                {cout<<"\n Insufficient fund."; goto payment;}
                                else {change=cash-pricetotal+discount;}
                                transactiontotal=transactiontotal+pricetotal;//for summary of transaction
                                
                                time_t tim;  //create variable of time_t

                                 time(&tim); //pass variable tim to time function
  
                                
                                system("cls");
                                cout<<"     __    ____  ____  _____  _    _    ____  _  _  ____  ____  ____  ___  ___ \n";
                                cout<<"    /__\\  (  _ \\(  _ \\(  _  )( \\/\\/ )  ( ___)( \\/ )(  _ \\(  _ \\( ___)/ __)/ __) ";
                                cout<<"   /(__)\\  )   / )   / )(_)(  )    (    )__)  )  (  )___/ )   / )__) \\__ \\\\__ \\ ";
                                cout<<"  (__)(__)(_)\\_)(_)\\_)(_____)(__/\\__)  (____)(_/\\_)(__)  (_)\\_)(____)(___/(___/ \n";
                                cout<<"     ___  __  __  ____  ____  ____  __  __    __    ____  _  _  ____  ____       ";
                                cout<<"   / __)(  )(  )(  _ \\( ___)(  _ \\(  \\/  )  /__\\  (  _ \\( )/ )( ___)(_  _)     ";
                                cout<<"    \\__ \\ )(__)(  )___/ )__)  )   / )    (  /(__)\\  )   / )  (  )__)   )(       ";
                                cout<<"    (___/(______)(__)  (____)(_)\\_)(_/\\/\\_)(__)(__)(_)\\_)(_)\\_)(____) (__)    \n "<<endl;
                                cout<<"    Laguna Blvd,LTI Spine Road,Brgy Biñan and Malamig, Biñan City, Laguna \n";
                                cout<<"\t \t \t      Tel No. (02)5244611 \n";
                                cout<<"\t \t \t      TIN 123-456-789-000 \n";
                                cout<<"\t \t \t   Permit# 0932-160-01910-321 \n"<<endl<< endl;
                                cout<<"\t \t \t Date: "<<ctime(&tim); // this translates what was returned from time() into a readable format
                                
                                //printing border
	                            cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                            //printing inventory
	                            cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << left << "Item No." << setw(1) << "|" << setw(10) << left << "Quantity" << setw(1) << "|"  << setw(40) << left << "Item" << setw(1) << "|" << setw(10)<< left <<"Price" << setw (1) <<"|" << endl;
	                            //printing border
                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
	                  
                                
                                for (int k=0; k<ciadd; k++)
                                {   //open printing
                                
                                    if (sitemquantity[k]!=0)
                                    {// if printing open 
                                    //printing inventory
	                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << left << k+1 << setw(1) << "|" << setw(10) << left << sitemquantity[k] << setw(1) << "|"  << setw(40) << left << item[k] << setw(1) << "|" << setw(10)<< right <<sitemprice[k] << setw (1) <<"|" << endl;
	                                //printing border
	                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
                   
                                    tsitemquantity[k]=tsitemquantity[k]+sitemquantity[k];
                                    tsitemnum[k]=sitemnum[k];
                                    tsitemprice[k]=tsitemprice[k]+sitemprice[k];
                                    
                                    
                                    }//if close printing
                                    
                                }// close printing
                                wovat=pricetotal*0.88;
                                vat=pricetotal*0.12;
                                    
                                
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Total Amount" << setw(1) << "|" << setw(10)<<right <<wovat << setw (1) <<"|" << endl;                            
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" 12% VAT" << setw(1) << "|" << setw(10) << right<<vat << setw (1) <<"|" << endl;
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Amount of Sales with VAT" << setw(1) << "|" << setw(10) << right <<pricetotal << setw (1) <<"|" << endl;
                                switch (adiscount)
                                {
                                       case'y':
                                       case 'Y':
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" less 10% Discount" << setw(1) << "|" << setw(10) << right <<-1*discount << setw (1) <<"|" << endl;                                                    
                                                   }
                                
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Total Payment" << setw(1) << "|" << setw(10) << right <<cash << setw (1) <<"|" << endl;
                                cout <<"  "<< setfill(' ') << setw(1) << "|" << setw(10) << " " << setw(1) << " " << setw(10) << " " << setw(1) << " " << setw(40) << right<<" Change" << setw(1) << "|" << setw(10) <<right <<change  << setw (1) <<"|" << endl;
                                cout <<"  "<< setfill('-') << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(10) << "-" << setw(1) << "+" << setw(40) << "-" << setw(1) << "+" << setw(10)<< "-" << setw(1)<< "+"<< endl;
                                cout<<endl;
                                cout<<" \t \t     Received Merchandise in Good Condition"<<endl<<endl;
                                cout<<" \t \t       Thank YOu and Please Come Again!"<<endl<<endl;
                                cout<<" \t \t      This Serve as your Official Receipt"<<endl<<endl;
                                cout<<" \t \t      Your feedback is important to us..."<<endl<<endl;
                                cout<<" \t \t      email us at charles_li@dlsu.edu.ph "<<endl<<endl;
                                system("pause");
                                goto menu;
                                break;
                           
                       default:
                           cout<<"\n Invalid input";
                           system("cls");
                           goto dmenu;     
                       }// dchoice close switch
                      
                  // }                                              
               // }
                      
                           
                      break; // EndCase D create transaction

                 case 'E':
                 case 'e':
                      
                          system("cls");
                          cout<<"Enter Old Password: ";
                          cin>>npw;
                          
                          if (npw==pw)
                          {
                          pass:
                          npw="";
                          cout<<"Enter New password: ";
                          cin>>npw;
                          cout<<"Enter New password again: ";
                          cin>>nnpw;
                                    if (nnpw==npw)
                                    {cout<<"Password Saved ";
                                    _sleep(500);
                                    system("cls");
                                    goto home;}
                                    else {goto pass;};
                          }
                          else 
                          {
                               cout<<"Invalid Password";
                               _sleep(500);
                               goto menu;
                               system("cls");
                           }
                          
                          break;
                      
                 case 'F':  
                 case 'f': 
                           cout<<"\n \t \t \tHave a nice day! See you soon! \n\n";
                           _sleep(500);
                           return 0;
                      break; // EndCase E exit
                
                 default: 
         cout<<"\n\n \t \t \t Invalid selection \n\n";
         goto enter; 
         
               
    } //EndSwitch 
          
                        
      }// check password close yes
      else
      {// check password open no
       cout<<" Access Denied \n";
       system("pause");
       system("cls");
                     if (pwctrl<3) // 3 time error allowance
                      {
                      pwctrl=pwctrl+1;
                      goto home;
                      }
                      else
                      {
                          cout<<"\n \n Contact your Administrator. \n";
                          system("pause");
                          return 0;
                      }
         
       }// check pasword close no
      
  
      system("pause");
}
