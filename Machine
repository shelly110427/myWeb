#include <iostream>
#include <cmath>
#include <string>

using namespace std;


class Machine {  
    protected:
        string type;
    public:
        virtual void welcome_message(){}
        virtual void problem_solver(int x){}
		virtual void problem_solver(string str){}
};


class Math_machine:public Machine{
    public:
        Math_machine(string type){this->type=type;}
        void welcome_message(){cout<<"Solving the "<<type<<" problem."<<endl;}

        void problem_solver(int x) {
        int aa=-1 , aaa=-1 , bb=-1 , bbb=-1;
            for(int a=sqrt(x);a>=1;a--)
            {
            	if(x%a ==0){
            		//cout << a << " " << x/a << endl;
            		aa=a,aaa=x/a;
            		break;
				}	
			}
            for(int b=sqrt(x+1);b>=1;b--)
            {
            	if((x+1)%b ==0){
            		//cout << b << " " << (x+1)/b <<endl;
					bb=b,bbb=(x+1)/b;	
            		break;
				}	
			}
			if(abs(aa-aaa)>abs(bb-bbb))
			{
				cout << bb << " " << bbb << endl;
		    }
		    else 
		    {
		    	cout << aa <<" "<< aaa << endl;
			}  
        }
};

class String_machine:public Machine{
    public:
        String_machine(string type){this->type=type;}
        void welcome_message(){cout<<"Solving the "<<type<<" problem."<<endl;}

        void problem_solver(string str) {
        	int count = 1;
        	int array[str.length()];
        	int len=0;
        	int ans=0;
         	for(int a=0;a < str.length();a++){ 
         		if(str[a]==str[a+1]){
         			count = count + 1;
				}
				else{
					array[len] = count;
					len++;
					count = 1;
				} 
			}
			//cout << b <<endl;
			for(int a=0 ;a < len-1 ;a++){
				//cout << array[a] <<endl;
				if(array[a] > array[a+1]){
		    		//cout << array[a+1] << endl;
		    		ans += array[a+1];
			}
				else if(array[a] < array[a+1]){
					//cout << array[a] << endl;
					ans += array[a];
				}
				else{
					//cout << array[a] << endl;
					ans += array[a];
				}
			}
			cout << ans << endl;  
        }
};

int main(){

   string typenum= "";
   int x ;
   string str ;
   while(cin >> typenum){
	   	if(typenum =="math"){
		   	Math_machine m1(typenum);
		    m1.welcome_message();
		    cin >> x;
		    m1.problem_solver(x); 
	  	}
	   	else if(typenum =="string")
	    {
	   		String_machine m2(typenum);
			m2.welcome_message();
			cin >> str;
			m2.problem_solver(str); 
		}
	   else
	   {
	   		break;
		  // return 0;
	   }
   }
    return 0;
}
