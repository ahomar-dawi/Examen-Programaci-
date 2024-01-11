# Examen Presencial Programació

pseudocoid

EXERCICI 1
void decimalBinari(int decimal){  
    while(decimal/2!=0){  
        int binari=decimal%2;  
        print(binari);  
        decimal/=2;  
    }  
    print(1);  
}

EXERCICI 2  
void binariDecimal(long binari){  
    double decimal=0;  
    for(int i=0; decimal !=0; i++){  
        int digit = (int) binari%10;  
        decimal+=digit·2^i;  
        binari=binari/10;  
    }  
}
        
EXERCICI 3  
boolean esParell(int num){  
    if(num%2==0){  
        return true;  
    }else{  
    return false;  
    }  
}

EXERCICI 4  
void primersNombresParells(int num2){  
    for(int i=0; i<=num2; i++){  
        if(i%2==0){  
            print(i);  
        }  
    }  
}

EXERCICI 5  
int menu(int opcio){  
    print("Tria una de les següents opcions: ");  
    print("1. Decimal a binari");  
    print("2. Binari a decimal");  
    print("3. Es parell?");  
    print("4. Calcular parells de 0 a n");  
    print("0. Sortir");  
    input opcio();  
    retrun opcio;  
}

EXERCICI 6  
main{  
    menu(opcio);  
    if(opcio==0){  
        break;  
    }else if(opcio>4){  
        print("Opció no vàlida");  
        menu(opcio);  
    }else if(opcio==1){  
        print("Introdueix un nombre sencer decimal: ");  
        input int decimal();  
        decimalBinari(decimal);  
    }else if(opcio==2){  
        print("Introdueix un nombre sencer binari: ");  
        input long binari();   
        binariDecimal(binari);  
    }else if(opcio==3){   
        print("Introdueix un nombre sencer: ");  
        intput int num();  
        esParell(num);  
    }else if(opcio==4){  
        print("Introdueix un nombre sencer: ");  
        input int num2();  
        primersNombresParells(num2);  
    }  
    }

EXERCICI 7  
double volumCilindre(double radi, double long){  
    return pi·radi^2·long;
}

double volumPrismaRectangular(double c1, double c2, double c3){  
    return c1·c2·c3;
}

EXERCICI 8  
main{  
    int volum=0; int viatges=0;  
    print("Què has de transportar? 1. Líquids 2.Sòlids");  
    input int resposta();  
    if(resposta!=1||resposta!=2){  
        print("No és una opció vàlida");  
        print("Què has de transportar? 1. Líquids 2.Sòlids");  
        input resposta();  
    }else fi(resposta==1){  
        print("Quants de cm de radi té la cisterna? ");  
        input double radi();  
        print("Quants de cm de longitud té la cisterna? ");  
        input double long();  
        volum==volumCilindre(radi, long);  
    }else if(resposta==2){  
        print("Quants de cm de ample té la caixa? ");   
        input double c1();  
        print("Quants de cm de alt té la caixa? ");  
        input double c2();  
        print("Quants de cm de gruix té la caixa? ");  
        input double c3();  
        volum==volumPrisma(c1,c2,c3);  
    }  
    print("Quants metres cúbics hem de transportar? ");  
    input double m3();  
    print("El camió té capacitat per "+volum+" cm cúbics");  
    print("Hi caben "+volum/10^6+" metres cúbics");  
    viatges=(int)(m3/(volum/10^6));  
    viatges++;
    print("Has de fer "+viatges+" viatges");  
}
