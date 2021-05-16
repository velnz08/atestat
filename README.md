#include <iostream>
#include <fstream>
#include <string.h>

using namespace std;

int main()
{
    ///////////////////////////////////////////////////////////////
    //bilet 1 suma fractii
    /*
    ifstream file("date.in");
    int x,y,x1,y1,n;

    file >> n >> x >> y;
    while(file >> x1 >> y1)
    {
        x=x*y1+x1*y;
        y=y*y1;
    }

    int d=2;
    while(d<=y/2 && d<=x/2)
    {
        while(y%d==0 && x%d==0)
        {
            x=x/d;
            y=y/d;
        }
        d++;
    }

    file.close();
    ofstream file2("date.out");
    file2 << x << ' ' << y;
    file2.close();
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 2 cifra control
    ifstream file("date.in");
    int n,aux;
    file >> n;
    file.close();

    while(n>10)
    {
        aux=0;
        while(n)
        {
            aux=aux+n%10;
            n/=10;
        }
        n=aux;
    }

    ofstream file2("date.out");
    file2 << n;
    file2.close();
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 3 n zecimale

    ifstream file("date.in");
    int x,y,n;
    file >> x >> y >> n;
    file.close();

    ofstream file2("date.out");

    while(n)
    {
        while(x<y)
            x=x*10;

        while(x/y>0)
        {
            file2 << x/y;
            x=x-x/y*y;
        }

        n--;
    }

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 4 prime si invers

    ofstream file("date.out");
    int x,ogl,aux,ok;

    for(x=100;x<1000;x++)
    {
        ogl=0;
        aux=x;
        ok=1;
        for(int d=2;d<=x/2 && ok;d++)
            if(x%d==0)
                ok=0;

        if(ok)
        {
            while(aux)
            {
                ogl=ogl*10+aux%10;
                aux/=10;
            }

            for(int d=2;d<=aux/2 && ok;d++)
                if(aux%d==0)
                    ok=0;
        }

        if(ok)
            file << x << endl;
    }
    file.close();c
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 5 numar deosebit

    ifstream file("date.in");
    int n,p=0,aux,s,ok=1;
    file >> n;
    file.close();

    aux=n;

    while(aux)
    {
        p++;
        aux/=10;
    }
    aux=1;
    while(p)
    {
        aux*=10;
        p--;
    }
    p=aux;

    for(int i=n-n%(p/10);i<=n && ok;i++)
    {
        aux=i;
        s=0;
        while(aux)
        {
            s=s+aux%10;
            aux/=10;
        }
        if(i+s==n)
            ok=0;
    }
    ofstream file2("date.out");
    if(ok==0)
        file2 << "DA";
    else file2 << "NU";

    file2.close();
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 6 numar deosebit

    ifstream file("date.in");
    int n,p=1,s=0,k=1,aux=0;
    file >> n;

    for(int i=1;i<=n;i++)
    {
        aux=i;
        while(aux)
        {
            s++;
            aux/=10;
        }
    }

    file.close();

    ofstream file2("date.out");
    file2 << s;
    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 7 termeni fibonacci consecutivi

    ifstream file("date.in");
    int a,b,x1=0,x2=1,fibb=1;
    file >> a >> b;
    file.close();

    if(a>b)
    {
        x1=a;
        a=b;
        b=x1;
    }
    x1=0;

    while(fibb<a)
    {
        fibb=x2+x1;
        x1=x2;
        x2=fibb;
    }
    ofstream file2("date.out");

    if(fibb==a && fibb+x1==b)
        file2 << "DA";
    else file2 << "NU";

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 8 suma de numere consecutive

    ifstream file("date.in");
    int n,k,s,aux;
    file >> n;
    file.close();
    ofstream file2("date.out");
    for(int i=1;i<n;i++)
    {
        k=1;
        s=i;
        aux=i+1;
        while(s<n)
        {
            s=s+aux;
            aux++;
            k++;
        }

        if(s==n)
        {
            while(k)
            {
                file2 << aux-k << ' ';
                k--;
            }
            file2 << endl;
        }
    }

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 9 super prim
    ifstream file("date.in");
    int n,ok=1,aux,p=1;
    file >> n;
    file.close();
    aux=n;
    while(aux && ok)
    {
        for(int i=2;i<aux/2 && ok;i++)
            if(aux%i==0)
                ok=0;
        aux/=10;
        p*=10;
    }
    ofstream file2("date.out");
    if(ok)
    {
        file2 << "DA" << endl;

        while(p>10)
        {
            file2 << n/(p/10) << endl;
            p/=10;
        }
    }
    else file2 << "NU";
    file2.close();
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 10 apropiat prim
    ifstream file("date.in");
    int n,ok,i,d,ok2=1,ok3=1;
    file >> n;
    file.close();

    for(i=0;ok2 && ok3;i++)
    {
        ok=1;
        for(d=2;d<=(n-i)/2 && ok;d++)
            if((n-i)%d==0)
                ok=0;
        if(ok && n-i>1)
            ok2=0;
        ok=1;
        for(d=2;d<=(n+i)/2 && ok;d++)
            if((n+i)%d==0)
                ok=0;
        if(ok && n+i>1)
            ok3=0;
    }

    ofstream file2("date.out");
    if(!ok2)
    {
        file2 << n-i+1 << endl;
    }
    else if(!ok3)
        file2 << n+i-1 << endl;
    file2.close();
    */
    ///////////////////////////////////////////////////////////////
    /*bilet 11 cate elemente fibonacci

    ifstream file("date.in");
    int n,a,x1=0,x2=1,fibb=1,s=0;
    file >> n;

    while(file >> a)
    {
        while(fibb<a)
        {
            fibb=x2+x1;
            x1=x2;
            x2=fibb;
        }
        if(fibb==a)
            s++;
        x1=0;
        x2=1;
        fibb=1;
    }
    file.close();

    ofstream file2("date.out");
    file2 << s;

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 12 vector multime

    ifstream file("date.in");
    int n,v[101],a,k=0,i,j;
    file >> n;

    while(file >> a)
    {
        v[k]=a;
        k++;
    }
    file.close();

    i=0;
    while(i<k)
    {
        j=i+1;
        while(j<k)
        {
            if(v[i]==v[j])
            {
                for(int l=j;l<k;l++)
                    v[l]=v[l+1];
                k--;
            }
            else j++;
        }
        i++;
    }

    ofstream file2("date.out");
    for(i=0;i<k;i++)
        file2 << v[i] << ' ';

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 13 elemente mai mici

    ifstream file("date.in");
    int n,minn,m,a,s=0,k=1;
    file >> n >> minn;

    while(k<n)
    {
        file >> a;
        if(minn>a)
            minn=a;
        k++;
    }
    k=0;
    file >> m;
    while(k<m)
    {
        file >> a;
        if(minn>a)
            s++;
        k++;
    }
    file.close();

    ofstream file2("date.out");
    file2 << s;
    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 14 suma numere mari
    //necesita biblioteca <string.h>           #include <string.h>
    ifstream file("date.in");

    char num1[100],num2[100],num3[200]="0";
    int i,k,d=0,e,f;
    file >> num1 >> num2;
    file.close();
    i=strlen(num1)-1;
    k=strlen(num2)-1;

    strrev(num1);
    strrev(num2);
    i=0;
    k=0;
    d=0;
    while(i<strlen(num1) || k<strlen(num2))
    {
        num3[d+1]='0';
        e=num1[i];
        f=num2[k];

        if(i<strlen(num1) && k<strlen(num2))
            num3[d]=num3[d]+e-'0'+f-'0';
        else if(i<strlen(num1))
                num3[d]=e;
                else if(k<strlen(num2))
                    num3[d]=f;

        while(num3[d]>'9')
        {
            num3[d+1]++;
            num3[d]=num3[d]+'0'-'9'-1;
        }
        i++;
        k++;
        d++;
    }

    num3[d]='\0';
    strrev(num3);
    ofstream file2("date.out");
    file2 << num3;
    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 15 interclasare
    ifstream file("date.in");

    int a[101],d=0,n,j,aux;
    file >> n;
    while(d<n)
    {
        file >> a[d];
        d++;
    }
    file.close();

    for(d=0;d<n;d++)
    {
        for(j=0;j<n;j++)
        {
            if(a[d]<a[j])
            {
                aux=a[d];
                a[d]=a[j];
                a[j]=aux;
            }
        }
    }

    ofstream file2("date.out");
    for(d=0;d<n;d++)
        file2 << a[d] << ' ';
    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 16 maximul
    ifstream file("date.in");

    int a[101]={0},b[101]={0},d=0,n,j=0,aux,ok=0,maxx=0;
    file >> n;
    while(d<n)
    {
        ok=0;
        file >> aux;
        for(j=0;j<d && !ok;j++)
        {
            if(a[j]==aux)
                ok=1;
        }
        if(ok)
            b[j-1]++;
        else a[d]=aux;

        d++;
    }
    file.close();

    for(d=0;d<n;d++)
        if(maxx<b[d])
            maxx=b[d];

    ofstream file2("date.out");
    for(d=0;d<n;d++)
        if(maxx==b[d])
            file2 << a[d] << ' ';

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 17 numar aparitii
    ifstream file("date.in");

    int v[101]={0},w[101]={0},n,d=0,j=0;
    file >> n;
    while(file >> v[d])
        d++;

    file.close();

    for(d=0;d<n;d++)
        for(j=0;j<n;j++)
            if(v[d]==v[j])
                w[d]++;

    ofstream file2("date.out");
    for(d=0;d<n;d++)
        file2 << v[d] << ' ';
    file2 << endl;
    for(d=0;d<n;d++)
        file2 << w[d] << ' ';

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 18 numar aparitii
    ifstream file("date.in");

    int n,v[21][21],k=0,x1=0,x2=1,fibb=1,i=0;
    file >> n;
    file.close();

    while(k<n*n)
    {
        v[i][k%n]=fibb;
        fibb=x1+x2;
        x1=x2;
        x2=fibb;

        if((k+1)%n==0)
            i++;
        k++;
    }

    ofstream file2("date.out");
    for(int d=0;d<n;d++)
    {
        for(int k=0;k<n;k++)
        {
            file2 << v[d][k] << ' ';
        }
        file2 << endl;
    }

    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 19 suma elemente impare nord
    ifstream file("date.in");

    int n,v[21][21],s=0;
    file >> n;
    for(int i=0;i<n;i++)
        for(int j=0;j<n;j++)
            file >> v[i][j];
    file.close();

    for(int i=0;i<n;i++)
        for(int j=0;j<n;j++)
            if(j>i && j<n-i-1 && v[i][j]%2)
                s+=v[i][j];

    ofstream file2("date.out");
    file2 << s;
    file2.close();*/
    ///////////////////////////////////////////////////////////////
    /*bilet 20 cuvinte distincte*/
    //necesita <string.h>         #include <string.h>
    ifstream file("date.in");

    int i=0;
    char text[21],aux[21];
    file >> text;
    file.close();

    ofstream file2("date.out");
    for(i=0;i<strlen(text);i++)
    {
        if(text[i]!=text[i+1])
        {
            strncpy(aux,text,i);
            strcpy(aux+i,text+i+1);
            file2 << aux << endl;
            strcpy(aux,"");
        }
    }
    file2.close();
    ///////////////////////////////////////////////////////////////
    return 0;
}
