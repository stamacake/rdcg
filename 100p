//============================================================================
// Name        : lab12.cpp
// Author      : stamacake
// Version     : 1.1
// Copyright   : stamacake copyright
// Description : Radius, diameter and center of graph
//============================================================================

#include <iostream>

#include <vector>


#include <iomanip>
using namespace std;

int main() {
	const int N =4;
	const int inf = 9999;
	int n[N][N] = {
	//	1   .2  .3  .4
		inf,inf,5,inf, //1
		3,inf,inf,6, //2
		inf,4,inf,inf,  //3
		inf,inf,2,inf //4


	};



	int n2[N][N]={
			0,0,3,0,
			1,0,0,4,
			0,2,0,0,
			0,0,3,0

	};

	for (int i=0;i<N;i++){
		for (int j=0;j<N;j++){
			if(n[i][j]!=0){
			for (int k=0;k<N;k++){
					if(n[i][k]>n[i][j]+n[j][k]){
						n[i][k]=n[i][j]+n[j][k];
						n2[i][k]=n2[i][j];
						}
								}
			}
		}
	}

	for(int i=0;i<N;i++){
		for(int j=0;j<N;j++){
			cout<<setw(10)<<n[i][j]<<" ";
		}
		cout<<"\n";
	}

	int e1=inf;
	vector<int> r2;
	vector<int> e;
	int diametr=0;
	vector<int> center;

	for(int i=0;i<N;i++){
		e1=inf; // "обнуление" эксцентриситета
			for(int j=0;j<N;j++){ // поиск кандидатов на эксц-т
				if(n[i][j]<e1){
					r2.push_back(n[i][j]);
				}

		}
		int maxe=0; //макс кандидат эксц-та
		if(r2.size()!=0){
			for(auto aa:r2){
				if(aa>maxe){
					maxe=aa;
				}
			}
		e.push_back(maxe);
		}
		r2.clear();

	}

	int radius =inf;

	for(auto aa:e){
		if(aa<radius){
			radius=aa;
		}
		if(aa>diametr){
					diametr=aa;
				}

	}
int h=0;
for(auto aa:e){
	if(aa==radius){
		center.push_back(h+1);
	}
	h++;
}

	cout<<"radius= "<<radius<<endl;
	cout<<"diametr= "<<diametr<<endl;
	cout<<"centers: ";
	for(auto aa:center){
		cout<<aa<<" ";
	}

	return 0;
}
