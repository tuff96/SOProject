# SOProject
C program find command

Scrieti un program C ce implementeaza urmatoarele functii, pentru o cale data sau pentru calea actuala:
 
1 afiseaza informatii despre fisiere folosind `stat.h`, dupa cum urmeaza:
 
        <numar inode> <tip fisier> <permisiuni> <numar linkuri> <userid> <groupid> <dimensiune> <timestamp creare> <nume fisier>
 
2 afiseaza informatii in mod recursiv pentru fisierele aflate in directoarele existente la calea specificata;
        2.1 trebuie implementata o optiune `--adancime-maxima` pentru a specifica pana la ce nivel se merge cu recursivitatea;
 
3 alte optiuni:

        3.1 --dim-max, --dim-min, pentru a afisa fisierele ce se incadreaza in intervalul specificat in bytes(B), megabytes(MB) sau gigabytes(GB);
        
        3.2 --hardlink-max, --hardlink-min, pentru a afisa fisierele ce se incadreaza in intervalul specificat numeric (ex: 1, 2, 3 samd.);
        
        3.3 --userid, --groupid, pentru a specifica o cautare dupa id-ul utilizatorului sau grupului asociat fisierului;
        
        3.4 --timestamp-min, --timestamp-max pentru a cauta fisiere create intr-un anumit interval;
        
        3.5 --timestamp-mdata-min, --timestamp-mdata-max, pentru a cauta fisiere modificate intr-un anumit interval;
        
        3.6 --permisiuni, pentru a cauta fisierele ce au setate anumite permisiuni (masca de permisiuni va fi declarata in formatul `rwxrwxrwx`);
        
        3.6 --iname, pentru a cauta fisiere al caror nume este reprezentat de expresia regulata definita (omitem `case-senzitive` si aplicam cautarea doar dupa numele scris cu caractere mici);
 
4 pentru fiecare fisier gasit, folosind optiunile de mai sus sau o combinatie a acestora, sa se poata executa o comanda folosind argumentul --exec urmat de o comanda externa, de exemplu:
 
        find --iname retele*.c --permisiuni rwxrwxrwx --exec "chmod 755"
