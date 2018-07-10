Sebastian Cojocariu 311CB UPB ACS	

				                               Generic HashTable Data Structure

	Am inceput prin a creea functiile de afisare pentru student,materie,cheie de tip intreg si cheie de tip string(Afisare_Student,Afisare_Materie,Afisare_cheie_s,Afisare_cheie_d).Apoi,am creat functiile pentru comparare chei de tip intreg(f_comp_cheie_d),respectiv de tip string (f_comp_cheie_s).
  
	Totodata,am scris functia citire_student_materie (de tip void *) in care ,in functie de parametru d primit sa stim ce sa citim din fisierul din intrare.(d=1 inseamna ca citim un TStudent si facem alocarile corespunzatoare,respectiv d=2 pentru TMaterie).
	
	Functia aloca_celula (de tip TLG) citeste mai intai cheia (in functie de semnul dat ca parametru).In functie de stringul citit ( "stud" sau "mat") apeleaza functia citire_student_materie si initializeaza functiile de afisare_valoare,eliberare_valoare,cat si introduce adresa cheii in campul Info_celula alocat.celula->info va pointa catre pointerul Info_Celula initializat si completat mai sus,dupa care celula->urm=NULL;
  
	Functia HashTable *Init initializeaza hashul cu un nr egal cu numarul primit in parametrul d si,in functie de semnul cheii( 's' sau 'd') se atribuie functiile specifice cheii(cele pentru stringuri,respectiv cele pt intregi,dupa caz)
	
	Functia de Realocare_Hash realoca hashul dat ca parametru,dubland valoarae bucketului si apeland noua functie de hash pentru noul nr_bucket
	
	Functia Adaugare_Element_Hash adauga un TLG primit ca parametru in hash astfel: se ia cheia si se calculeaza intrarea in hash(cu functia hash_f).Se duce in lista corespunzatoare si se adauga la sfarsit daca cheia nu s-a mai gasit in aceasta ultima lista,sau sterge elementul cu aceeasi cheie din lista si il insereaza pe aceeasi pozitie cu acesta(il suprascrie)

	Functia delete e similara cheie de Adaugare_ELement_Hash,cu mentiunea ca sterge elementul fara a mai insera ceva in lista(pasii sunt cei prezentati anterior)

	In main citim mai intai prima linia si a 2a(ce reprezinta numarul de linii de citit din fisier).In stringul operatie se citeste cu un for fiecare operatie in parte si se apeleaza una din functiile de mai sus.(cu mici diferente,in functie de caz).

	Fisierul dezalocari.c contine functiile de dezalocari pentru info_celula,TLG,Hash,etc.
    
	Fisierul lib.h contine declaratiile pentru TStudent,TMaterie,HashTable si headerele unor functii;

