# Què hi ha de nou al NVDA


## 2015.4

### Noves característiques

* NVDA apareix ara en el Centre d'accessibilitat del Windows 8 i versions posteriors. (#308)
* Al moure't al voltant de les cel·les a l'Excel, s'informa automàticament dels canvis de format si s'ha activat l'opció corresponent en el diàleg de configuració de formatació de documents del NVDA. (#4878)

### Correccions d'errors

* Millores de rendiment en la navegació a la llista de missatges d'Outlook 2010/2013. (#5268)
* Ara, en els gràfics del Microsoft Excel, la navegació amb certes tecles (com canviar els fulls amb  Ctrl+RePag i Ctrl+AvPag) funciona correctament. (#5336)
* S'ha corregit l'aparença visual dels botons en el diàleg d'alerta que es mostra quan canvies a una versió anterior de NVDA. (#5325)
* Al Windows 8 o versions posteriors, NVDA ara comença molt abans si es configura per començar després de l'inici del Windows. (#308)
 * Si vas activar aquesta funció en una versió anterior del NVDA, hauràs de desactivar-la i activar-la de nou en el diàleg de Configuració general per a què el canvi sigui efectiu.
* Millores de rendiment per UI Automation, que inclouen l'explorador de fitxers i el visor de tasques. (#5293)

## 2015.3

Aquesta versió destaca per incloure suport inicial al Windows 10; la possibilitat de desactivar navegació per lletra en mode de navegació (útil per algunes aplicacions web); millores al Internet Explorer; i correccions per text il·legible en algunes aplicacions, quan el braille està activat.

### Noves característiques

* S'anuncien els errors d'ortografia en els camps d'edició a l'Internet Explorer i en d'altres controls MSHTML. (#4174)
* Molts més símbols matemàtics UNICODE es lletrejen quan apareixen al text. (#3805)
* S'informa automàticament dels suggeriments de cerca a la pantalla d'inici del Windows 10. (#5049)
* NVDA és compatible amb els terminals braille EcoBraille 20, EcoBraille 40, EcoBraille 80 i EcoBraille Plus. (#4078)
* En el mode de navegació, pots activar i desactivar la navegació per lletra prement NVDA+Maj+Espai. quan la navegació per lletra està desactivada, les lletres s'envien a l'aplicació, la qual cosa és útil per a algunes aplicacions web com el Gmail, el Twitter o el Facebook. (#3203)
* Noves taules de traducció Braille: Finès 6 punts, Irlandès grau 1, Irlandès grau 2, Coreà grau 1 (2006), Coreà grau 2 (2006). (#5137, #5074, #5097)
* Compatible amb el teclat QWERTY del terminal braille Papenmeier BRAILLEX Live Plus. (#5181)
* Suport experimental per al navegador Microsoft Edge i per al motor de navegació del Windows 10. (#5212)
* Nou idioma: Canadenc.

### Canvis

* Traductor liblouis braille actualitzat a la versió 2.6.3. (#5137)
* Quan proves d'instal·lar una versió anterior del programa de la que ja està instal·lada, ara NVDA t'avisarà que no és recomanable fer-ho i que cal desinstal·lar completament NVDA abans de res. (#5037)

### Correccions d'errors

* En el mode de navegació a l'Internet Explorer i a d'altres controls MSHTML, la navegació ràpida per formulari ja no inclou els elements de llista de presentació. (#4204)
* Al Firefox, NVDA ja no informa incorrectament del contingut en el panell de la pestanya ARIA quan el focus s'hi desplaça. (#4638)
-A l'Internet Explorer i altres controls MSHTML, NVDA ja no informa incorrectament del contingut dels contenidors quan et desplaces amb el tabulador a dins de seccions, articles o diàlegs. (#5021, #5025)
* Quan s'usen els terminals braille Baum/Humanware/APH Braille Displays  amb un teclat braille, l'entrada de braille ja no s'atura després de prémer algun altre tipus de tecla al terminal. (#3541)
* Al Windows 10, quan es commuta entre aplicacions amb Alt+Tab o Alt+Maj+Tab ja no s'informa d'informació estranya. (#5116)
* El text escrit no es torna il·legible quan s'usen aplicacions com el Microsoft Outlook amb un terminal braille. (#2953)
* En el mode de navegació a l'Internet Explorer i altres controls MSHTML, s'informa correctament del contingut quan un element apareix o canvia i rep el focus immediatament. (#5040)
* En el mode de navegació al Microsoft Word, la navegació per lletra actualitza el terminal braille i el cursor de text com seria d'esperar. (#4968)
* A braille, ja no es mostren espais estranys entre o després dels indicadors de control o format. (#5043)
* Quan una aplicació respon lentament i en surts, la majoria de vegades NVDA respon molt més ràpidament. (#3831)
* Al Windows 10 s'informa de les notificacions del sistema correctament. (#5136)
* En alguns (UI Automation) quadres combinats, s'anuncien correctament els canvis de valor, allà on no funcionava anteriorment.
* en mode de navegació  en els navegadors web, el tabulat funciona correctament quan es tabula a un document amb marcs. (#5227)
* La pantalla de bloqueig de Windows 10 es pot obviar amb una pantalla tàctil. (#5220)
* Al Windows 7 i versions posteriors, el text ja no resulta intel·ligible quan s'escriu des d'aplicacions com el Wordpad o l'Skype amb un terminal braille. (#4291)
* A la pantalla de bloqueig del Windows 10, no es permet llegir el porta-retalls, accedir a les aplicacions en execució amb el cursor de revisió o canviar la configuració NVDA. (#5269)

### Canvis per desenvolupadors

* Ara pots introduir dades en brut des d'un teclat de sistema que Windows no gestiona de forma nadiua (per exemple, un teclat QWERTY en un terminal braille) amb la nova funció keyboardHandler.injectRawKeyboardInput. (#4576)
* s'ha afegit eventHandler.requestEvents per demanar alguns esdeveniments que per defecte estan bloquejats; per exemple mostra esdeveniments d'un control en particular o alguns esdeveniments que s'executen en segon pla (#3831)
* En comptes d'un únic atribut i18nName, ara synthDriverHandler.SynthSetting té dos atributs separats, displayNameWithAccelerator i displayName per evitar informar de l'accelerador en el menú de configuració del sintetitzador en alguns idiomes.
 * Per motius de compatibilitat cap enrere, en el constructor, el displayName és opcional i, en cas que no s'indiqui, es dedueix de displayNameWithAccelerator. De totes maneres, si vols disposar d'un accelerador per a una configuració, hauries d'indicar-los ambdós.
 * L'atribut i18nName està desfasat, i es podria eliminar en properes versions.

## 2015.2

Aquesta versió destaca per la capacitat de llegir gràfics al Microsoft Excel i per ser compatible amb la lectura i la navegació ineractiva del contingut matemàtic.

### Noves característiques

* Ara és possible moure's endavant i enrera per frases al Microsoft Word i a l'Outlook amb Alt+fletxa avall i Alt+Fletxa amunt respectivament. (#3288)
* Noves taules de traducció braille per diversos idiomes de l'Índia. (#4778)
* A Microsoft Excel, ara NVDA Informa quan una cel·la té contingut tallat o que desborda la cel·la. (#3040)
* A Microsoft Excel, pots usar la llista d'elements (NVDA + Tecla de funció 7) per llistar els gràfics, comentaris i fòrmules. (#1987)
* Compatible amb la lectura de gràfics al Microsoft Excel. Per a fer servir aquesta funció, selecciona el gràfic amb la llista d'elements (NVDA + Tecla de funció 7) i llavors usa les tecles de fletxa per moure't entre els diferents punts de dades. (#1987)
* Amb MathPlayer 4 de Design Science, NVDA ara pot llegir i navegar interactivament pel contingut matemàtic en els navegadors web, al Microsoft Word i a PowerPoint. Per a més informació, consulta la secció "Lectura de contingut matemàtic" a la Guia d'usuari. (#4673)
* Ara és possible assignar gestos d'entrada (ordres de teclat, Gestos tàctils, etc.) a tots els diàlegs de preferències de NVDA i a les opcions de format de documents amb el diàleg de gestos d'entrada. (#4898)

### Canvis

* En el diàleg NVDA de formatació del document, les dreceres de teclat per informar sobre llistes, informar sobre els enllaços, informar sobre el número de línia i informar del tipus de lletra han canviat. (#4650)
* Al diàleg NVDA de configuració del ratolí, s'han afegit dreceres de teclat per emetre les coordenades per àudio quan el ratolí es mou i la brillantor controla el volum de l'àudio. (#4916)
* Millora important de la informació dels noms de color. (#4984)
* Traductor Liblouis braille actualitzat a la versió 2.6.2. (#4777)

### Correccions d'errors

* La descripció de caràcters per lligadures d'alguns idiomes d'Índia ara es gestionen correctament. (#4582)
* Si està activada l'opció "Confia en l'idioma de veu per al processat de caràcters i símbols", el diàleg de pronunciació de puntuació i símbols ara usa correctament l'idioma de veu. A més, l'idioma del qual s'està editant la pronunciació es mostra en el títol del diàleg. (#4930)
* A l'Internet Explorer i altres controls MSHTML, ja no s'anuncien els caràcters escrits en camps de quadre editables com el camp de cerca de Google a la pàgina inicial de Google. (#4976)
* Quan se seleccionen colors a les aplicacions del Microsoft Office, ara s'informa dels noms dels colors. (#3045)
* La sortida braille en Danès torna a funcionar. (#4986)
* Re Pàg/Av Pag es pot tornar a usar per desplaçar-se entre les diapositives d'una presentació PowerPoint. (#4850)
* A l'Skype per sobretaula 7.2 i versions posteriors, s'informa dels avisos d'introduccio de dades, i s'han resolt els problemes que es donaven just després de moure el focus fora d'una conversa. (#4972)
* S'han resolt els problemes que apareixien quan s'introduïen alguns símbols o puntuació, com parèntesis, en el camp de filtre del diàleg de gestos d'entrada. (#5060)
* a l'Internet Explorer i altres controls MSHTML, la navegació per gràfics amb g o Maj+g ara inclou elements marcats com a imatges per raons d'accessibilitat (per exemple rol img d'ARIA). (#5062)

### Canvis per desenvolupadors

* brailleInput.handler.sendChars(mychar) no obviarà un caràcter pel fet de ser el mateix que l'anterior i garantirà que la tecla de tramesa s'ha deixat anar correctament. (#4139)
* Els scripts per canviar els modes tàctils ara tindran en compte les noves etiquetes afegides a touchHandler.touchModeLabels. (#4699)
* Les extensions podran oferir la seva pròpia implementació de presentació del contingut matemàtic. Per a més informació, vegeu el paquet mathPres. (#4509)
* S'han creat ordres de veu per insertar una pausa entre paraules, per canviar el to, el volum o la velocitat. Vegeu BreakCommand, PitchCommand, VolumeCommand i RateCommand en el mòdul de parla. (#4674)
 * També s'ha creat l'ordre speech.PhonemeCommand per introduir una pronúncia específica, però la implementació actual inclou un número molt límitat de fonemes.

## 2015.1

Aquesta versió destaca per incloure el mode de navegació per a documents en el Microsoft Word i l'Outlook; millores importants de compatibilitat amb l'Skype per ordinadors de sobretaula; i correccions imporants d'errors en el Microsoft Internet Explorer.

### Noves característiques

* Pots afegir nous símbols an al diàleg de Pronunciació de símbols. (#4354)
* En el diàleg de gestos d'entrada, pots usar el camp "filtrar per" per mostrar només aquells gestos que inclouen certes paraules. (#4458)
* NVDA informa automàticament de text nou a mintty. (#4588)
* En el mode de navegació, al diàleg de Cerca, ara hi ha l'opció de fer una cerca tenint en compte majúscules i minúscules. (#4584)
* navegació ràpida (Si prems h per moure't per encapçalaments, etc.) i ara està disponible la llista d'elements (NVDA+tecla de funció 7) als documents Microsoft Word si s'activa el mode de navegació amb NVDA+Espai. (#2975)
* S'ha millorat molt la lectura dels missatges HTML a Microsoft Outlook 2007 i versions posteriors ja que el mode de navegació està activat automàticament per aquests missatges. Si el mode de navegació no s'activa en algunes situacions especials, pots forçar-lo amb NVDA+Espai. (#2975)
* NVDA informa automàticament de les capçaleres de columna de taula quan els autors han especificat explícitament que una fila és capçalera en les propietats de la taula al Microsoft Word. (#4510)
 * De totes maneres, a les taules en les que les files s'han combinat, això no funciona automàticament. En aquesta situació, també pots indicar les capçaleres de columna manualment amb NVDA+Maj+c
* A l'Skype per ordinadors de sobretaula, ara s'informa de les notificacions. (#4741)
* A l'Skype per ordinadors de sobretaula, pots llegir i revisar els missatges recents amb NVDA+Ctrl+1 fins a NVDA+Ctrl+0; per exemple NVDA+Ctrl+1 per el missatge més recent i NVDA+Ctrl+0 per el desè més recent. (#3210)
* A l'Skype per ordinadors de sobretaula, NVDA Informa quan un dels contactes està escrivint. (#3506)
* NVDA es pot instal·lar sense veu amb la línia de comandes sense engegar la còpia instal·lada després de la instal·lació. Per fer-ho, utilitzeu l'opció --instal·lació-silenciosa. (#4206)
* NVDA és compatible amb els terminals Braille Papenmeier BRAILLEX Live 20, BRAILLEX Live i BRAILLEX Live plus. (#4614)

### Canvis

* L'opció d'informar dels errors ortogràfics, al diàleg NVDA de configuració de format del document ara té una drecera associada  (Alt+r). (#793)
* NVDA usarà ara l'idioma del sintetitzador/de la veu per lletrejar els caràcter i símbols (inclosos la puntuació/i els noms de símbols),  sense tenir en compte si s'ha activat la commutació d'idioma automàtica. Per desactivar aquest funcionament, i fer que NVDA  torni a usar l'idioma de la interfície, desactiveu la nova opció a la  Configuració de veu anomenada Confia en l'idioma de veu per processar caràcters i símbols. (#4210)
* Ja no és compatible amb el sintetitzador Newfon. Newfon ara està disponible com a extensió NVDA. (#3184)
* Cal la versió 7 o superior de l'Skype per ordinadors de sobretaula per treballar amb NVDA; NVDA no és compatible amb versions anteriors. (#4218)
* La descàrrega de les actualitzacions de NVDA ara és més segura (específicament, la informació d'actualització es recupera per https i el codi hash del fitxer es verifica després de la descarrega). (#4716)
* S'ha actualitzat eSpeak a la versió 1.48.04. (#4325)

### Correccions d'errors

* Al Microsoft Excel, els encapçalaments de files i columnes combinades ara es gestionen correctament. Per exemple, si A1 i B1 es combinen, llavors B2 indicarà que les seves capçaleres són A1 i B1, en comptes de cap capçalera. (#4617)
* Quan s'edita el contingut d'una caixa de text al Microsoft PowerPoint 2003, NVDA informarà correctament del contingut de cada línia. prèviament, a cada paràgraf, les línies es desplaçaran automàticament per un caràcter de forma incremental. (#4619)
* Tots els diàlegs de NVDA se centren actualment a la pantalla, millorant la presentació visual i la usabilitat. (#3148)
* A l'Skype per ordinadors de sobretaula, quan s'entra un missatge de presentació per afegir un contacte, funciona correctament l'entrada i desplaçament pel text. (#3661)
* Quan el focus es mou a un nou element en una vista d'arbre a l'entorn de desenvolupament Eclipse, si l'anterior element que tenia el focus era una casella de verificació, aquesta ja no s'anuncia incorrectament. (#4586)
* En el menú de verificació d'ortografia del Microsoft Word, s'anunciarà automàticament el següent error quan l'anterior s'hagi canviat o ignorat amb les respectives tecles de drecera. (#1938)
* de nou és possible llegir correctament el text en llocs com el terminal Windows de Tera Term Pro o en els documents de Balabolka. (#4229)
* Ara el focus torna correctament al document en edició, quan es finalitza la composició de text coreà o d'altres idiomes asiàtics, mentre s'edita dins un marc a Internet Explorer i altres documents MSHTML. (#4045)
* En el diàleg de gestos d'entrada, quan s'escull una disposició de teclat per al gest de teclat que es vol afegir, si prems Escapada ara tanca el menú en comptes del diàleg, tal i com seria d'esperar. (#3617)
* Quan s'elimina una extensió, la carpeta de l'extensió s'esborra correctament després de reinicialitzar NVDA. prèviament, has de reiniciar dues vegades. (#3461)
* S'han corregit problemes importants a l'Skype per ordinadors de sobretaula, versió 7. (#4218)
* quan envies un missatge l'Skype per ordinadors de sobretaula, ja no es llegeix dues vegades. (#3616)
* A l'Skype per ordinadors de sobretaula, NVDA no hauria de llegir puntualment i erròniament un gran bloc de missatges (fins i tot una conversació sencera). (#4644)
* s'ha corregit un problema en el què, ocasionalment, l'ordre NVDA Anuncia la data i l'hora no feia cas de la configuració regional especificada per l'usuari. (#2987)
* En el mode de navegació, ja no es mostra text sense sentit (de vegades ocupava diverses línies) per alguns gràfics com els que es troben en els grups de Google. (específicament, això passava amb les imatges codificades en base64.) (#4793)
* NVDA no s'hauria d'aturar després d'uns quants segons quan desplaces el focus fora de l'app de la botiga Windows, ja que queda en suspens. (#4572)
* Ara NVDA té en compte l'atribut aria-atomic de les regions actives a Mozilla Firefox fins i tot quan el propi element canvia. prèviament, només afectava als elements descendents. (#4794)
* El mode de navegació mostrarà les actualitzacions, i s'informarà de les regions actives, pels documents en mode de navegació dins d'aplicacions ARIA incrustades en un document a Internet Explorer o altres controls MSHTML. (#4798)
* Quan es canvia o s'afegeix text en una regió activa a Internet Explorer i altres controls MSHTML en la que l'autor ha especificat que el text és important, només s'anuncia el text canviat o afegit, en comptes d'anunciar tot el text de l'element contenidor. (#4800)
* El contingut indicat segons l'atribut aria-labelledby a Internet Explorer i altres controls MSHTML reemplaça el contingut original quan és pertinent fer-ho. (#4575)
* Quan es revisa l'ortografia amb el Microsoft Outlook 2003, ara s'informa de la paraula mal escrita. (#4848)
* A Internet Explorer i altres controls MSHTML, el contingut dintre d'elements amagats amb visibility:hidden ja no es mostra en mode de navegació. (#4839, #3776)
* A Internet Explorer i altres controls MSHTML, l'atribut del títol en els controls de formulari ja no té preferència sobre altres etiquetes associades. (#4491)
* A Internet Explorer i altres controls MSHTML, NVDA ja no ignora el focus d'elements gràcies a l'atribut aria-activedescendant. (#4667)

### Canvis per desenvolupadors

* wxPython s'ha actualitzat a la versió 3.0.2.0. (#3763)
* Python s'ha actualitzat a la versió 2.7.9. (#4715)
* NVDA ja no peta quan es reinicia després d'haver esborrat o actualitzat una extensió que importa el speechDictHandler en el seu mòdul installTasks. (#4496)

## 2014.4

### Noves característiques

* Nous idiomes: Espanyol colombià, Punjabi.
* Ara és possible triar si es reinicia NVDA normalment o amb les extensions desactivades des del diàleg de sortida de NVDA. (#4057)
* NVDA també es pot iniciar amb les extensions desactivades amb l'opció de línia de comandes --disable-addons.
* En els diccionaris de veu, ara és possible especificar que un patró només s'apliqui si és una paraula sencera; és a dir, el patró no és part d'una paraula més llarga. (#1704)

### Canvis

* Si un objecte al que t'has mogut amb la navegació d'objectes es troba dins un document en mode de navegació, però l'objecte d'on venies no, s'activa el mode de revisió de manera automàtica en el document. prèviament, això només passava si l'objecte de navegació es movia a causa d'un canvi de focus. (#4369)
* la llista de terminals braille i de sintetitzadors en els respectius diàlegs de configuració apareixen ordenats alfabèticament excepte per les opcions Sense braille/Sense veu, que apareixen al final. (#2724)
* Traductor liblouis braille actualitzat a la versió 2.6.0. (#4434, #3835)
* en mode de navegació, la navegació als camps d'edició amb e i Maj+e ara inclou els quadres combinats. Això inclou la caixa de cerca a la darrera versió de Cerca Google. (#4436)
* Si cliques la icona NVDA a l'àrea de notificació amb el botó esquerre del ratolí, s'obre el menú NVDA en comptes de no fer res. (#4459)

### Correccions d'errors

* Quan desplaces el focus enrere a un document en mode de navegació (per exemple Alt+Tab a una pàgina web ja oberta), el cursor de revisió es posiciona correctament al cursor del sistema virtual, en comptes de en el control que rep el focus (per exemple enllaç). (#4369)
* A les presentacions PowerPoint, el cursor de revisió segueix correctament el cursor del sistema. (#4370)
* Al Mozilla Firefox i altres navegadors basats en Gecko, el nou contingut en una regió activa s'anunciarà fins i tot si el nou contingut té un tipus de regió ARIA activa diferent que la regió activa pare;  per exemple, quan el contingut marcat com a assertiu s'afegeix a una regió marcada com a polite. (#4169)
* A Internet Explorer i altres controls MSHTML, alguns casos en els que un document està inclòs en un altre document, ja no impedeixen a l'usuari que accedeixi a part dels continguts (específicament, en marcs dins de marcs). (#4418)
* NVDA no peta quan prova d'usar el terminal braille Handy Tech en alguns casos. (#3709)
* A Windows Vista, ja no es mostra un fals diàleg "Punt d'entrada no trobat" en diversos casos, com quan s'inicia NVDA des de la tecla de drecera de l'escriptori o via la tecla de drecera. (#4235)
* S'han corregit problemes seriosos amb els controls de textos d'edició en els diàlegs de les versions recents d'Eclipse. (#3872)
* A Outlook 2010, moure el cursor ara funciona tal i com seria d'esperar al camp d'ubicació de cites i peticions de trobada. (#4126)
* Dins d'una regió activa, el contingut que està marcat com a no actiu (per exemple aria-live="off") ara s'ignora, correctament. (#4405)
* quan s'informa del text d'una barra d'estat que té un nom, ara el nom se separa correctament de la primera paraula del text de la barra d'estat. (#4430)
* En els camps d'entrada de contrasenyes, quan està activada l'opció de verbalitzar les paraules escrites, no s'informa ja inútilment de múltiples asteriscs a l'inici de les paraules. (#4402)
* A la llista de missatges del Microsoft Outlook, els elements no s'anuncien ja inútilment com a elements de dades. (#4439)
* En seleccionar el text en el editor de codi de l'IDE de l'Eclipse, no s'anunciarà la selecció sencera cada vegada que canvií. (#2314)
* Diverses versions de l'Eclipse, com Spring Tool Suite i la versió inclosa al Android Developer Tools bundle, ara són reconegudes com a Eclipse i gestionades apropiadament. (#4360, #4454)
* El control del ratolí i l'exploració tàctil al Internet Explorer i a d'altres controls MSHTML (incloses diverses aplicacions per al Windows 8) són més precises en pantalles amb alta resolució o quan el zoom del document canvia. (#3494) 
* Ara, el control del ratolí i l'exploració tàctil al Internet Explorer i a d'altres controls MSHTML anuncien l'etiqueta de més butons. (#4173)
* Ara, en utilitzar el terminal braille Papenmeier BRAILLEX amb BrxCom, les tecles de la pantalla funcionen correctament. (#4614)

### Canvis per desenvolupadors

* Per als executables que contenen diferents aplicacions (per exemple, javaw.exe), ara, el codi es pot proporcionar per carregar mòduls específics de l'aplicació per a cada aplicació, en comptes de carregar el mateix mòdul per a totes les aplicacions que conté l'executable. (#4360)
* Vegeu la documentació del codi del appModuleHandler.AppModule per saber-ne més.
* S'ha implementat el suport per javaw.exe.

## 2014.3

### Noves característiques

* Els sons reproduïts quan NVDA s'inicia i s'atura poden ser desactivats a partir d'una nova opció disponible al menú de paràmetres generals. (#834)
* En el cas dels connectors suportats per NVDA, es pot accedir a la seva ajuda des del gestor de connectors. (#2694) 
* Suport per al calendari del Microsoft Outlook 2007 i posteriors (#2943) inclou:
* L'anunci de l'hora actual quan l'usuari es desplaça amb les tecles del cursor.
* La indicació de si l'hora seleccionada es troba dins d'alguna cita.
* L'anunci de la cita seleccionada en polsar el tabulador.
* Filtrat intel·ligent de la data per anunciar-la només en el cas que la nova hora o cita seleccionada sigui en un dia diferent a aquesta.
* Millora del suport a la safata d'entrada i a d'altres tipus de llistes de missatges al Microsoft Outlook 2010 i posteriors (#3834) incloent-hi:
* La capacitat de silenciar els encapçalaments de columna (de, assumpte, etc.) desactivant l'opció de l'informe de files i encapçalaments de taules als paràmetres del format del document.
* La capacitat d'utilitzar els controls de navegació per les taules (control + alt + fletxes) per moure's a través de les columnes individuals.
* Microsoft Word: Si una imatge en línia amb el text no té cap text alternatiu, NVDA informarà del títol de la imatge en el cas que l'autor n'hagi proporcionat un. (#4193)
* Microsoft Word: NVDA ja pot informar del sagnat dels paràgrafs amb l'ordre d'informe de format del text (NVDA+f). També en pot informar automàticament quan la nova opció Informe del sagnat del paràgraf, es troba activada en els paràmetres del format del document. (#4165)
* Informa automàticament del text inserit com un nou pic de llista, número o sagnat amb el tabulador, en polsar la tecla de retorn en els documents editables i els camps de text. (#4185)
* Microsoft Word: Polsant NVDA+alt+c s'informa del text d'un comentari en el cas que el cursor sigui dins d'aquest. (#3528)
* Suport millorat per a la lectura automàtica dels encapçalaments de columnes i files al Microsoft Excel (#3568) incloent-hi:
-Suport en els noms de rangs definits per identificar les d'encapçalaments (compatible amb el lector de pantalla Jaws).
* Ara, les ordres per especificar un encapçalament de columna (NVDA+shift+c) i de fila (NVDA+shift+r) emmagatzemen aquests paràmetres en el full de càlcul, de manera que estaran disponibles la propera vegada que s'obri el full i, també, per altres lectors de pantalla que en donin suport.
* Aquestes ordres també poden ser utilitzades diverses vegades per cadascun dels fulls, per tal d'establir diferents encapçalaments de diferents regions.
* Suport per a la lectura automàtica d'encapçalaments de columnes i files al Microsoft Word (#3110), incloent-hi:
* Suport en els marcadors del Microsoft Word per identificar cel·les d'encapçalaments (compatible amb Jaws).
* Les ordres per especificar un encapçalament de columna (NVDA+shift+c) i de fila (NVDA+shift+r) et permeten comunicar a NVDA, sempre que es tracti de la primera cel·la de l'encapçalament d'una taula, que ha d'informar automàticament d'aquests encapçalaments. Els paràmetres s'emmagatzemen en el document, de manera que estaran disponibles la propera vegada que s'obri el document, i també per altres lectors de pantalla que ho suportin.
* Microsoft Word: Informa de la distància des del límit esquerre de la pàgina quan es polsa el tabulador. (#1353) 
* Microsoft Word: proporciona realimentació de veu i Braille per a la majoria de dreceres de teclat de format de text disponibles (negreta, itàliques, subratllat, alineació, superíndex, subíndex i mida de la lletra). (#1353)
* Microsoft Excel: Si la cel·la seleccionada conté comentaris, es poden verbalitzar polsant les tecles NVDA+alt+c. (#2920)
* Microsoft Excel: Proporciona una finestra específica del NVDA per editar els comentaris de la cel·la seleccionada, una vegada polsada l'ordre Maj+f2 de l'Excel per entrar en el mode d'edició dels comentaris. (#2920)
* Microsoft Excel: realimentació de veu i Braille per a més dreceres de selecció de moviment (#4211) incloent-hi:
* Moviment vertical de la pàgina (inici i fi):
* Moviment horitzontal de la pàgina (alt+inici) i (alt+fi);
* Ampliar la selecció (tecla Maj + fletxa esquerra o fletxa dreta); i
* Selecció de la regió actual (control+maj+8).
* Microsoft Excel: L'ordre que informa del format del text (NVDA+f), ara pot informar de l'alineació vertical i horitzontal de les cel·les. També en pot informar automàticament si la opció d'informe de l'alineació dels paràmetres del format del document es troba activada. (#4212)
* Microsoft Excel: L'ordre que informa del format del text (NVDA+f), ara pot informar de l'estil d'una cel·la. També en pot informar automàticament si l'opció Informa de  l'estil dels paràmetres del format del document es troba activada. (#4213)
* Microsoft Power Point: S'informa de la posició de les formes quan aquestes es mouen dins d'una diapositiva amb les fletxes de moviment (#4214), incloent-hi:
* La distància entre la forma i els límits de la diapositiva.
* Si la forma cobreix o es coberta per una altra forma, s'informa de la distància de superposició.
* Per a que NVDA doni aquesta informació sense moure la forma, polseu l'ordre d'informe de localització (NVDA+Supr).
* Quan la forma seleccionada es coberta per una altra forma, NVDA informa que s'ha enfosquit.
* L'ordre d'informe de localització (NVDA+Supr) és més específica d'acord al context, en determinades situacions. (#4219)
* En els camps d'edició estàndard i en el mode de navegació, s'informa de la posició del cursor com a un percentatge respecte al contingut i coordenades de la pantalla.
* En les presentacions de Power Point, s'informa de la posició de les formes en relació a la diapositiva i a la resta de formes.
* Polsant dues vegades aquesta ordre es produeix el comportament anterior resultat d'informar de la localització de tot el control.
* Nou idioma: Català.

### Canvis

* Traductor liblouis braille actualitzat a la versió 2.5.4. (#4103)

### Correccions d'errors

* Al Google Chrome i a la resta de navegadors basats en aquest navegador, alguns fragments del text (per exemple, el representat amb èmfasi) ja no es repeteixen quan s'informa del text d'una alerta o diàleg. (# 4066)
* Ja no falla l'activació (ni activa altres controls) del mode de navegació a les aplicacions del Mozilla, que fallaven en certs casos com, per exemple, en els botons superiors del Facebook. (#4106)
* S'ha deixat d'anunciar informació inútil quan es tabula a l'iTunes. (#4128) 
* Ja funcionen correctament les opcions per moure's a l'ítem següent en algunes llistes de l'itunes com, per exemple, la llista de Música. (#4129)
* Els elements HTML considerats com a encapçalaments pel fet de estar marcats amb la sintaxi de WAI-ARIA, ara s'inclouen en la llista d'elements del mode de navegació, i en la navegació ràpida dels documents de l'Internet Explorer. (#4140)
* Els enllaços que s'activen dins de la mateixa pàgina a les darreres versions de l'Internet Explorer, funcionen correctament i se n'informa de la posició de la destinació en el mode de navegació de documents. (#4134)
* Seguint enllaços mateixa pàgina en les últimes versions d'Internet Explorer ara es mou correctament i els informes de la posició de destinació en els documents de manera d'exploració. (#4134)
* Microsoft Outlook 2010 i posterior: S'ha millorat l'accés general als diàlegs de seguretat com, per exemple, els nous perfils i diàlegs de configuració del correu. (#4090, #4091, #4095)
* Microsoft Outlook: S'ha reduït  la quantitat d'informació poc útil durant la navegació per determinats diàlegs. (#4096, #3407)
* Microsoft Word: Tabular cap a una cel·la en blanc dins d'una taula ja no s'anuncia com si es sortís de la taula. (#4151)
* Microsoft Word: El primer caràcter després del final d'una taula (incloses les línies en blanc) ja no es consideratt erròniament dins de la taula. (#4152)
* Diàleg de verificació ortogràfica del Microsoft Word 2010: S'informa de l'actual paraula mal escrita, en comptes de fer-ho només de la primera paraula en negreta. (#3431)
* Al fer servir el mode de navegació a l'Internet Explorer i a d'altres controls MSHTML, la tabulació o la navegació a partir d'una sola lletra per moure's cap als camps dels formularis, informa, en molts casos, dues vegades de l'etiqueta del camp, quan no ho hauria de fer (especialment quan s'utilitzen els elements label de l'HTML). (#4170)
* Microsoft Word: L'informe de l'existència i ubicació dels comentaris és més precís. (#3528)
* La navegació d'alguns dels diàlegs de determinats paquets com el Word, l'Excel i l'Outlook s'ha millorat, i ja no informen de determinades barres d'eines que no són útils per a l'usuari. (#4198)
* Els panells de tasques com, per exemple, el gestor del porta-retalls o el de recuperació d'arxius, sembla que ja no reben el focus accidentalment, en obrir-se aplicacions com el Microsoft Word o l'Excel. Això provocava que l'usuari hagués d'alternar entre una aplicació i l'altre per poder utilitzar el document o full de càlcul. (#4199)
* NVDA ja no falla en executar-se en les darreres versions del sistema operatiu Windows en l'idioma serbi (llatí). (#4203)
* El bloqueig numèric dins del mode d'ajuda a l'entrada, ja funciona correctament, evitant els problemes de sincronització entre el teclat i el sistema operatiu. (# 4226)
* Al Google Chrome, el títol del document s'informa cada vegada que es canvia de pestanya. Al NVDA 2014.2, això no passa en alguns casos. (#4222)
* S'ha deixat d'anunciar l'URL en el Google Chrome, i la resta de navegadors basats en el Google Chrome, en el moment d'informar del document. (#4223)
L'ordre Verbalitza-ho tot ara funciona correctament, en comptes d'aturar-se després de les primeres línies, quan s'activa sense haver seleccionat cap sintetitzador (útil per a proves automatitzades). (# 4225)
* Diàleg de les signatures del Microsoft Outlook: El camp per editar la signatura ja és accessible, permetent un control complet del seguiment del cursor i la detecció del format. (# 3833)
* Microsoft Word: Quan es llegeix l'última línia de la cel·la d'una taula, ja no es torna a llegir la taula sencera. (#3421)
* Microsoft Word: Quan es llegeix la primera o última línia d'una taula de continguts, ja no es torna a llegir la taula sencera. (#3421)
* Al verbalitzar les paraules escrites i en altres casos, aquestes ja no es tallen de manera incorrecta en marques com ara els signes vocàlics o els virama dels idiomes indoàries. (#4254)
* Els camps editables de text numèrics al GoldWave ja es gestionen correctament. (#670)
* Microsoft Word: En moure't pels paràgrafs amb control + fletxa avall / control + fletxa amunt, ja no és necessari polsar dues vegades al passar per llistes numerades o de pics. (#3290)

### Canvis per desenvolupadors

* NVDA ha unificat la documentació relativa als complements. Vegeu la secció dels complements a la Guia per desenvolupadors per saber-ne més. (#2694)
* En proporcionar gesture bindings en el objecte ScriptableObject via __gestures, ara és possible proporcionar la tecla Cap com a l'script. Això s'uneix al gest en qualsevol de les classes base. (#4240)
* Ja es possible canviar la tecla de drecera utilitzada per iniciar NVDA en equips en els que la drecera per defecte dóna problemes. (#2209)
* Realitzat amb el gettext.
* Tingueu present que el text de l'opció per crear una drecera a l'escriptori dins del diàleg d'instal·lació del NVDA, així com la tecla de drecera en la Guia d'usuari, també s'han d'actualitzar.

## 2014.2

### Noves característiques

* En alguns camps d'edició personalitzats, on es fa servir la informació de pantalla, és possible anunciar la selecció de text. (#770)- En aplicacions Java accessibles és possible anunciar la posició de la informació mitjanant botons de ràdio i d'altres controls que exposen informació de grup.  (#3754)
* En aplicacions Java accessibles, les dreceres de teclat s'anuncien per aquells controls que en tenen.(#3881)
* En mode de navegació, es reporten les etiquetes dels punts de referencia. Aquests s'inclouen també en el diàleg Llista d'Elements. (#1195)
* En mode de navegació les regions etiquetades apareixen tractades ara com a punts de referencia. (#3741)- En documents i aplicacions d'Internet Explorer, se suporten ara les Live Regions (part de la normativa ARIA del W3C) permetent  que els autors dels web marquin determinats continguts per a ser automàticament parlats si són modificats. (#1846)

### Canvis

Quan se surt d'un diàleg o d'una aplicació dins d'un document en mode de navegació, ja no s'anuncia el nom i tipus del document en mode de navegació  (#4069)

### Corecció d'errors

* El menú estàndard de sistema de Windows ja no es silencia de forma accidental en les aplicacions Java. (#3882)
* Quan es copia text des de la revisió de pantalla, ja no s'ignoren els salts de línia. (#3900)
* Els objectes situats en espais en blanc insubstancials ja no apareixen reportats en algunes aplicacions quan el focus canvia o quan es fa servir la navegació d'objectes amb la revisió simple activada.  (#3839)
* Les finestres de missatge i d'altres quadres de diàleg produïts per NVDA originen de nou i causen veu de forma prèvia a ser cancel·lats abans de anunciar el diàleg
* En mode de navegació, les etiquetes de controls com ara enllaços o botons, apareixen representades correctament allà  on l'etiqueta hagi estat anul·lada per l'autor amb fins d'accessibilitat  (concretament, usant aria-label or aria-labelledby). (#1354)
* En mode de navegació dins d'Internet Explorer, el text contingut dins d'un element marcat com de presentació (ARIA rol=presentació"), ja no s'ignora de forma inapropiada. (#4031)- Ara 
és possible escriure text en Vietnamita fent servir el programari Unikey.  Per a fer això, organitzeu les tecles des de les caselles d'altres aplicacions en el quadre de diàleg Paràmetres del teclat.  (#4043)- En mode de navegació, els menús de radio i de verificació estan reportats com a controls enlloc de només text clicable. (#4092)
* NVDA ja no canvia de forma incorrecta del mode de focus al mode de navegació quan està activat un menú de ràdio o de verificació. 
* Al Microsoft PowerPoint, si hi ha activada la parla de les paraules escrites, els caràcters que s'hagin esborrat amb la tecla de retrocés, ja no es llegeixen com a part de la paraula escrita. (#3231)- Al diàleg d'opcions del Microsoft Office 2010 les etiquetes de les quadres combinats es llegeixen correctament. (#4056)
* En el mode de navegació en aplicacions Mozilla, l'accés de comandaments ràpids de navegació per a moure's d'un botó a l'anterior o a un camp de formulari inclou ara els botons de commutació que caldria esperar. (#4098)- El contingut de les alertes a les aplicacions ja no es reporta dues vegades. (#3481)
* En el mode de navegació, els contenidors i punts de referència ja no es repeteixen de forma inapropiada mentre es navega entre ells al mateix temps que s'està canviant el contingut de la pàgina (per exemple, navegant per llocs com Facebook o Twitter) (#2199)- NVDA es recupera en més casos quan es canvia des d'aplicacions que han deixat de respondre. (#3825)- El símbol d'intercalació  (punt d'inserció) s'actualitza correctament quan es fa un comandament Verbalitza-ho tot mentre es porta un text a edició un text directament de la pantalla.  (#4125)

## 2014.1

### Noves característiques

* Afegit suport per al Microsoft PowerPoint 2013. Cal notar que la vista protegida no està suportada. (#3578)
* En el Microsoft Word i Excel, NVDA pot ara llegir el símbol seleccionat quan es fa servir el diàleg Inserció  Símbol. (#3538)
* Ara és possible escollir si el contingut en els documents ha de ser identificat com a clicable via una nova opció en el quadre de diàleg Formatació de Documents. Aquesta opció és, per defecte, d'acord amb el comportament previ.  (#3556)
* Afegit suport per línies Braille connectades via Bluetooth a un ordinador que està executant el programari Widcomm Bluetooth. (#2418)
* Ara s'informa dels enllaços quan s'està editant text en Power Point.  (#3416)
* En aplicacions ARIA o en diàlegs del web, ara és possible forçar NVDA a canviar a mode de navegació amb NVDA+espai. Això permet navegar per l'estil del document de l'aplicació o del diàleg.  (#1594)
* Quan es navega per taules en aplicacions accessibles Java, ara s'informa de les coordenades de fila i columna, tot incloent capçaleres de fila i columna, si existeixen. (#3756)

### Canvis

* Per línies braille Papenmeier, s'ha eliminat el comandament que canviava a revisió plana/focus. Els usuaris poden assignar les seves pròpies tecles usant el quadre de diàleg Gestos d'entrada.  (#3652)
* NVDA ara es basa en la versió 11 del Microsoft VC runtime, la qual cosa suposa que ja no funcionarà en sistemes operatius anteriors a Windows XP Service Pack 2 o Windows Server 2003 Service Pack 1.
* Nivell de puntuació. En alguns casos ara es pronunciaran l'estrella(*) i els caràcter mes (+)  
* S'ha actualitzat eSpeak a la versió 1.48.04, que inclou diverses correccions d'idioma i corregeix diversos bloquejos. . (#3842, #3739, #3860)

### Correccions d'errors

* Quan es moguin o seleccionin cel·les en el Microsoft Excel, NVDA ja no anunciarà de forma inapropiada la cel·la antiga abans que la cel·la nova, quan el Microsoft Excel desplaci amb lentitud la selecció. (#3558)
* NVDA gestiona adequadament l'obertura d'una cel·la desplegable via el menu contextual. (#3586)
* El contingut d'una nova pàgina en iTunes Store 11 ara es mostra adequadament en mode de navegació quan se segueix un enllaç en la botiga o bé quan s'inicia aquesta. (#3625)
* Els botons per escoltar les cançons en el iTunes Store 11 ara mostren el seu etiquetat en mode de navegació.  (#3638)
* En mode de navegació en Google Chrome, les etiquetes de les caselles i botons de radio es representen ara correctament. (#1562)
* A Instantbird, NVDA ja no reporta informació inútil cada vegada que es mou un contacte en la llista de contactes. (#2667)
* En mode de navegació, en l'Adobe Reader, es representa ara el text correcte per als botons, etc, allà on l'etiqueta havia estat ignorada usant indicadors de funció o altres mitjans.(#3640)
* En el mode de navegació, en l'Adobe Reader, ja no es llegeixen gràfics estranys que contenen el text "mc ref".(#3645)
* NVDA ja no indica que totes les cel·les estan subratllades en la seva informació de format. (#3669)
* Ja no es mostren caràcters sense sentit en documents en mode de navegació com els que s'havien localitzat en el rang d'ús privat d'Unicode. En alguns casos això impedia que es mostressin etiquetes més significatives. (#2963)
* La composició d'entrada per a entrar caràcters de l'Àsia de l'Est ja no falla a PuTTY.(#3432)
* La navegació en un document després de cancel·lar un Verbalitza-ho tot ja no dona resultats incorrectes en NVDA tot anunciant que s'ha deixat un camp (com una taula) inferior en el document que el Verbalitza-ho tot mai havia parlat. (#3688)
* Quan es fan els comandaments de navegació ràpida en el mode de navegació mentre hi ha activat el Verbalitza-ho tot amb la lectura per sobre, NVDA ara anuncia de forma més acurada el nou camp.  Per exemple, ara diu que un encapçalament és un encapçalament, no només text.(#3689)
* El salt cap al final o l'inici en els comandaments de navegació ràpida d'un contenidor ara representen la lectura per sobre durant la configuració de Verbalitza-ho tot. Es a dir, ara ja no cancel·laran més el Verbalitza-ho tot actiu.  (#3675)
* Els noms de gestos tàctils llistats en el diàleg d'Entrada de textos ara són amigables i localitzats. (#3624)
* NVDA ja no causa que alguns programes es bloquegin quan es mou el ratolí sobre els seus controls d'edició (TRichEdit). Alguns programes són Jarte 5.1 i BRfácil. (#3693, #3603, #3581)
* A l'Internet Explorer i altres controls MSHTML, alguns contenidors, com les taules que apareixen marcades com a presentació per ARIA ja no s'informen a l'usuari. (#3713)
* Al Microsoft Word, NVDA  ja no repeteix múltiples vegades i de forma inapropiada en una línia Braille la informació sobre la fila i la columna d'una taula per a cada cel·la.  (#3702)
* En idiomes que fan servir un espai com a dígit de grup / separador de milers, com en el cas del francès i l'alemany, els números de grups separats de text ja no es pronuncien com un únic nombre. Això era particularment problemàtic per cel·les que contenien nombres.(#3698)
* El Braille ja no falla de vegades en actualitzar quan el cursor d'intercalació del sistema es desplaça en el Microsoft Word 2013. (#3784)
* Quan s'està posicionat en el primer caràcter d'un encapçalament en el Microsoft Word, el text que comunica que és un encapçalament (eicloent el nivell) ja no desapareix en una línia Braille. (#3701)
* Quan un perfil d'aplicació s'activa per una aplicació i se surt d'aquesta aplicació, NVDA ja no falla en desactivar el perfil.(#3732)
* Quan s'entra una entrada asiàtica dins d'un control en el mateix NVDA (per exemple el diàleg Cercar en el mode de navegació), NVDA ja no informa incorrectament en lloc del candidat. (#3726)
* Ara s'informa de les pestanyes en el quadre de diàleg d'opcions en el Outlook 2013. (#3826)
* Millorat el suport per les regions actives ARIA a Firefox i d'altres aplicacions Mozilla Gecko:
* Support per actualitzacions aria-atomic i pel filtrat d'actualitzacions aria-busy.(#2640)
* Si no hi ha cap altre text útil s'inclou el text alternatiu (com l'atribut alt o aria-label). (#3329)
* Les actualitzacions de regions actives ja no es silencien si s'esdevenen a la mateixa vegada que es mou el focus. (#3777)
* Alguns elements de presentació en Firefox i d'altres aplicacions Mozilla Gecko ja no es mostren de forma inapropiada en mode de navegació (específicament quan l'element apareix marcat com a aria-presentation però és també enfocable). (#3781)
* S'ha millorat el rendiment quan es navega per un document en el icrosoft Word amb el corrector ortogràfic activat.   (#3785)
* Corregits diversos errors per aplicacions Java accessibles  
* El control inicialment enfocat en un marc o en un diàleg ja no falla quan el marc o el diàleg passen a primer pla. (#3753)
* Ja no s'anuncia la posició de la informació per als botons de ràdio quan és inútil.(per exemple 1 de 1). (#3754)
* Millor informació dels controls JComboBox (ja no s'informa d'html i s'informa millor dels estats expandit i contret).  (#3755)
* Quan s'informa del text dels diàlegs, algun text que havia estat omès prèviament, ara s'inclou.(#3757)
* Els canvis al nom, valors o descripció del control enfocat s'informen ara molt més acuradament. (#3770)
* Corregit un bloqueig que s'havia vist en NVDA per Windows 8 quan es focalitzava en certs controls RichEdit que contenien grans quantitats de text (per exemple, el visor de registres NVDA, windbg). (#3867)
* En sistemes amb una configuració de pantalla d'alta DPI (cosa que per defecte passa en moltes pantalles modernes) NVDA ja no envia el ratolí a la localització equivocada en algunes aplicacions.(#3758, #3703)
* Corregit un problema ocasional quan es navegava pel web, segons el qual NVDA  aturava el seu correcte funcionament fins que es reinicialitzava, fins i tot si no es bloquejava ni congelava. (#3804)
* Ara es pot fer servir una línia Braille Papenmeier fins i tot si mai s'ha connectat abans una línia Papermeier via USB.   (#3712)
* NVDA ja no es congela quan se seleccionen els vells models de la línia Braille Papenmeier BRAILLEX sense que hi hagi un dispositiu connectat.    
== Canvis per desenvolupadors ==
* AppModules ara conté les propietats productName i productVersion. Aquesta informació s'inclou dins de la guia del desenvolupador. (NVDA+f1). (#1625)
* A la consola Phyton, ara pots prémer la tecla tabulador per a completar l'identificador actiu.. (#433)
* Si hi ha múltiples possibilitats, ara pots prémer tab una segona vegada per triar d'una llista.   

## 2013.3

### Noves característiques

* Ja s'informa dels camps dels formularis als documents del Microsoft Word. (#2295)
* NVDA ja pot anunciar la informació de revisió al Microsoft Word quan el seguiment de canvis es troba activat. Recordeu que l'informe de revisió de l'editor del diàleg de paràmetres del document del NVDA (desactivat per defecte), ha d'estar activat per a que aquesta informació s'anunciï. (# 1.670)
* Ja s'anuncia l'obertura i navegació per les llistes desplegables de les versions del Microsoft Excel de la 2003 a la 2010. (#3382)
* La nova opció "Permet la lectura superficial en el perfil verbalitza-ho tot", del diàleg de configuració del teclat, permet la navegació pel document amb el mode de navegació ràpid o a través de les odres de moviment per línies o paràgrafs, sense deixar de verbalitzar-ho tot. Aquesta opció es troba desactivada per defecte. (#2766)
-Ja es disposa d'un diàleg de gestos d'entrada que permet una personalització més simple d'aquests gestos (com per exemple, les tecles del teclat) per a les ordres del NVDA. (# 1532)
* Ja es pot disposar de diferents configuracions per a diferents situacions a partir dels perfils de configuració. Aquests perfils poden ser activats de forma manual o automàtica (p. e., per una aplicació en concret) . (#87, #667, #1913)
* Les cel·les del Microsoft Excel que contenen enllaços, ja s'anuncien com enllaços. (#3042)
* L'existència de comentaris a una cel·la del Microsoft Excel, ja s'anuncia a l'usuari. (#2921)

== Correccions d'errors ==
* El Zend Studio, funciona ara com l'Eclipse. (#3420)
* Ara s'informa automàticament del canvi d'estat de certes caselles de verificació del quadre de diàleg de regles del Microsoft Outlook 2010. (#3063)
* NVDA informa de l'estat fixat de determinats controls com ara les pestanyes del Mozilla Firefox. (#3372)
* Ara és possible enllaçar scripts a gestos de teclat que contenen Alt i/o tecles de Windows com a modificadors. Anteriorment, si això succeïa, s'activava en alguns casos el menú Inici o la barra de menú. (# 3472)
* Seleccionar text en el mode de navegació dels document (p. e. utilitzant control+maj+fi) ja no provoca que la distribució del teclat canvií en els sistemes que tenen instal·lades més d'una. (#3472) 
* L'Internet Explorer ja no es bloqueja al tancar NVDA. (#3397)
* El moviment físic i d'altres esdeveniments en determinats ordinadors moderns, ja no són tractats com pulsacions incorrectes de tecles. Anteriorment, o no es verbalitzaven o disparaven algunes ordres del NVDA. (# 3468)
* NVDA ja es comporta adequadament al Poedit 1.5.7. Els usuaris que utilitzen versions anteriors hauran d'actualitzar a la versió 1.5.7 o posterior. (#3485)
* NVDA ja pot llegir documents protegits al Microsoft Word 2010, sense que aquest últim es bloquegi. (#1686)
* Si es realitza una entrada desconeguda a la línia d'ordres en el moment en que el paquet de la distribució del NVDA s'executa, ja no es provoca un bucle infinit amb el diàleg de missatge d'error. (#3463)
* NVDA ja no falla a l'informar del text alternatiu dels gràfics i objectes del Microsoft Word, quan aquest text alternatiu conté cometes o altres caràcters no estàndards. (#3579)
* El nombre d'ítems de certes llistes horitzontals en el mode de navegació ja és correcte. Anteriorment, s'estava anunciant el doble del nombre real. (#2151)
* Al polsar control+a a un full de càlcul del Microsoft Excel, ja s'informa de la nova selecció. (#3043)
* NVDA ja llegeix correctament documents XHTML al Microsoft Internet Explorer i a d'altres controls MSHTML. (#3542)
* Quadre de diàleg de configuració del teclat: Si no s'ha triat cap tecla com a tecla modificadora de NVDA, i l'usuari prem l'opció de cancel·lar, es presentarà un error a l'usuari fins que no trií una de les opcions. (#2871)
* Diàleg de configuració de teclat: si cap tecla ha estat escollit per ser utilitzat com la tecla NVDA, un error es presenta a l'usuari quan es desestima el diàleg. Almenys una de les claus ha de ser elegida per a l'ús adequat de NVDA. (# 2871)
* NVDA ja anuncia de manera diferent les cel·les combinades i els grups de múltiples cel·les seleccionades al Microsoft Excel. (#3567)
* El mode del cursor de navegació ja no es posiciona incorrectament al sortir d'un quadre de diàleg o aplicació dins del document. (#3145)
* S'ha solucionat un problema pel qual la visualització braille de la sèrie HumanWare Brailliant BI/B no es presentava com a opció en el quadre de diàleg de la configuració Braille, tot i estar connectat via USB.
* NVDA ja no falla al commutar cap a la revisió de pantalla quan l'objecte del navegador no té cap ubicació a la pantalla. En aquest cas, el cursor de revisió es posiciona a la part superior de la pantalla. (#3454)
* S'ha solucionat un problema causat pel controlador del terminal Braille Freedom Scientific, que provocava que fallés al connectar-se en certs casos, al port USB. (#3509, #3662)

== Canvis per desenvolupadors ==
* Ja podeu especificar la categoria que voleu mostrar a l'usuari per als scripts utilitzant l'atribut scriptCategory de les classes del ScriptableObject i l'atribut de la categoria dels mètodes dels scripts. Vegeu la documentació del baseObject.ScriptableObject per saber-ne més. (#1532)
* config.save ha quedat obsolet i pot ésser eliminat en futures versions. Utilitzeu el config.conf.save com alternativa. (#667)
* config.validateConfig ha quedat obsolet i pot ésser eliminat en futures versions. Els complements que ho necessiten, han de proporcionar la seva pròpia implementació com alternativa. (#667, #3632)

## 2013.2

### Noves característiques

* Suport per Chromium Embedded Framework, un control del navegador web utilitzat en diverses aplicacions. (#3108)
* Nova variant de veu pel sintetitzador eSpeak: Iven3.
* Ja s'informa automàticament dels nous missatges de xat de l'l'Skype, quan la conversa té el focus. (#2298)
* Suport per al client de Twitter Tween, incloent la verbalització dels noms de les pestanyes i la reducció de la velocitat de la verbalització en llegir tuits.
* Ja es pot desactivar la visualització del missatges del NVDA en els terminals Braille, configurant el missatge en temps d'espera com a 0 dins del diàleg de configuració del Braille. (#2482)
* Ara, el gestor de complements disposa d'un botó que permet obrir el lloc web de complements del NVDA. En aquest lloc web, podeu veure i descarregar complements disponibles per al NVDA. (#3209)
* Dins del diàleg de benvinguda del NVDA, podeu configurar que NVDA s'iniciï automàticament després d'iniciar sessió al Windows. (#2234)
* El mode de suspensió es troba activat automàticament quan s'utilitza Dolphin Cicero. (#2055)
* Ja s'ofereix suport per a la versió  del Miranda IM/Miranda NG per a sistemes operatius Windows de 64 bits. (#3296)
* S'informa automàticament dels suggeriments de cerca a la pàgina d'inici del Windows 8.1. (#3322)
* Suport per a la navegació i edició de fulls de càlcul del Microsoft Excel 2013. (#3360)
* Els terminals Braille Freedom Scientific Focus 14 Blue i el Focus 80 Blue, així com el Focus 40 Blue abans no suportaven certes configuracions que ara si suporten via Bluetooth. (#3307)
* S'informa automàticament dels suggeriments d'emplenament automàtic al Outlook 2010. (#2816)
* Noves taules de traducció Braille: Anglès (U.K.) per codi d'ordinador, Coreà grau 2, Braille rus per codi d'ordinador.
* Nou idioma: Persa. (#1427)

== Canvis ==
Ara, els gestos d'un sol toc cap a l'esquerra o la dreta a les pantalles tàctils dins del mode de revisió d'objectes, et permeten moure't per l'objecte anterior i següent respectivament, i no només pels objectes dins del contenidor actiu. Per realitzar l'acció  original de moviment per l'objecte anterior i següent del contenidor actiu, fes servir dos tocs cap a l'esquerra o la dreta.
* s'ha substituït la revisió plana pels modes de revisió d'objectes, documents i pantalla. (#2996)
* Object review reviews text just within the navigator object, document review reviews all text in a browse mode document (if any) and screen review reviews text on the screen for the current application.
* Les ordres que abans permetien moure a l'usuari a, o, des del mode de revisió plana, ara permeten commutar entre els nous modes de revisió.
* L'objecte de navegació segueix automàticament el cursor de revisió, de manera que continua sent l'objecte més profund del cursor de revisió quan s'utilitzen els modes de revisió en un document o pantalla.
* Després de canviar al mode de revisió de pantalla, NVDA roman en aquest mode fins que es torna de manera explícita al document o al mode de revisió de l'objecte.
* NVDA commuta automàticament entre el mode de revisió de documents i d'objectes, segons si s'està fent servir o no el mode de navegació per moure's en el document.
* S'ha actualitzat el traductor liblouis braille a la versió 2.5.3. (#3371)

### Correccions d'errors

* L'acció d'activació d'un objecte ara s'anuncia abans de l'activació, en comptes de fer-ho després (per exemple, l'acció d'expandir-se abans que la de col·lapsar-se). (#2982)
* S'ha millorat la lectura i el seguiment del cursor en diferents camps d'entrada de dades (com el xat o els camps de cerca) per a les darreres versions de l'l'Skype. (#1601, #3036)
* Ja es llegeix la llista de converses recents i el nombre d'esdeveniments a l'l'Skype, sempre que siguin rellevants. (#1446)
* Millores en el seguiment del cursor i en l'ordre de lectura del text escrit de dreta a esquerra; per exemple, en l'edició de textos en àrab al Microsoft Excel. (#1601)
* Dins del Microsoft Explorer, saltar directament a botons i camps de formulari, permet localitzar enllaços que s'han codificat com a botons per a millorar l'accessibilitat. (#2750)
* La navegació ràpida als botons i camps de formulari ara localitza enllaços marcats com botons per a fins d'accessibilitat a Internet Explorer. (# 2750)
* En el mode de navegació, el contingut dins de l'arbre jeràrquic ja no es renderitza com una representació plana. Podeu prémer la tecla d'inserció dins de l'arbre jeràrquic per interactuar amb ell dins del mode del focus del sistema. (#3023)
* Prémer alt + fletxa avall, o alt + fletxa amunt per expandir un quadre combinat en el mode del focus del sistema, ja no fa saltar al NVDA al mode de navegació. (#2340)
Al Microsoft Explorer 10, les cel·les de les taules ja no activen automàticament el mode de focus del sistema, sempre i quan l'autor del lloc web no les hagi codificat expressament per rebre el focus. (#3248)
* NVDA ja no falla en iniciar-se si l'hora del sistema és anterior a l'hora de l'última revisió d'actualitzacions disponibles. (# 3260)
 * Si una barra de progrés es mostra en un terminal Braille, aquest s'actualitza quan la barra de progrés canvia. (#3258)
* Dins del mode de navegació a les aplicacions del Mozilla, les llegendes de les taules ja no es llegeixen dues vegades. El resum es llegeix quan també hi ha una llegenda. (#3196)
* Ara, NVDA anuncia correctament l'idioma triat en canviar els idiomes d'entrada al Windows 8., en comptes de triar l'idioma anterior.
* NVDA anuncia els canvis del mode de conversió IME al Windows 8.
* NVDA ja no anuncia la brossa en l'escriptori quan s'utilitzen els mètodes d'entrada del Google japonès o l'Atok IME. (#3234)
* Al Windows 7 i posteriors, NVDA ja no anuncia incorrectament el reconeixement de veu o els gestos tàctils com un canvi de l'idioma del teclat.
* NVDA ja no anuncia un caràcter especial (0x7f) en prémer control+Retrocés en determinats editors, quan la verbalització dels caràcters escrits es troba activada. (#3315)
L'eSpeak ja no canvia incorrectament el to, volum, etc., quan NVDA llegeix text que conté certs caràcters de control o en documents XML. (# 3334) (regressió de # 437)
* A les aplicacions Java, ara s'anuncien automàticament els canvis a l'etiqueta o el valor del control que té el focus. Així mateix, queden reflectits quan es consulta el control en qüestió. (#3119)
* En els control Scintilla, ja s'informa correctament de les línies quan l'ajust de línia es troba activat. (#885)
* A les aplicacions del Mozilla, s'informa correctament del nom dels ítems de només lectura; per exemple, al navegar pels tuits en mode de focus del sistema a twitter.com. (#3327)
* Els diàlegs de confirmació del Microsoft Office 2013 es llegeixen automàticament, tan bon punt apareixen.
* Millores en el rendiment al navegar en determinades taules en Microsoft Word. (# 3326)
* Les ordres de navegació per les taules del NVDA (control+alt+fletxes) funcionen millor en certes taules del Microsoft Word amb cel·les combinades.
* Ja no dóna error activar el gestor de complements si aquest ja es trobava obert. Anteriorment, l'error impedia tancar aquest gestor en aquesta situació (#3351)
NVDA ja no es queda bloquejat en certs diàlegs de l'Office 2010 on s'utilitza l'IME japonès o xinès
* Ja no es comprimeixen en un sol espai, els múltiples espais detectats pels terminals Braille. (#1366)
* Zend Eclipse PHP Developer Tools ara funciona com l'Eclipse. (#3353)
* A l'Internet Explorer, ja no es necessari prémer el tabulador per interactuar amb els objectes embeguts (per exemple, el contingut Flash) després d'accedir-hi. (#3364)
* En editar text al Microsoft PowerPoint, l'última línia ja no es informada com una línia anterior, si la darrera línia és en blanc. (#3403)
* Els objectes del Microsoft Power Point ja no es verbalitzen dues vegades quan es seleccionen o es trien per editar-los. (#3394)
* NVDA ja no provoca que l'Adobe Reader es bloquegi quan el contingut del document es troba mal format perquè conté files fora de les taules. (#3399)
* NVDA ja detecta correctament la diapositiva següent en tenir el focus a l'esborrar una diapositiva dins la vista de miniatures del Microsoft Power Point. (#3415)

== Canvis per desenvolupadors ==
* S'ha afegit el windowUtils.findDescendantWindow per a la cerca de finestres
* S'ha afegit el windowUtils.findDescendantWindow per a la cerca de finestres descendents (HWND) que coincideixen amb la visibilitat especificada, l'ID del control i/o el nom de la classe.
* La consola remota Python ja no s'atura després de 10 segons d'inactivitat. (#3126)
* Ha quedat obsoleta la inclusió del mòdul bisect en el muntatge binari. Pot ésser eliminat a futures versions. (#3368)
* Els complements que depenen del mòdul bisect (incloent-hi el mòdul urllib2) han de ser actualitzats per incloure aquest mòdul.

= 2013.1.1 =
Aquesta versió soluciona el problema pel qual NVDA es bloquejava en iniciar-se si se seleccionava l'idioma irlandès. També s'inclouen noves traduccions i altres correccions d'errors.

== Correccions d'errors ==
* Ja es creen caràcters correctes a la interfície d'usuari del NVDA quan el mètode d'entrada utilitza caràcters coreans i japonesos com a mètode per defecte. (#2909)
* A l'Internet Explorer i a d'altres controls MSHTML, els camps dels formularis que contenen un error es gestionen correctament. (#3256)
* NVDA ja no es bloqueja al iniciar-se quan està configurat per fer servir l'idioma irlandès.

= 2013.1 =
Les millores més importants d'aquesta versió inclouen una nova disposició de teclat per a ordinadors portàtils més intuïtiva i consistent; suport bàsic per Microsoft Power Point; suport per a descripcions llargues als navegadors; i suport per a l'entrada des de terminals Braille que tenen un teclat Braille.

== Important ==

=== Nova disposició del teclat dels portàtils ===
S'ha redissenyat completament la disposició del teclat dels ordinadors portàtils per fer-la més intuïtiva i consistent.
La nova disposició del teclat utilitza les fletxes de direcció en combinació amb la tecla NVDA, i d'altres tecles modificadores per a les ordres de revisió.
S'han produït diferents canvis en les ordres d'ús comú següents:

| Nom |Tecla en el teclat portàtil|
|---|---|
|Verbalitza-ho tot |NVDA+a|
|Llegeix la línia actual |NVDA+l|
|Llegeix la selecció de text actual| NVDA+Maj+s|
|Llegeix la barra d'estat |NVDA+Maj+fi|

Entre d'altres canvis, tots els objectes de navegació, de revisió del text, de clics del ratolí i d'opcions del sintetitzador han canviat.
Vegeu el document [Commands Quick Reference](keyCommands.html) per saber-ne més.

### Noves característiques

* Suport bàsic per a l'edició i lectura de presentacions del Microsoft PowerPoint. (#501)
* Suport bàsic per a la lectura i escriptura de missatges al Lotus Notes 8.5. (#543)
* Suport per al canvi automàtic d'idioma al llegir documents al Microsoft Word. (#2047)
* En el mode de navegació per MSHTML (per exemple, Internet Explorer) i Gecko (per exemple, Firefox), s'anuncia l'existència de descripcions llargues. També es possible obrir la descripció llarga en una nova finestra amb la combinació NVDA+d. (#809)
* Ja s'anuncien les notificacions a l'Internet Explorer 9 i posteriors (per exemple, el contingut bloquejat o la descàrrega de fitxers). (#2343)
* Ja es suporta l'anunci automàtic dels encapçalaments de les files i columnes del mode de navegació de documents a l'Internet Explorer i a d'altres controls MSHTML. (#778)
* Nous idiomes: aragonès i irlandès
* Noves taules de traducció Braille: danès grau 2, coreà grau 1. (#2737)
* Suport pels terminals Braille connectats per Bluetooth a ordinadors amb Bluetooth Stack de Toshiba per Windows. (#2419)
* Suport per a la selecció del port a l'utilitzar en els terminals Freedom Scientific (automàtic, USB o Bluetooth).
* Suport per a la família d'anotadors BrailleNote de HumanWare quan actuen com a terminal Braille per a un lector de pantalla. (#2012)
* Suport per models antics dels terminals Braille Papenmeier BRAILLEX. (#2679)
* Suport per a l'entrada de dades des de terminals Braille que disposen d'un teclat Braille. (#808)
* Nous paràmetres del teclat que permeten commutar entre la verbalització o no verbalització dels caràcters escrits i/o la tecla inserció. (#698)
* Suport per una gran quantitat de navegadors en Google Chrome: Rockmelt, BlackHawk, Comodo Dragon i SRWare Iron. (#2236, #2813, #2814, #2815)

== Canvis ==
* Traductor liblouis Braille actualitzat a la versió 2.5.2. (#2737)
* S'ha redissenyat completament la disposició del teclat dels ordinadors portàtils per fer-la més intuïtiva i consistent.
* S'ha actualitzat el sintetitzador de veu eSpeak a la versió 1.47.11. (#2680, #3124, #3132, #3141, #3143, #3172)

== Correccions d'errors ==
* Les tecles de drecera per saltar a l'anterior o següent separador en el mode de navegació, ara funcionen a l'Internet Explorer i d'altres controls MSHTML. (#2781)
* Si es torna a l'eSpeak o no hi ha cap sintetitzador configurat per suplir al sintetitzador en ús quan aquest falla, en el moment d'iniciar-se NVDA, l'opció configurada ja no canvia automàticament al sintetitzador de reserva. Això vol dir que la propera vegada que NVDA s'iniciï, s'intentarà activar el sintetitzador original . (#2589)
* Si es desactiva el Braille a l'NVDA degut a una fallada del terminal Braille en iniciar-se NVDA, el terminal configurat ja no canvia automàticament a Braille desactivat. Això vol dir, que el terminal original pot ésser triat de nou  la propera vegada que NVDA s'inicia. rt(#2264)
* Al mode de navegació de les aplicacions de Mozilla les actualitzacions de les taules ja es renderitzen correctament. Per exemple, a les cel·les actualitzades s'informa correctament de les coordenades de la fila i la columna. (#2784)
* En el mode de navegació dins dels navegadors web, determinats gràfics clicables sense etiquetar que abans no es renderitzaben, ara si ho fan correctament. (#2838)
* Ja es suporten les versions actuals i les més antigues del SecureCRT. (#2800)
* Ja s'informa correctament de les cadenes de caràcters per als mètodes d'entrada com el Easy Dots IME sota Windows XP.
* La llista candidata en el mètode d'entrada del Microsoft Pinyin de xinès simplificat del Windows 7, ja es verbalitza correctament en canviar de pàgina amb les fletxes d'esquerra i dreta, i quan s'obre des de la pàgina d'inici.
* Quan es desa la informació sobre la pronunciació personalitzada dels símbols, el camp avançat "preserva", ja no s'elimina. (#2852)
* Quan es desactiva la comprovació automàtica d'actualitzacions, ja no cal reiniciar NVDA per a que aquest canvi tingui efecte.
NVDA ja no falla en iniciar-se si un complement no pot ésser eliminat del directori perquè encara s'està utilitzant per una altra aplicació. (#2860)
* Ja es poden veure les etiquetes de les pestanyes del diàleg de preferències del DropBox amb el mode de revisió plana.
* Si l'idioma d'entrada es canvia, NVDA ja detecta correctament les tecles per a les ordres, i per a les entrades del mode d'ajuda.
* Per als idiomes com l'alemany on el símbol + (més) és una tecla individual en el teclat, ara es possible utilitzar també la paraula "més". (#2898)
* A l'Internet Explorer i a d'altres controls MSHTML, les cites en línia ja s'informen on toca. (#2888)
* Els terminals Braille HumanWare Brailliant BI/B series, ja poden ser seleccionatss quan el terminal es connecta a través de Bluetooth, però no s'ha connectat mai a través de l'USB.
* Els filtres en els elements del mode de navegació ara són sensibles a les majúscules i minúscules. (#2951)
* En els navegadors Mozilla, es pot tornar a fer servir el mode de navegació quan el contingut Flash rep el focus. (#2546)
* Quan s'utilitza una taula Braille contreta i es passa a Braille d'ordinador, el cursor del Braille ara es posiciona correctament quan es troba després d'una paraula amb caràcters que es representen amb múltiples cel·les (per exemple, lletres majúscules, números, etc.). (#2947)
* La selecció de text ja es mostra correctament als terminals Braille en aplicacions com Microsoft Word 2003 i els controls d'edició de l'Internet Explorer.
* Torna a ser possible seleccionar text de dreta a esquerra al Microsoft Word mentre el Braille es troba activat.
* En revisar, fer retorn o eliminar caràcters als controls d'edició del Scintilla, NVDA anuncia correctament els caràcters multibyte. (#2855)
* La instal·lació del NVDA ja no fallarà quan el camí al perfil d'usuari conté determinats caràcters multibyte. (#2729)
* L'informe de grups per als controls en vista de llista (SysListview32) de les aplicacions de 64 bits ja no provoquen errors.
* En el mode de navegació a les aplicacions Mozilla, el contingut textual ja no es tracta incorrectament com contingut editable en determinats casos. (#2959)
-Al IBM Lotus Symphony i al OpenOffice, moure el cursor ara també mou el cursor de revisió quan sigui apropiat.
* El contingut de l'Adobe Flash ja és accessible a l'Internet Explorer del Windows 8. (#2454)
* Corregit el suport pel Bluetooth del Papenmeier Braillex Trio. (#2995)
* Corregida la impossibilitat d'utilitzar determinades versions de les veus de l'API del Microsoft Speech 5, com Koba. (#2629)
* A les aplicacions que utilitzen Java Access Bridge, el terminal Braille ja s'actualitza correctament quan el cursor es mou per camps de text editables. (#3107)
* Suport per al rol "form" (formulari) a les regions en el mode de navegació dins de documents que suporten regions. (#2997)
* El controlador del sintetitzador eSpeak ara gestiona la lectura dels caràcters d'una manera més acurada (per exemple, a l'anunciar el nom o valor de les lletres de noms estrangers, en comptes d'anunciar el seu so genèric). (#3106)
* NVDA ja no falla en copiar els paràmetres de configuració de l'usuari per utilitzar-los a la pantalla d'accés i en d'altres pantalles segures, quan el camí al perfil de l'usuari conté caràcters no ASCII. (#3092)
* NVDA ja no es bloqueja a l'utilitzar caràcters asiàtics a l'entrada de determinades aplicacions .NET. (#3005)
* Ara és possible utilitzar el mode de navegació de manera estandarditzada per les pàgines a l'Internet Explorer 10; per exemple, la pàgina d'inici de sessió del gmail.com. (#3151)
Ara és possible utilitzar el mode de navegació per les pàgines a Internet Explorer 10 en la manera d'estàndards

== Canvis per desenvolupadors ==
* Els controladors dels terminals Braille ja suporten la selecció de port manual. (#426)
* Això és molt útil per als terminals Braille que suporten la connexió a través d'un port sèrie llegat.
* Això es pot fer amb el mètode de la classe getPossiblePorts a la classe BrailleDisplayDriver
* Ja es suporta l'entrada des de teclats Braille. (#808)
* Ara, les entrades Braille es troben a la classe del brailleInput.BrailleInputGesture,o a les subclasses d'aquest.
Les subclasses del braille.BrailleDisplayGesture (implementat als controladors dels terminals Braille) també es poden heretar del brailleInput.BrailleInputGesture. Això permet mostrar ordres i entrades Braille que poden ser gestionades per la mateixa classe gesture.
* Ja podeu fer servir l'objecte comHelper.getActiveObject per obtenir un objecte COM actiu des d'un procés normal quan NVDA funciona amb els privilegis UIAccess. (#2483)

## 2012.3

Les principals novetats d'aquesta versió inclouen suport per a l'entrada de caràcters asiàtics; suport experimental per a pantalles tàctils sobre Windows 8; l'informe de la numeració de les pàgines, i el suport millorat per a les taules a l'Adobe Reader; les ordres de navegació a les files de les taules que tenen el focus, i els controls en forma de llista; suport per molts més terminals Braille; i l'informe de files i columnes al Microsoft Excel.

### Noves característiques

* NVDA ja suporta l'entrada de caràcters asiàtics utilitzant l'IME i els mètodes d'entrada de serveis de text a totes les aplicacions, incloent-hi:
* L'informe i navegació de les llistes candidates;
* L'informe i navegació de les cadenes de text; i
* L'informe de les cadenes de text,
* Ja s'informa del subratllat i tatxat a l'Adobe Reader. (#2410)
* Quan es troba activa la funció tecles enganxifoses del Windows , la tecla modificadora del NVDA es comporta com altres tecles modificadores. Això permet utilitzar la tecla modificadora del NVDA sense haver de mantenir-la premuda mentre es premen altres tecles. (# 230)
* Ja es suporta l'informe automàtic dels encapçalaments de les columnes i les files al Microsoft Excel. Premeu NVDA+Maj+c per establir la fila que conté els encapçalaments de columna i NVDA+Maj+r per establir la columna que conté els encapçalaments de les files. Premeu qualsevol ordre dues vegades per esborrar aquesta configuració. (#1519)
* Suport per als terminals HIMS Braille Sense, Braille EDGE i SyncBraille braille. (#1266, #1267)
* NVDA informa de l'aparició de les notificacions del Windows 8, si es troba activat l'informe d'indicadors de funció. (#2143)
* Suport experimental per a pantalles tàctils sobre Windows 8, incloent-hi:
* La lectura directa del text sota el dit, mentre aquest es mou al voltant del contingut.
* Diversos gestos per millorar la navegació d'objectes, la revisió de text, i d'altres ordres NVDA.
* Suport per VIP Mud. (#1728)
* A l'Adobe Reader, si una taula te un resum associat, ara es presenta. (#2465)
* A l'Adobe Reader, els encapçalaments de les files i les columnes pot ésser informat. (#2193, #2527, #2528)
* Nous idiomes: amhàric, coreà, nepalès, eslovè.
* NVDA ja pot llegir els suggeriments d'auto emplenat  al escriure adreces de correu al Microsoft Outlook 2007. (#689)
* Noves variants de veu per l'eSpeak: Gene, Gene2. (#2512)
* A l'Adobe Reader, s'informa de la numeració de les pàgines. (#2534)
* A l'Adobe Reader XI, s'informa de les etiquetes de les pàgines que hi són presents, reflectint els canvis de numeració de les diferents seccions, etc. En versions anteriors, no és possible, i només s'informa de la numeració de les pàgines.
* Ara, es pot reiniciar la configuració del NVDA per la de fàbrica prement tres vegades consecutives la combinació NVDA+control+r, o triant l'opció Reinicialitza la configuració als valors per defecte en el menú del NVDA. (#2086)
* Suport per a les versions 3, 4 i 5 del terminal Braille Seika 80 de Nippon Telesoft. (#2452)
* El primer i l'últim dels botons d'enrutament del terminal Braille Freedom Scientific PAC Mate i Focus Braille ara poden utilitzar-se per a desplaçar-se cap a enredera i endavant. (#2556)
* Moltes més funcionalitats suportades pel terminal Braille Freedom Scientific Focus, com barres avançades, rocker bars i determinades combinacions de punts per accions comunes. (#2516)
* A les aplicacions que fan servir IAccessible2, com per exemple les aplicacions Mozilla, es pot informar dels encapçalaments de les files i les columnes de les taules fora del mode de navegació. (#926)
* Suport preliminar per al control del document al Microsoft Word 2013. (#2543)
* Ara, es pot informar de l'alineació del text a les aplicacions utilitzant la IAccessible2, com a les aplicacions Mozilla. (#2612)
* Quan la fila d'una taula o un control estàndard en forma de llista del Windows amb múltiples columnes rep el focus, pots utilitzar les ordres de navegació per la taula per accedir a les diferents cel·les. (#828)
* Noves taules de traducció Braille: estonià grau 0, portuguès 8 punts de Braille per ordinador, Italià 6 punts de Braille per ordinador. (#2319, #2662)
* Si NVDA es troba instal·lat en el sistema, a l'obrir el paquet d'un complement (per exemple, des de l'explorador del Windows, o després de la seva descàrrega des del navegador) s'instal·larà directament al NVDA. (#2306)
* Suport per als models més nous dels terminals Braille Papenmeier BRAILLEX. (#1265)
* Ara, s'informa de la posició (per exemple, 1 de 4) dels elements de les llistes a l'explorar del Windows  i posteriors. Això també inclou controls UIAutomation que suportin les propietats personalitzades itemIndex i itemCount. (#2643) 

== Canvis ==
* En el diàleg de preferències del cursor de revisió del NVDA, s'ha canviat el nom de l'opció de seguiment del focus del teclat per seguiment del focus del sistema, per un tema de coherència amb la terminologia emprada a altres opcions  del NVDA.
* Quan es revisa amb el Braille, i el cursor es troba sobre un objecte no textual (per exemple, un camp de text editable), les tecles de moviment del cursor activaran l'objecte. (#2386)
* L'opció desa la configuració en sortir es troba activada per defecte per a les noves configuracions.
* en actualitzar una versió del NVDA instal·lada prèviament, la tecla de drecera de l'escriptori no es veu forçada a tornar a la combinació control+alt+n, en el cas que aquesta hagi estat modificada manualment per l'usuari. (#2572)
* Ara, la llista de complements del gestor de complements mostra primer el nom del paquet abans que el seu estat. (#2548)
* Si instal·les la mateixa o una altra versió d'un complement ja instal·lat, NVDA us preguntarà si vols actualitzar-lo, en comptes de mostrar un error i avortar la instal·lació. (#2501)
Ara, les ordres de la navegació d'objectes (excepte l'informe de l'ordre de l'objecte actual), informen amb menys loquacitat. Podeu continuar obtenint informació addicional, utilitzant l'informe de l'ordre de l'objecte. (#2560)
* Traductor liblouis braille actualitzat a la versió 2.5.1. (#2319, #2480, #2662, #2672)
* S'ha canviat el nom del document Referència ràpida d'ordres de teclat del NVDA per Referència ràpida d'ordres, ja que ara inclou ordres tàctils a més de ordres de teclat.
* La llista d'elements en el mode de navegació, ara recorda l'últim tipus d'element mostrat (per exemple, enllaços, encapçalaments o regions) cada vegada que el diàleg es mostra durant la mateixa sessió del NVDA. (#365)
* La majoria d'aplicacions Metro del Windows 8 (per exemple, Mail  o Calendar) ja no activen el mode de navegació per tota l'aplicació.
* S'ha actualitzat Handy Tech BrailleDriver COM-Server a la versió 1.4.2.0.

== Correccions d'errors ==
* Al Windows Vista i posteriors, NVDA ja no tracta incorrectament la tecla Windows quan es manté premuda al desbloquejar el Windows, després d'haver-lo bloquejat amb la combinació Windows+l. (#1856)
* A l'Adobe Reader, els encapçalaments de les files ja són reconeguts correctament com a cel·les de la taula; això vol dir que s'informa de les coordenades i que s'hi pot accedir amb les ordres de navegació de les taules. (#2444)
* A l'Adobe Reader, les cel·les d'una taula que ocupen més d'una columna i/o fila, ja es gestionen correctament. (#2437, #2438, #2450)
* Ara, el paquet de la distribució del NVDA comprova la seva integritat abans d'executar-se. (#2475)
* Ara, els fitxers de descàrregues temporals s'esborren si la descàrrega d'una actualització del NVDA falla. (#2477)
* NVDA ja no es bloqueja en copiar la configuració de l'usuari a la configuració del sistema quan s'executa com administrador (pel seu ús a la pantalla d'inici de sessió del Windows i altres pantalles de seguretat). (#2485)
* Ara es presenten millor les finestres en mosaic de la pantalla d'inici del Windows 8. Ja no es repeteix el nom,  no s'informa dels elements no seleccionats a totes les finestres, i la informació d'estat es presenta com la descripció de la finestra (per exemple, la temperatura actual per la finestra que mostra el temps).
* Al llegir els camps de contrasenyes del Microsoft Outlook i altres controls d'edició estàndards, les contrasenyes ja no es llegeixen, i aquests camps es marquen com a protegits. (#2021)
* A l'Adobe Reader, els canvis als camps dels formularis es reflecteixen correctament al mode de navegació. (#2529)
* Suport millorat  per al corrector ortogràfic del Microsoft Word, incloent-hi una lectura més acurada de l'actual error, i el suport per aquest corrector sobre una instància del NVDA instal·lada al Windows Vista o superiors.
* Ara, els complements que inclouen fitxers que contenen caràcters no anglesos es poden instal·lar correctament en la majoria dels casos. (#2505)
* A l'Adobe Reader, l'idioma del text no es perd quan s'actualitza o quan l'usuari s'hi desplaça. (#2544)
* Ara, en instal·lar un complement, el diàleg de confirmació mostra correctament, en el cas que estigui disponible, el nom traduït del complement. (#2422)
* A les aplicacions que utilitzen UI Automation (com per exemple, les aplicacions .net i Silverlight), s'ha corregit el càlcul dels valors numèrics per a controls com els lliscants. (#2417)
* La configuració dels informes de les barres de progrés ara es reconeix per a barres de progrés indeterminades mostrades per NVDA a l'instal·lar, crear una còpia portable, etc. (#2574)
-Les ordres NVDA ja no poden ser executades des d'un terminal Braille mentre es troba activa una pantalla de seguretat (per exemple, la pantalla de bloqueig). (#2449)
* En el mode de navegació, s'actualitza el Braille si el text visualitzat canvia. (#2074)
-  Ara, quan es verbalitza o visualitza Braille a través del NVDA a les pantalles de seguretat del Windows com, per exemple, la pantalla de bloqueig, aquest es ignorat.
* Ja no es possible anar a la part inferior del document amb la tecla fletxa dreta quan el caràcter final, o el final d'un contenidor són l'últim ítem del document. (#2463)
* Ja no s'inclou de manera incorrecta continguts estranys a l'informar del text de diàlegs a les aplicacions web (específicament, en diàlegs ARIA sense l'atribut aria-describedby). (#2390)
* NVDA ja no informa o localitza incorrectament determinats camps editables en els documents MSHTML (per exemple, a l'Internet Explorer), específicament quan l'autor de la pàgina web ha utilitzat un rol ARIA. (#2435)
* Ja es gestiona correctament la tecla de retrocés en verbalitzar les paraules escrites a les consoles d'ordres del Windows. (#2586)
* Les coordenades de les cel·les del Microsoft Excel es tornen a mostrar en Braille.
* Al Microsoft Word, NVDA ja no et deixa enganxat en un paràgraf amb una llista al intentar navegar fora del pic o del número amb la tecla esquerra o control + tecla esquerra. (#2402)
* En el mode de navegació dins d'aplicacions Mozilla, els ítems de determinades llistes combinades (específicament llistes combinades ARIA), ja no es renderitzen incorrectament.
* En el mode de navegació dins d'aplicacions Mozilla, determinats controls que es renderitzaven amb una etiqueta incorrecta o simplement amb un espai en blanc, ara es renderitzen amb l'etiqueta correcta.
* S'ha eliminat un espai en blanc estrany que apareixia a les aplicacions Mozilla quan s'utilitzava el mode de navegació.
* En el mode de navegació dins dels navegadors web, determinats gràfics marcats específicament com decoratius (amb l'atribut alt buit) s'ignoren correctament.
* En els navegadors web, NVDA oculta el contingut marcat com ocult per als lectors de pantalla (específicament, quan s'utilitza l'atribut aria-hidden). (#2117)
* Les quantitats monetàries negatives (per exemple, -$123) es verbalitzen correctament com a negatives, amb independència del nivell del símbol. (#2625)
* Durant el mode verbalitza-ho tot, NVDA ja no torna incorrectament a l'idioma per defecte on les línies no finalitzen una frase. (#2630)
* La informació de les fonts ja es detecta correctament a l'Adobe Reader 10.1 i posteriors. (#2175)
* A l'Adobe Reader, si es proporciona un text alternatiu, només es renderitza aquest text. Anteriorment, en alguns casos s'incloïa també un text estrany . (#2174)
* Quan el document conté una aplicació, el contingut de  l'aplicació ja no s'inclou en el mode de navegació. Això prevén que l'usuari es desplaci inesperadament dins de l'aplicació durant la navegació. Podeu interactuar amb l'aplicació de la mateixa manera que ho feu amb els objectes embeguts. (#990)
* A les aplicacions Mozilla, ja s'informa correctament del valor dels botons de selecció de valors quan aquests canvien. (#2653)
* S'ha actualitzat el suport per a l'Adobe Digital Editions per tal que funcioni amb la versió 2.0. (#2688)
* Prémer NVDA+fletxa amunt en un quadre combinat del Internet Explorer o altres documents MSHTML, ja no llegirà tots els ítems. Alternativament, només s'activarà l'ítem que ha de ser llegit. (#2337)
* Els diccionaris de veu ja es desen correctament a l'utilitzar números (#) dins del patrons o camps de reemplaçament. (#961)
* El mode de navegació per als documents MSHTML (per exemple, Internet Explorer) ja mostra correctament el contingut visible dins de contingut ocult (especificament, aquells elements amb l'estil visibility:visible dins d'un element amb l'estil visibility:hidden). (#2097)
* Els enllaços al Centre de seguretat del Windows XP, ja no informen de cap text arbitrari després del seu nom. (#1331)
* Els controls de text de la UI Automation (per exemple, el formulari de cerca del Windows 7 i 8 al menú d'inici) ja s'anuncien correctament en moure el ratolí en comptes de romandre en silici.
* Ja no s'informa dels canvis de disposició del teclat en el mode "verbalitza-ho tot", cosa que era particularment problemàtica en els documents multilingües, inclosos els textos en àrab. (#1676)
* El contingut complet de determinats controls de text editables de la UI Automation (per exemple, el formulari de cerca del Windows 7 i 8 al menú d'inici) ja no s'anuncien cada vegada que canvien.
* Al moure't entre els grups de la pantalla d'inici del Windows 8, els grups sense etiquetar ja no anuncien la seva primera finestra com a nom del grup. (#2658)
* A l'obrir la pantalla d'inici del Windows 8, el focus es posiciona correctament a la primera finestra, en comptes de saltar a l'arrel de la pantalla d'inici, podent causar confusió en la navegació. (#2720)
* NVDA ja no falla en iniciar-se quan el camí al perfil de l'usuari conté determinats caràcters multibyte. (#2729)
* En el mode de navegació dins del Google Chrome, el text de les pestanyes es renderitza correctament.
* En el mode de navegació, ja s'informa correctament dels botons dels menús.
* Al Calc de l'OpenOffice/LibreOffice, la lectura de les cel·les dels fulls de càlcul ja funciona correctament. (#2765)
* NVDA ja torna a funcionar a la llista de missatges del gestor de correu del Yahoo!, quan s'utilitza des de l'Internet Explorer. (#2780)

== Canvis per desenvolupadors ==
* L'anterior fitxer de registre, s'ha copiat a nvda-old.log a la inicialització del NVDA. Per tant, si NVDA falla o es reinicia, la informació de l'inici de sessió es manté disponible per a la seva inspecció. (#916)
* La obtenció de la propietat role en chooseNVDAObjectOverlayClasses ja no fa que el rol sigui incorrecte, i no s'informi d'ell quan determinats objectes com les consoles d'ordres del Windows o els controls Scintilla reben el focus. (#2569)
* Els menús de preferències, eines i ajuda del NVDA, són accessibles com atributs a gui.mainFrame.sysTrayIcon com preferencesMenu, toolsMenu i helpMenu respectivament. Això permet als complements, afegir fàcilment nous elements a aquests menús.
* S'ha canviat el nom de l'script navigatorObject_doDefaultAction dels globalCommands, per review_activate.
* Ja es suporten els missatges contextuals del Gettext. Això permet establir múltiples traduccions per a un únic missatge en anglès segons el context. (#1524)
* Això es fa amb la funció pgettext(context, missatge)
* És suportat tant per NVDA com pels seus complements.
* xgettext i msgfmt del GNU gettext s'han d'utilitzar per crear qualsevol fitxer PO i MO. Les eines Phyton no suporten els missatges contextuals.
* For xgettext, pass the --keyword=pgettext:1c,2 command line argument to enable inclusion of message contexts.
* Vegeu https://www.gnu.org/software/gettext/manual/html_node/Contexts.html#Contexts per saber-ne més.
* Ara és possible accedir als mòduls incorporats al NVDA quan aquests s'han anul·lat per tercers mòduls. Vegeu el mòdul nvdaBuiltin per saber-ne més.
* El complement de suport a la traducció es pot utilitzar amb el mòdul installTasks. (#2715)

= 2012.2.1 =
Aquesta versió soluciona diversos problemes potencials de seguretat (mitjançant l'actualització a Python 2.7.3).

= 2012.2 =
Aspectes destacats d'aquesta versió són la creació d'un instal·lador incorporat i portable, les actualitzacions automàtiques, la gestió senzilla de nous complements NVDA, l'anunci de gràfics en el Microsoft Word, el suport per a les aplicacions de Windows 8 Metro, i diverses correccions importants d'errors.  

== Noves característiques ==
* Ara, NVDA pot buscar, baixar i instal·lar  actualitzacions de forma automàtica. 
(#73)
* Ampliar les funcionalitats de NVDA s'ha fet més senzill mitjançant l'adició d'un Gestor de complements (es pot trobar sota Eines en el menú NVDA) que permet instal·lar i desinstal·lar nous paquets de complements NVDA (fitxers .nvda-addon) que continguin connectors i controladors. Cal remarcar que el gestor de complements no mostra els connectors i controladors més antics que hagin estat copiats manualment al directori de configuració (#213)
* Moltes característiques habituals de NVDA treballen ara en les aplicacions del Windows 8 estil Metro quan s'està fent servir una versió instal·lada de NVDA, incloent la parla dels caràcters escrits i el mode de navegació per documents web (inclou suport per la versió Metro de Internet Explorer 10). Les còpies portables de NVDA no poden accedir a les aplicacions estil Metro. (#1801)
* En mode de navegació  de documents Internet Explorer, Firefox, etc.), És possible ara anar al principi i al final d'alguns elements contenidors (com ara llistes i taules) amb Maj+, i, respectivament. (#123)
* Nou idioma: Grec.
* Ara, els gràfics i el text alternatiu són informats en el documents del Microsoft Word. (#2282, #1541)

== Canvis ==
* L'anunci de cel·les combinades en el Microsoft Excel es fa ara després del contingut i no abans, i només s'inclou si l'informe de taules i informe de cel·les combinades en taules estan activats en el diàleg de configuració del format del document. (#320)- NVDA es distribueix ara en un paquet. Enlloc de les versions separades portable i instal·lador ara hi ha només un fitxer que, quan s'activa, inicia una còpia temporal de NVDA i permet instal·lar el producte o generar una distribució portable. (#1715)
* NVDA s'instal·la ara sempre en el directori Fitxers de Programa de tots els sistemes. Si es fa una actualització sobre una instal·lació prèvia el programa es mourà de forma automàtica a l'esmentada carpeta si originàriament no estava instal·lat allí  

== Correccions d'errors ==
Amb la selecció automàtica de llenguatge activada, s'informa de continguts com text alternatiu per gràfics i etiquetes per altres controls al Mozilla Gecko (e.g. Firefox), sempre i quan s'hagi marcat apropiadament el llenguatge correcte.
* Verbalitza-ho tot a BibleSeeker (i en altres controls TRxRichEdit) ja no s'atura al mig d'un passatge.- Es llegeixen correctament les llistes trobades a les propietats de fitxer de Windows 8 Explorer (pestanya permisos) i a Windows 8 Windows Update.
* S'han corregit possibles aturades a MS Word que tenien lloc quan prenia més de 2 segons l'extracció de text d'un document (línies extremadament llargues o taules de continguts). (#2191)
* La detecció de trencaments de paraules funciona ara correctament quan els espais en blancs són seguits per determinades puntuacions. (#1656)
* En mode de navegació a l'Adobe Reader, es pot ara navegar a encapçalaments sense nivell, tot usant la navegació ràpida i la llista d'elements. (#2181)- Al Winamp, el braille s'actualitza ara correctament quan et mous cap a un ítem diferent en Editor de la Llista de Reproducció. (#1912)- L'arbre en la Llista d'Elements (disponible per a documents en mode de navegació) té ara una mida prou adequada com per mostrar el text de cada element. (#2276)
* A les aplicacions que facin servir el Java Access Bridge, els camps de text editable es presenten ara correctament en Braille.(#2284)- A les aplicacions que facin servir el Java Access Bridge, els camps de text editable  ja no reporten estranys caràcters en determinades circumstàncies. (#1892)- A les aplicacions que facin servir el Java Access Bridge, ara s'informa correctament de la línia en curs quan s'està al final d'un camp de text editable. (#1892)
* En mode de navegació, a aplicacions que usen Mozilla Gecko 14 i posteriors (per exemple Firefox 14), la navegació ràpida ara funciona per blockquotes i objectes incrustats. (#2287)
* A Internet Explorer 9, NVDA ja no llegeix contingut no desitjat quan el focus es mou a l'interior de determinats punts de referència o elements enfocables (específicament un element div que pot rebre el focus o que té un paper de punt de referència ARIA) 
* La icona NVDA per a l'escriptori NVDA i les dreceres cap al menœ d'inici es mostren ara adequadament en l'edició de 64 bits de Windows. (#354)

== Correccions d'errors ==
* Amb la selecció automàtica de llenguatge activada, s'informa de continguts com text alternatiu per gràfics i etiquetes per altres controls al Mozilla Gecko (e.g. Firefox), sempre i quan s'hagi marcat apropiadament el llenguatge correcte.
* Verbalitza-ho tot a BibleSeeker (i en altres controls TRxRichEdit) ja no s'atura al mig d'un passatge.- Es llegeixen correctament les llistes trobades a les propietats de fitxer de Windows 8 Explorer (pestanya permisos) i a Windows 8 Windows Update.
* S'han corregit possibles aturades a MS Word que tenien lloc quan prenia més de 2 segons l'extracció de text d'un document (línies extremadament llargues o taules de continguts). (#2191)
* La detecció de trencaments de paraules funciona ara correctament quan els espais en blancs són seguits per determinades puntuacions. (#1656)
* En mode de navegació a l'Adobe Reader, es pot ara navegar a encapçalaments sense nivell, tot usant la navegació ràpida i la llista d'elements. (#2181)- Al Winamp, el braille s'actualitza ara correctament quan et mous cap a un ítem diferent en Editor de la Llista de Reproducció. (#1912)- L'arbre en la Llista d'Elements (disponible per a documents en mode de navegació) té ara una mida prou adequada com per mostrar el text de cada element. (#2276)
* A les aplicacions que facin servir el Java Access Bridge, els camps de text editable es presenten ara correctament en Braille.(#2284)- A les aplicacions que facin servir el Java Access Bridge, els camps de text editable  ja no reporten estranys caràcters en determinades circumstàncies.  (#1892)- A les aplicacions que facin servir el Java Access Bridge, ara s'informa correctament de la línia en curs quan s'està al final d'un camp de text editable. (#1892)
* En mode de navegació, a aplicacions que usen el Mozilla Gecko 14 i posteriors (per exemple Firefox 14), la navegació ràpida ara funciona per blockquotes i objectes incrustats. (#2287)
* A Internet Explorer 9, NVDA ja no llegeix contingut no desitjat quan el focus es mou a l'interior de determinats punts de referència o elements enfocables (específicament un element div que és enfocable o que té un paper de punt de referència ARIA) 
* La icona NVDA per a l'escriptori NVDA i les dreceres cap al menœ d'inici es mostren ara adequadament en l'edició de 64 bits de Windows. (#354)

== Canvis per desenvolupadors ==
* A causa de la substitució de l'anterior instal·lador NSIS  per a NVDA  per un instal·lador integrat en Python, ja no és necessari per als traductors mantenir un fitxer langstrings.txt per a l'instal·lador. Totes les cadenes de localització estan ara gestionades per els fitxers gettext po.

## 2010.2

Notables característiques d'aquesta versió són: una navegació d'objectes considerablement simplificada; memòries intermèdies virtuals per al contingut de l'Adobe Flash; accés a diversos controls que abans eren inaccessibles mitjançant la recuperació de text escrit a la pantalla; revisió plana del text de la pantalla; suport per documents IBM Lotus Symphony; informe dels encapçalaments de files i columnes en el Mozilla Firefox, i millores significatives en la documentació de l'usuari.

### Noves característiques

* La navegació pels objectes amb el cursor de revisió s'ha simplificat molt. El cursor de revisió ara exclou objectes que no són útils a l'usuari.; per exemple, objectes que només es fan servir amb finalitats de disseny i objectes no accessibles.
* En aplicacions que fan servir Java Access Bridge (incloent OpenOffice.org), ara s'informa del format en els controls de text.  (#358, #463)
* Quan es mogui el ratolí sobre les cel·les del Microsoft Excel, NVDA  ho anunciarà de forma adequada. 
* En aplicacions que fan servir Java Access Bridge, el text d'un quadre de diàleg s'anuncia quan apareix el quadre de diàleg.  (#554)
* Una memòria intermèdia virtual es pot fer servir quan es navega en continguts de l'Adobe Flash Player. Ja es suporta la navegació d'objectes i la interacció directa amb els controls (tot activant el mode de focus). (#453)
* Els controls de text editable, incloent el l'editor de codi, són ara accessibles a Eclipse IDE. Es pot estar usant Eclipse 3.6 o posterior.  (#256, #641)
* NVDA pot ara recuperar la major part del text escrit a la pantalla. (#40, #643)
* Això permet la lectura de controls que no exposin la informació de forma més directa o fiable.  
* Els controls que s'han fet accessibles amb aquesta característica són : alguns ítems de menú que mostren icones (per exemple el menú "Obrir amb" de Xindows XP) (#151), camps de text editables en aplicacions Windows Live (#200), la llista d'errors a Outlook Express (#582), el control de text editable a TextPad (#605), les llistes a Eudora, molts controls a Australian E-tax i la barra de fórmules del Microsoft Excel
* Suport per a l'editor de codi del Microsoft Visual Studio 2005 i 2008. Com a mínim es requereix Visual Studio Standard; no funciona en les edicions Express. (#457)
* Suport per documents IBM Lotus Symphony.
* Suport experiment primerenc per a Google Chrome. Si us plau, prengueu nota que el lector de pantalla de Chrome és lluny de ser complet i cal fer encara feina addicional amb NVDA. Caldrà que es disposi d'una compilació recent de Chrome per provar-ho. 
* L'estat de les tecles de commutació (Bloq Maj, Bloq Núm i Bloq Despl) es mostra ara en Braille quan es premen. (#620)
* Els Globus d'ajuda es mostren ara en Braille quan escau. (#652)
* S'ha afegit un controlador per la línia Braille MDV Lilli. (#241)
* Ara  s'anuncia la selecció d'una fila o columna sencera en el Microsoft Excel, amb les tecles de drecera Maj+Espai i Control+Espai, (#759)
* Ara s'anuncien els encapçalaments de files i columnes. Això es pot configurar des del quadre de diàleg Formatació de documents. 
* Això és suportat actualment per documents de aplicacions Mozilla, com Firefox (versió 3.6.11 i posteriors) i   Thunderbird (version 3.1.5 i posteriors). (#361)
* S'han introduït comandaments per revisions planes: (#58)
* NVDA+TeclNum7 commuta a revisió plana, tot col·locant el cursor de revisió a la posició de l'objecte principal, tot permetent la revisió de la pantalla (o d'un document si n'hi ha un) amb els comandaments de revisió de text.
* NVDA+TeclNum1 mou el cursor de revisió dins de l'objecte representat pel text a la posició del cursor de revisió, tot permetent la navegació per l'objecte a partir d'aquest punt.
* Els paràmetres actius de l'usuari NVDA poden ser copiats per a ser usats en pantalles segures de Windows, com les d'inici de sessió o UAC, tot prement un botó en el quadre de diàleg Paràmetres Generals.
* Suport per al Mozilla Firefox 4.
* Suport per al icrosoft Internet Explorer 9.

== Canvis ==
* S'han eliminat momentàniament els següents comandaments : el sayAll per a l'objecte de navegació (NVDA+TeclNumSuma; el objecte de navegació posterior en el flux (NVDA+Maj+TeclNúm6) i l'objecte de navegació anterior en el flux (NVDA+Maj+TeclNum4). L'eliminació dels comandament s'ha fet per eliminar errors i per alliberar les tecles per afegir altres possibles funcions. 
* En el quadre de diàleg Sintetitzador de NVDA, només es mostra el nom de visualització del sintetitzador. Abans apareixia prefixat el nom del controlador, el qual només és rellevant a nivell intern.  
* En aplicacions incrustades o en memòries intermèdies virtuals dins d'un altra memòria intermèdia virtual (per exemple, l'Adobe Flash) es pot ara prémer NVDA+Control+Espai per sortir de l'aplicació incrustada o de la memòria intermèdia virtual i anar cap el document contenidor. Abans es feia servir per això NVDA+espai. Ara NVDA+espai es fa servir només per commutar els modes de navegació i de focus a les memòries intermèdies virtuals.
* Si el visor de veu (activat amb el menú Eines) rep el focus (per exemple si es clica dins) el nou text no apareixerà en el control fins que el focus s'allunyi. Això permet la selecció de text amb major facilitat (per exemple, per copiar).
* El Visor de registre i la Consola Phyton es maximitzen quan estan activats.
* Quan el focus en un full de càlcul del Microsoft Excel o Similar afecta a més d'una cel·la, s'anuncia el rang de selecció i no només la cel·la activa. (#763)
* El guardat de la configuració i el canvi d'opcions sensibles ara està desactivat quan s'inicia sessió amb UAC i d'altres pantalles segures de Windows.
* El sintetitzador eSpeak s'ha actualitzat a la versió 1.44.03.
* Si NVDA està ja iniciat, l'activació de l'accés directe NVDA en l'escriptori (que inclou prémer Control+Alt+N) reiniciarà  NVDA.
* S'ha eliminat el text informatiu sota les caselles relatives al ratolí en el quadre de diàleg Opcions del ratolí i s'ha reemplaçat amb una casella Habilita el seguiment del ratolí que respon millor a la commutació del script del seguiment del ratolí
* S'ha actualitzat la distribució de teclat d'ordinador portàtil de forma que ja inclou tots els comandaments disponibles en l'escriptori i treballa correctament en teclats de configuració no anglesa.  (#798, #800)
* S'han fet millores i actualitzacions significatives en la documentació de l'usuari, tot incloent documentació sobre els comandaments dels teclats d'ordinador portàtil i sobre la sincronització de la Guia de referència ràpida de comandaments de teclat amb la Guia de l'usuari (#455)
* El traductor Liblouis Braille s'ha actualitzat a la versió  2.1.1. Cal destacar que soluciona alguns problemes relacionats amb el Braille xines així com amb caràcters que es troben poc definits per la taula de transliteració. (#484, #499)

== Correccions d'errors ==
* A µTorrent, el ítem enfocat en la llista de torrents no apareix reportat de forma repetida ni tampoc roba el focus quan un menú està obert.  
* A µTorrent, ara s'informa dels noms dels fitxers en la llista de continguts Torrent.   
* A les aplicacions Mozilla, ara ja es detecta correctament el focus quan s'atura sobre una taula buida o un arbre.  
* A les aplicacions Mozilla ara el "no verificat" s'informa correctament en controls amb caselles com ara les cel·les d'una taula que tinguin caselles. (#571)
* A les aplicacions Mozilla el text dels quadres de diàleg ARIA implementats correctament ja no s'ignoren i s'informen de forma correcta quan apareix el quadre de diàleg. . (#630)
* A Internet Explorer i altres controls MSHTML l'atribut de nivell ARIA apareix ara representat correctament. 
* A Internet Explorer i altres controls MSHTML, el rol d'ARIA pot escollir-se per damunt d'altres tipus d'informació amb la finalitat de donar una experiència ARIA més correcta i predicible.  
* S'ha aturat un estrany accident a Internet Explorer quan es navega per marcs o iMarcs. 
* En documents del Microsoft Word es possible llegir de nou les línies de dreta a esquerra (com en el text àrab). (#627)
* S'ha reduït molt el retard quan es mostren grans quantitats de text en una consola de comandaments Windows en un sistema de 64 bits. (#622)
* Si l'Skype ja s'ha inicialitzat quan s'inicia NVDA ja no serà necessari reiniciar l'Skype per assegurar-ne l'accessibilitat. Això pot ser també vàlid per altres aplicacions que analitzen l'indicador de seguiment de lectura de pantalla.
* En aplicacions Microsoft Office, NVDA ja no es penja quan està activada la parla en segon pla  (NVDA+b) o quan es navega per alguns objectes de la barra d'eines. (#616)
* S'ha corregit la pronuncia incorrecta de números que contenien un zero després d'un separador; per exemple 1.023. (#593)
* l'Adobe Acrobat Pro i Reader 9 ja no es pengen quan es tanca un fitxer o quan es fan algunes altres tasques. (#613)
* Ara s'anuncia la selecció quan es prem Control+a amb la finalitat de seleccionar tot el text en alguns controls de text editable, com ara en el Microsoft Word. (#761)
* En els controls Scintilla (per exemple en  Notepad++), el text ja no es selecciona de forma incorrecta quan NVDA mou el cursor, per exemple, durant un SayAll. (#746)
* Ara és de nou possible revissar els continguts de les cel·les en el Microsoft Excel amb el cursor de revisió. 
* NVDA pot de nou llegir per línia en alguns camps textArea problemàtics d'Internet Explorer 8. (#467)
* Windows Live Messenger 2009 ja no es tanca immediatament si s'inicia sessió mentre NVDA s'està executant.  (#677)
* En navegadors web ja no cal prémer TAB per a interactuar amb un objecte incrustat (com els continguts Flaix) un cop premut retorn en l'objecte incrustat o bé quan es retorna cap aquest des d'una altra aplicació.  (#775)
-En controls Scintilla (e.g. Notepad++), l'inici de les línies llargues ja no apareix truncat quan questes marxen ora de la pantalla. A més, aquestes línies llargues es mostraran correctament en Braille quan se seleccionin.
* A Loudtalks, ja és possible accedir a la llista de contactes.
* La URL dels documents i  "MSAAHTML Registered Handler" ja no s'informen falsament a Internet Explorer i en altres controls MSHTML. (#811)
* En les vistes d'arbre de Eclipse IDE, l´´item prèviament enfocat ja no s'anuncia incorrectament quan el focus es mou cap un nou ítem.  
* NVDA funciona ara correctament en un sistema on el directori de treball actual hagi estat esborrat del camí de cerca DLL (mitjançant la configuració de l'entrada de registre CWDIllegalInDllSearch a 0xFFFFFFFF). Cal destacar que això no és rellevant per la major part dels usuaris.
* Quan els comandaments de navegació de les taules es fan servir fora d'una taula en el Microsoft Word, ja no es diu "vora de la taula" després de "no taula". (#921)
* Quan els comandaments de navegació de les taules. no es poden moure a causa que s'està en el límit d'una taula al Microsoft Word, "límit de la taula" ja no es diu en anglès sinó en el llenguatge en que NVDA està configurat.  (#921)
* A Outlook Express, Windows Mail and Windows Live Mail, ja s'informa de l'estat de les caselles de verificació en les llistes de normes dels missatges.(#576)
* La descripció de les normes de missatge ara es pot llegir a Windows Live Mail 2010.

= 2012.1 =
Les principals novetats d'aquesta versió inclouen noves funcionalitats per a una lectura més fluida del Braille; la indicació del format del document en Braille; l'accés a més informació sobre el format i suport millorat al Microsoft Word; i suport per l'iTunes Store.

== Noves característiques ==
* NVDA pot anunciar el nombre de tabulacions i espais en la línia acutal en el ordre en el que s'han introduït. Això es pot activar seleccionant l'informe d'indentació de les línies en el diàleg format del document. (#373)
* NVDA ja pot detectar la pulsació de tecles generada per l'emulació de teclats alternatius com els teclats de pantalla o els programaris de reconeixement de veu.
* Ara, NVDA pot detectar colors a les consoles d'ordres del Windows.
* Les negretes, cursives i el subratllat s'indica al Braille amb els signes apropiats segons la taula de traducció configurada. (#538)
* Ara s'informa de molta més informació sobre els documents del Microsoft Word, incloent-hi:
* La informació en línia com les notes a peu de pàgina o els números de les notes al final del document, els nivells dels encapçalaments, l'existència de comentaris, la nidació dels nivells de les taules, els enllaços, i el color de text; 
* S'informa de l'entrada a les seccions del document com, per exemple, els comentaris, les notes a peu de pàgina i els encapçalaments i peus de pàgina
* Ara, el Braille indica el text seleccionat utilitzant els punts 7 i 8. (#889)
* Ara, el Braille informa sobre els controls en documents, com ara enllaços, botons i encapçalaments. (#202)
* Suport per als terminals Braille hedo ProfiLine i MobilLine USB braille. (#1863, #1897)
* Ara, NVDA evita separar paraules al braille quan sigui possible de forma predeterminada. Aquest comportament pot ser desactivat en el diàleg de configuració del Braille. (#1890, #1946)
* Ara és possible mostrar el braille per paràgrafs en comptes de mostrar-lo per línies. Això permet una lectura més fluida en textos llargs. Aquesta característica es configurable mitjançant l'opció Llegir per paràgrafs del diàleg de configuració del Braille. (#1891)
* En el mode de navegació podeu activar l'objecte sota el cursor utilitzant un terminal braille. Aquesta funcionalitat s'activa prement la tecla de guiat del cursor, allà on es trobi el cursor (es a dir, prement dues vegades si el cursor no es troba allí). (# 1893)
* Suport bàsic per àrees del web a l'iTunes i l'Store. També es suporten altres aplicacions que utilitzen WebKit 1. (#734)
* Ara, les pàgines dels llibres a l'Adobe Digital Editions 1.8.1 i posteriors, passen automàticament a l'utilitzar l'opció "verbalitza-ho tot". (#1978)
* Noves taules de traducció Braille: portuguès grau 2, Braille d'ordinador de 8 punts islandès, tàmil grau 1, Braille d'ordinador de 8 punts espanyol, persa grau 1. (#2014)
* Ara pots configurar si vols que s'anunciïn els marcs en els documents des del diàleg de preferències del Format de Documents. (#1900)
* El mode de suspensió s'activa automàticament a l'utilitzar l'OpenBook. (#1209)
* En Poedit, ara els traductors poden llegir els comentaris afegits i extrets automàticament. Els missatges sense traduir o provisionals es marquen amb una estrella i s'emet un xiulet quan es navega per ells. (#1811)
* Suport per als terminals Braille HumanWare Brailliant BI i B series. (#1990)
* Nous idiomes: noruec, bokmål, xinès tradicional (Hong Kong).

== Canvis ==
* Les ordres per descriure el caràcter actual o per lletrejar la paraula o línia actual, ara es lletrejarà en l'idioma apropiat d'acord amb el text, si el canvi automàtic d'idioma està activat i la informació de l'idioma adequada està disponible.
* S'ha actualitzat el sintetitzador eSpeak a la versió 1.46.02.
* NVDA truncarà els noms extremadament llargs (30 caràcters o més) deduïts dels URLs d'imatges i enllaços que probablement no aportin res al contingut i només obstaculitzin la lectura. (#1989)
* S'han abreviat determinades informacions mostrades al Braille. (#1955, #2043)
* Quan els cursors del sistema o de revisió es mouen, ara el braille es mou de la mateixa manera com si es mogués manualment. Això ho fa més apropiat quan el braille s'ha configurat per llegir per paràgrafs i/o per evitar la partició de paraules. (#1996)
* S'ha actualitzat a la nova taula de traducció de Braille espanyol grau 1.
* Traductor liblouis braille actualitzat a la versió 2.4.1.

== Correccions d'errors ==
* Al Windows 8, el focus ja no es mou incorrectament del camp de cercca del Windows Explorer, cosa que impedia al NVDA interactuar amb ell.
* Importants millores quan els llegeix i es navega pels documents del Microsoft Word quan es troba activat l'anunci automàtic del format. D'aquesta manera és una mica més confortable la lectura del format, etc. El rendiment també podria millorar-se per alguns usuaris.
* Ara, el mode de navegació s'utilitza pel contingut l'Adobe Flash a pantalla completa.
S'ha corregit la pobre qualitat de l'àudio produïda en determinats casos, per les veus del Microsoft Speech API versió 5, quan la sortida de l'àudio no era la sortida per defecte (Microsoft Sound Mapper). (#749)
* NVDA es pot tornar a utilitzar amb el sintetitzador "sense veu", utilitzant només el Braille o el visor de veu. (#1963)
* Les ordres de navegació d'objectes ja no anuncien "Sense fills" i "Sense pares", però, en canvi, anuncien missatges consistents amb la documentació.
* Quan NVDA es configurada en un idioma diferent a l'anglès, s'informa correctament del nom de la tecla tabulador.
* Al Mozilla Gecko (per exemple, Firefox, NVDA ja no commuta intermitentment al mode de navegació mentre es navega pels menús dels documents. (#2025)
* A la calculadora, la tecla de retrocés informa del resultat actualitzat, en comptes de no informar de res. (#2030)
* En el mode de navegació, l'ordre per moure el ratolí al navegador d'objectes ara es mou al centre de l'objecte en el cursor de revisió, en lloc de moure's a la cantonada superior esquerra, fent-lo més precís en determinats casos. (#2029)
* En el mode de navegació amb el mode de focus automàtic activat per als canvis en el focus, quan la barra d'eines rep el focus, ara canviarà al mode focus. (#1339)
* L'ordre d'informe del títol torna a funcionar correctament a l'Adobe Reader.
* Amb el mode de focus automàtic activat per als canvis en el focus, el mode de focus ara s'utilitza correctament per a les cel·les de la taula que reben el focus; p. e.: en quadrícules ARIA. (#1763)
* A l'iTunes, ara s'informa correctament de la informació de posició de determinades llistes.
A l'Adobe Reader, determinats enllaços ja no es tracten com camps de text editables de només lectura.
* Les etiquetes d'alguns camps de text editables ja no s'inclouen incorrectament quan s'anuncia el text d'un diàleg. (#1960)
* S'informa de nou de la descripció dels grups si la descripció dels objectes es troba activada.
* Ara, les mides llegibles per humans s'inclouen al text del diáleg de propietats de l'explorador del Windows.
* L'anunci doble del text de la pàgina de propietats s'ha eliminat en alguns casos. (#218)
* S'ha millorat el seguiment del cursor del sistema en camps de text editables per pantalla. En concret, aquesta millora afecta a l'editor de cel·les del Microsoft Excel i a l'editor de missatges del Eudora. (#1658)
* Al Firefox 11, l'ordre per moure't al contingut de la memòria intermèdia (NVDA+Ctrl+espai) funciona correctament per a sortir dels objectes embeguts com el contingut Flash.
* NVDA ja es reinicia correctament (per exemple, després de canviar l'idioma) quan es troba en un directori que conté caràcters no ASCII. (#2079)
* El Braille respecta correctament la configuració de l'informe de les tecles de drecera dels objectes, la informació de posició i les descripcions.
* A les aplicacions Mozilla, commutar entre els modes de navegació i de focus ja no resulta tant lent quan es té activat el Braille. (#2095)
* Ara, guiar el cursor cap a l'espai al final de la línia/paràgraf utilitzant els sensors del cursor braille en alguns camps de text editables, funciona correctament en comptes de col·locar el cursor a l'inici del text. (#2096)
* NVDA torna a funcionar correctament amb el sintetitzador Audiologic Tts3. (#2109)
* Els documents del Microsoft Word es tracten correctament com a multi-línia. Això fa que el Braille es comporti d'una manera més apropiada quan el document rep el focus.
* Al Microsoft Internet Explorer, ja no es produeixen errors quan determinats controls estranys reben el focus. (#2121)
* El canvi de la pronuncia de la puntuació o dels símbols per part de l'usuari, ara té un efecte immediat , en comptes de requerir que el NVDA es reiniciï o que s'hagi desactivat el canvi automàtic d'idioma. 
* A l'utilitzar l'eSpeak, la veu ja no s'atura en determinades circumstàncies al diàleg "desa com" del visor de registre del NVDA. (#2145)

== Canvis per desenvolupadors ==
Ara es disposa d'una consola Python remota per a situacions on és útil la depuració en remot. Vegeu la guia de desenvolupador per a saber-ne més.
* Per millorar la llegibilitat, s'ha eliminat el rastreig de la ruta base del codi del NVDA en el registre. (#1880)
* Ara, els objectes TextInfo disposen del mètode activate(), per activar la posició representada pel TextInfo.
* Això es utilitzat pel braille per activar la posició fent servir tecles de guiat del cursor a la pantalla braille. No obstant això, en un futur podrien haver-hi altres trucades.
* Els TreeInterceptors i els NVDAObjects que exposen una única pàgina de text simultàniament, ara donen suport per a l'avanç automàtic de pàgines en el mode verbalitza-ho tot, quan s'utilitzen els textInfos.DocumentWithPageTurns mix-in. (#1978)
* S'han reanomenat o mogut moltes constants de control i sortida. (#228)
 * Les constants speech.REASON_* s'han mogut a controlTypes.
* En els controlTypes, les speechRoleLabels i speechStateLabels s'han reanomenat per roleLabels and stateLabels, respectivament.
* Ara, la sortida braille es registra al nivell entrada/sortida. Primerament, es registra el text sense traduïr de totes les regions, a continuació per cel·les braille de la finestra que s'està mostrant. (#2102)
* Les subclasses del sapi5 synthDriver ara poden sobrescriure _getVoiceTokens i estendre init per suportar els tokens de veu personalitzats com amb la sapi.spObjectTokenCategory per obtenir tokens des d'una localització personalitzada.

## 2011.3

Aspectes destacables d'aquesta versió són el canvi automàtic d'idioma, quan s'estan llegint documents amb apropiada informació de l'idioma; suport per entorns de 64 bits Java Runtime; informació sobre formatació de text en mode d'exploració en aplicacions Mozilla; millor maneig de bloquejos i congelacions en l'aplicació; i correccions inicials per Windows 8.

### Noves característiques

* NVDA pot ara canviar sobre la marxa l'idioma del sintetitzador eSpeak quan es llegeixen determinats documents web/pdf, tot proporcionant adequada informació de l'idioma. El canvi automàtic de llenguatge / dialecte pot ser activat i desactivat des del quadre de diàleg de Paràmetres de veu.(#845) 
* Ara es suporta Java Access Bridge 2.0.2, el que inclou suport per a entorns de 64 bits Java Runtime.
* Al Mozilla Gecko (per exemple a Firefox) els nivells d'encapçalament s'anuncien ara quan es fa servir la navegació d'objectes.  
* La formatació de text pot ser ara informada quan es fa servir el mode de navegació usant Mozilla Gecko (per exemple en Firefox i Thunderbird). (#394)
* El text subratllat o tatxat ara pot ser detectat i informat en els controls de text de l'estàndard IAccessible2, com ara en aplicacions Mozilla.
* En mode de navegació en l'Adobe Reader, s'informa ara dels recomptes de fila i columna de la taula.
* S'ha afegit suport per al sintetitzador Microsoft Speech Platform. (#1735)
* Els números de línia i pàgina estan ara informats per al signe d'intercalació en  IBM Lotus Symphony. (#1632)
* El percentatge de canvi del to quan es pronuncia una lletra majúscula es pot configurar ara des del quadre de diàleg Paràmetres de veu. Tanmateix, això no reemplaça l'antiga casella per a incrementar el to en les Majúscules (de fet, desactivar aquesta característica retorna el percentatge a 0) (#255)
* El text i el color de fons ara s'inclouen en la informació sobre el format de les cel·les en el Microsoft Excel. (#1655)
* En aplicacions que usen el Java Access Bridge, el comandament per activar els objectes de navegació, ara funciona quan és apropiat. (#1744)
* Nou idioma: Tàmil.
* Suport bàsic per Design Science MathPlayer.

== Canvis ==
* NVDA ara es reinicia sol si es bloqueja.
* S'ha abreujat alguna informació mostrada en Braille.  (#1288)
* El script per a lectura de la finestra activa (NVDA+b) ha estat millorat per a filtrar controls inútils i també és molt més senzill de silenciar.  (#1499)
* El Verbalitza-ho tot automàtic quan es carrega un document en mode de navegació és ara opcional gràcies a una funció afegida en el quadre de diàleg Mode de Navegació. (#414)  
* Quan s'intenta llegir la barra d'estat (Escriptori NVDA+Fi), si no es pot localitzar una barra d'estat real, en el seu lloc NVDA recorrerà  a usar la darrera línia del text escrit i mostrat en l'aplicació activa.  (#649)
* Quan es llegeixen documents, amb el Verbalitza-ho tot en mode de navegació, NVDA es pausarà al final dels encapçalaments i altres elements de nivell de bloc, i no es llegirà el text de forma conjunta amb el següent lot de text, com si fos una frase llarga.
* En mode de navegació, prémer Retorn o Espai en una pestanya ara l'activa enlloc de canviar a mode de focus.   (#1760)
* S'ha actualitzat el sintetitzador de veu eSpeak a la versió 1.45.47.

### Correccions d'errors

* NVDA ja no mostra vinyetes o números per a les llistes en Internet Explorer i altres MSHTML controls quan l'autor ha indicat que aquests no haurien de ser mostrats (per exemple, si l'estil de llista és "cap")   (#1671)
* El reinici de NVDA quan s'ha congelat (per exemple, quan es prem control+alt+n) ja no fa sortir de la còpia anterior sense iniciar-ne una de nova.  
* Prémer les tecles retrocés o les fletxes en una consola de comandaments Windows ja no provoca que en alguns casos hi hagi resultats estranys.  (#1612)
* L'element seleccionat en els quadres combinats WPF (i possiblement en d'altres quadres combinats que facin servir  UI Automation) els quals no permeten edició de text, és ara informat correctament.
* En mode de navegació en l'Adobe Reader, ja és sempre possible anar a la següent fila des de la fila de capçalera, i a l'inrevés, tot usant els comandaments moure's a la fila següent i moure's a la fila anterior. A més, la fila de capçalera ja no es reporta com a fila 0. (#1731)
* En mode de navegació, a l'Adobe Reader, ara és possible moure's a (i, en conseqüència, passar) les cel·les buides en una taula.
* La informació de posició insubstancial (per exemple, 0 de nivell 0) ja no s'informa en Braille.
* Quan el Braille és obligat a revisar, ara és possible mostrar contingut en revisió plana.  (#1711)
* El text d'un control de text ja no es presenta dues vegades en alguns casos en una línia Braille, per exemple, el desplaçament cap enrere des de l'inici dels documents Wordpad. 
* En mode de navegació, prémer retorn en el botó de càrrega de fitxers ara presenta de forma correcta el diàleg per a seleccionar un fitxer per a pujar en lloc de commutar a mode de focus. (#1720)
* Els canvis de contingut dinàmic, com els que es donen en les consoles DOS, ja no s'anuncien si el mode de repòs per a aquesta aplicació està activat. (#1662)
* En el mode de navegació, s'ha millorat el comportament de ALT+FletxaAmunt i ALT + FletxaAvall per a expandir i contreure els quadres combinats. (#1630)
* NVDA ara es recupera de moltes més situacions, com ara en aquelles aplicacions que deixen de respondre. Això abans ocasionava que NVDA es congelés completament. (#1408)
* Per al Mozilla Gecko (Firefox etc) en documents en mode de navegació, NVDA ja no s'equivoca en representar text en situacions molt específiques, com ara quan un element té definit com a estil display:table. (#1373)
* NVDA ja no anuncia controls d'etiqueta quan el focus es mou dins d'ells. S'han aturat també els anuncis dobles d'etiquetes per alguns camps de formulari en    Firefox (Gecko) i Internet Explorer (MSHTML). (#1650)
* NVDA ja no falla en llegir una cel·la al Microsoft Excel després d'enganxar quelcom en ella amb control+v. (#1781)
* A l'Adobe Reader ja no s'anuncia informació estranya sobre el document quan hom es mou cap a un control en una altra pàgina en mode de focus.   (#1659)
* En mode de navegació en aplicacions Mozilla Gecko (e.g. Firefox), ara es detecten i s'informen correctament els botons d'alternar. (#1757)
* NVDA pot ara llegir correctament la barra d'adreces de Windows Explorer en la vista prèvia del desenvolupador de Windows 8.
* NVDA ja no bloqueja aplicacions com Winver i Wordpad en la vista prèvia del desenvolupador de Windows 8, a causa de les males transliteracions de glifs.   
* En mode de navegació, en aplicacions que fan servir Mozilla Gecko 10 i posterior (per exemple, Firefox 10) el cursor és posiciona més sovint de forma correcta quan es carrega una pàgina amb un ancoratge de destinació. (#360)
* En mode de navegació en aplicacions Mozilla Gecko (e.g. Firefox), ara es representen les etiquetes per mapes d'imatges.
* Amb el seguiment del ratolí activat, moure el ratolí sobre certs camps editables (com ara  Synaptics Pointing Device Settings i SpeechLab SpeakText) ja no fa que l'aplicació es bloquegi. (#672)
* NVDA funciona ara  correctament en diversos quadres de diàleg d'aplicacions distribuïdes amb Windows XP, incloent el diàleg Quant a la Llibreta en la Llibreta de notes. (#1853, #1855)
* Corregida la revisió per paraula en els controls d'edició de Windows. (#1877)
* Sortir d'un camp de text editable amb FletxaEsquerra, FletxaAmunt o RePag en mode de focus, ara canvia correctament a mode de navegació quan està activat el mode de focus automàtic per al moviment del signe d'intercalació. (#1733)

== Canvis per desenvolupadors ==
* NVDA  pot ara ensenyar els sintetitzadors de veu a canviar d'idioma per a determinades seccions de parla.  
* Per suportar això els controladors han de manegar Speech.LangChangeCommand en seqüències, passat a SynthDriver.speak().
* Els objectes SynthDriver haurien de proporcionar també l'argument d'idioma als objectes VoiceInfo (o anul·lar l'atribut d'idioma per a recuperar l'idioma actiu). En cas contrari es farà servir l'idioma de la interfície NVDA.

= 2011.2 =
Aspectes destacats d'aquesta versió inclouen millores que tenen a veure amb la puntuació i els símbols, incloent nivells configurables, etiquetatge personalitzat i descripcions de caràcters, absència de pauses al final de la línia durant el Verbalitza-ho tot; suport millorat per ARIA a Internet Explorer; Explorer; millor suport per a documents PDF / LiveCycle XFA en l'Adobe Reader; accés al text escrit en la pantalla en més aplicacions; i accés a la informació de format i color per al text escrit en la pantalla.  

== Noves característiques ==
* Ara és possible escoltar la descripció per a un determinat caràcter tot prement dues vegades en ràpida successió el script de revisió del caràcter actiu. Per a caràcters en anglès s'usa l'alfabet fonètic anglès estàndard. Per llenguatges pictogràfics, com el Xinès tradicional, es proporcionen una o més frases que facin servir el símbol donat. També prement la revisió de la paraula activa o prement la revisió de la línia activa 3 vegades es lletrejarà la paraula/línia usant la primera d'aquestes descripcions.
* Es pot veure més text en revisió plana en aplicacions com el Mozilla Thunderbird, les quals escriuen el seu text directament en la pantalla en forma de glifs
* Ara és possible escollir entre diversos nivells de puntuació i d'anunci de símbols. (#332)
* Quan la puntuació o d'altres símbols es repeteixen més de 4 vegades, el nombre de repeticions ara s'anuncia enlloc de llegir els símbols repetidament. (#43)
* Noves taules de traducció braille: Noruec 8 punts ordinador braille, Etíop grau 1, Eslové grau 1, Serbi grau 1. (#1456)
* Quan es fa servir el comandament Verbalitza-ho tot, la parla ja no es pausa de forma no natural al final de cada línia.  (#149)
* Si alguna cosa s'ordena en els navegadors web (d'acord amb la propietat aria-sort) ara NVDA ho anuncia.(#1505)
* Els models Braille Unicode es mostren ara correctament en Braille. (#1505)
* A Internet Explorer i en altres controls MSHTML quan es mou el focus dins d'un grup de controls (envoltat per un grup de camps), NVDA anunciarà ara el nom del grup (la llegenda). (#535)
* A Internet Explorer i en altres controls MSHTML, les propietats aria-labelledBy i aria-describedB apareixen ara representades.
* A Internet Explorer i en altres controls MSHTML s'ha millorat el suport per a la llista ARIA, per cuadrícules i per controls lliscants i de barra de progrés.
* Els usuaris poden ara canviar la pronúncia de la puntuació i d'altres símbols, així com el nivell del símbol en el qual són llegits. (#271, #1516)
* Al Microsoft Excel, ara s'informa del nom de la fulla activa quan es canvien fulls amb Control+RePag o Control+AvPag. (#760)
* Quan es navega una taula en el Microsoft Word amb la tecla Tab, NVDA ara anunciarà la cel·la activa quan hom es mogui (#159)
* Ara es pot configurar si s'informa de les coordenades de les cel·les d'una taula des del quadre de diàleg Formatació de documents.(#719)
* NVDA pot ara detectar el color i el format del text escrit a la pantalla
* En la llista de missatges d' Outlook Express/Windows Mail/Windows Live, NVDA ara anunciarà el fet que un missatge no s'ha llegit i també si es troba expandit o no en el cas de fils de conversa. #868)
* eSpeak té ara una configuració del percentatge de velocitat que triplica la velocitat de la veu
* Afegit suport per controlar el calendari que es troba en el quadre de diàleg que dóna informació de data i hora, i que és accessible des del rellotge de Windows 7.
* S'han afegit noves associacions de tecles per la línia Braille MDV Lilli.(#241)
* Nous idiomes: Búlgar, Albanès. 

== Canvis ==
* Per a canviar el cursor a cursor de revisió, ara es prem dues vegades en ràpida successió desplaçar el focus cap al script objecte de navegació (en teclat d'escriptori NVDA+Maj+TeclNúmMenys, en teclat de portàtil NVDA+Maj+Retrocès. Això allibera més tecles en el teclat.  #837)
* Per escoltar la representació decimal i hexadecimal d'un caràcter que estigui sota el cursor de revisió, premeu ara la revisió del caràcter actiu tres vegades i no dos, ja que prémer dues vegades implica llegir la descripció del caràcter.  
* S'ha actualitzat el sintetitzador de veu eSpeak a la versió 1.45.03. (#1465)
* El disseny de les taules ja no s'anuncia en aplicacions Mozilla Gecko quan s'està movent el i s'està en mode de focus o fora del document. 
* A Internet Explorer i altres controls MSHTML, el mode de navegació funciona ara per documents que estiguin dins d'aplicacions ARIA. (#1452)
* El traductor liblouis braille s'ha actualitzat a la versió 2.3.0.
* Quan s'està en mode de navegació i se salta cap a un control amb focus o QuickNav, s'anuncia la descripció del control, si és que en te una. 
* Ara s'anuncien les barres de progrés en mode de navegació.
* Els nodes marcats amb un rol de presentació ARIA a Internet Explorer i altres controls MSHTML s'ignoren ara en revisió simple i en ascendència de focus.
* La interfície d'usuari NVDA i la documentació es refereixen ara a les memòries intermèdies virtuals com a mode de navegació, ja que el terme "memòria intermèdia virtual" és poc significatiu per a molts usuaris.(#1509)
* Quan l'usuari desitja copiar la seva configuració d'usuari al perfil del sistema per a l'ús en l'inici de sessió, i la seva configuració conté connectors personalitzats, ara se l'avisa que això podria ser un risc de seguretat. (#1426)
* El servei NVDA ja no inicia i atura NVDA en els escriptoris d'entrada de l'usuari.
* En Windows XP i Windows Vista, NVDA ja no fa us de UI Automation fins i tot si és accessible via la actualització de la plataforma. Encara que l'ús de    UI Automation pot millorar l'accessibilitat en algunes aplicacions modernes  que corren en XP i Vista, hi hauria massa congelacions, bloquejos i accidents i es perdria rendiment durant el seu ús.(#1437)
* En aplicacions que fan servir Mozilla Gecko 2 i posteriors (com Firefox 4 i posteriors), es pot llegir ara un document en mode de navegació encara que no hagi finalitzat totalment la seva càrrega.  
* NVDA anuncia ara l'estat d'un contenidor quan el focus es mou cap a un controlador que hi hagi dins (per exemple, si el focus es mou dins d'un document que encara s'està carregant, s'informarà que està ocupat).
* La interfície i documentació de NVDA ja no fa servir els termes "primer fill" i "pare" en relació a la navegació d'objectes, ja que aquests termes són confusos per a molts usuaris.
* El tancament ja no s'informa per alguns menús que tenen submenús.  
* El script reportCurrentFormatting (NVDA+f) ara informa del format en la posició del cursor de revisió més que en el cursor de sistema / focus. Com, per defecte, el cursor de revisió segueix el cursor, molta gent no hauria de notar la diferència. Tanmateix, això permet que el usuari s'assabenti del format quan mou el cursor de revisió, com en una revisió plana.

== Correccions d'errors ==
* El tancament dels quadres combinats en documents en mode de navegació quan el mode de focus ha estat forçat amb NVDA+espai ja no fa retornar de nou al mode de navegació.(#1386)
* En documents Gecko (per exemple Firefox) i MSHTML (per exemple, Internet Explorer), NVDA ara presenta correctament alguns textos que estan en la mateixa línia però que abans eren presentats en línies separades. (#1378)
* Quan Braille està vinculat a revisar i l'objecte de navegació es mou cap a un document en mode de navegació, ja sigui manualment o a causa d'un canvi de focus, el Braille mostrarà de forma apropiada el contingut en mode navegació.  (#1406, #1407)
* Quan està desactivat que s'informi de la puntuació, ja no s'informa de certa puntuació de forma incorrecta quan es fan servir alguns sintetitzadors. (#332)
* Ja no hi ha problemes quan es carrega la configuració per a sintetitzadors que no suporten els paràmetres de veu, com ara Audiologic Tts3. (#1347)
* Ara es llegeix de forma correcta el menú d'extres de l'Skype. (#648)
* L'activació del l'opció "La brillantor controla el volum de l'àudio" dins del quadre de diàleg Paràmetres del ratolí, ja no hauria d'ocasionar un retard important dels xiulets quan es mou el ratolí per la pantalla de Windows Vista/ Windows 7 amb Aero activat.  (#1183)
* Quan NVDA està configurat per usar la distribució de teclat d'ordinador portàtil, NVDA+Supr ara treballa per documentar les dimensions de l'objecte de navegació actiu.(#1498)
* NVDA ara representa de forma apropiada l'atribut aria-selected en documents Internet Explorer.
* Quan NVDA canvia de forma automàtica a mode de focus en documents que estan en mode navegació, ara es dóna informació sobre el context del focus. Per exemple, si un element del quadre de llista rep el focus, s'anuncia primer el quadre de llista. (#1491)
* A Internet Explorer i altres controls MSHTML, els quadres de llista ARIA es tracten ara com a llistes, en lloc de com a elements de la llista 
* Quan un control de text editable de només lectura rep el focus, NVDA ara informa que es de només lectura. (#1436)
* En mode de navegació, NVDA ara es comporta correctament en relació amb els camps de text editables de només lectura. 
* En documents en mode de navegació, NVDA ja no canvia de forma incorrecta a mode de focus quan està configurat aria-activedescendant; per exemple quan la llista de completar apareix en alguns controls d'autocompletar.  
* En l'Adobe Reader, ara s'informa del nom dels controls quan es desplaça el focus o bé quan es fa servir la navegació ràpida en el mode d'exploració. 
* En els documents XFA PDF, en l'Adobe Reader, ara es mostren correctament els botons, enllaços i gràfics.
* En els documents XFA PDF, en l'Adobe Reader, tots els elements es mostren ara en línies separades. Aquest canvi es va fer perquè grans seccions (de vegades fins i tot tot el document) eren representades sense salts, a causa de la falta d'estructura generalitzada d'aquests documents.   
* Corregits problemes que s'esdevenien quan es movia el focus cap/més enllà  de camps de text editable en documents XFA PDF en l'Adobe Reader.  
* En els documents XFA PDF, en l'Adobe Reader, ara s'anuncien els canvis en el valor d'un quadre combinat enfocat.
* Els quadres combinats dissenyats per l'usuari, com els que es fan per triar colors en Outlook Express, són ara accessibles amb NVDA.(#1340)
* En llenguatges que usen un espai com a separador en grups de dígits o en milers, com ara alemany i francès, els números que es troben en trossos separats de text ja no es pronuncien com un únic nombre. Això era especialment problemàtic en les cel·les de taules que contenien nombres. (#555)
* Els nodes que tenen un rol de descripció ARIA, en Internet Explorer i en altres controls MSHTML, ara apareixen classificats com a text estàtic i no com a camps editables.  
* S'han solucionat diversos problemes que s'esdevenien quan es polsava tabulador mentre el focus estava en un document en mode de navegació (per exemple el tabulador enviava de forma inapropiada cap a la barra d'adreces a Internet Explorer). (#720, #1367)
* En entrar a les llistes mentre es llegeix text, ara NVDA diu, per exemple, "llista amb 5 ítems" enlloc de "llista amb 5 ítems"  1515)
* En mode d'ajuda d'entrada els gestos es registren fins i tot si els seus scripts eviten l'ajuda d'entrada, com en el cas dels comandaments endavant i enrera del desplaçament de la línia Braille.
* En el mode d'ajuda d'entrada, quan un modificador es manté premut en el teclat, NVDA ja no informa del modificador com si estigués modificant a ell mateix; per exemple NVDA+NVDA.
* En els documents l'Adobe Reader, ja funciona el prémer c o Maj+c per navegar cap a un quadre combinat.  
* L'estat seleccionat de les files seleccionables d'una taula s'informa ara de la mateixa manera que es fa per als elements de llista i de vista d'arbre.
* Els controls en Firefox i d'altres aplicacions Gecko poden ara activar-se mentre s'està en mode navegació, fins i tot si el seu contingut ha estat fluctuant fora de la pantalla. #801)
* Ja no es pot mostrar un quadre de diàleg de configuració de NVDA mentre s'està mostrant un missatge de diàleg, donat que el quadre de diàleg de configuració es congelava en aquest cas. (#1451)
* En el Microsoft Excel, ja no hi ha retard mentre les tecles per a seleccionar cel·les o bé moure's entre cel·les es mantenen premudes o bé es premen ràpidament de forma successiva.  
* S'han corregit les aturades intermitents del servei NVDA, fet que implicava que NVDA aturava la seva execució en pantalles segures de Windows.  - S'han corregit problemes que s'esdevenien de vegades amb línies Braille quan un canvi originava que text que s'estava mostrant desaparegués.(#1377)
* Ara NVDA permet llegir i navegar per la finestra de baixades de Internet Explorer 9 (#1280)
* Ja no és possible iniciar de forma accidental diferents còpies de NVDA a l'hora.   (#507)
* En sistemes lents, NVDA ja no origina que la seva finestra principal es mostri de forma inapropiada tot el temps que NVDA estigui executant-se. (#726)
* NVDA ja no s'atura en Windows XP quan s'inicia una aplicació WPF. (#1437)
* Verbalitza-ho tot i Verbalitza-ho tot amb revisió ara poden funcionar amb controls de text de   UI automation que suporten totes les funcionalitats requerides. Per exemple, pots usar ara Verbalitza-ho tot amb revisió sobre documents en XPS Viewer.
* NVDA ja no classifica de forma inapropiada alguns elements de llista com si fossin caselles en les normes de missatge del quadre de diàleg Apply Now, en Outlook Express / Windows Live Mail. (#576)
* Ja no s'informa dels quadres combinats com si tinguessin un submenú. 
* NVDA ja pot llegir els receptors en els camps De, CC i BCC del Microsoft Outlook. (#421)
* Corregit un problema pel qual en el quadre de diàleg Paràmetres de Veu de NVDA no s'informava de les modificacions en les barres de desplaçament quan es feien canvis. (#1411)
* NVDA ja no s'equivoca en anunciar una nova cel·la quan es mou en un full de càlcul Excel, després de tallar i enganxar. (#1567)
* NVDA ja no va empitjorant en endevinar els noms dels colors, com més colors anuncia.  
* En Internet Explorer i d'altres controls MSHTML, s'ha corregit la incapacitat de llegir pàgines estranyes que continguin iframes marcats amb un rol de presentació ARIA. (#1569)
* En Internet Explorer i d'altres controls MSHTML, s'ha corregit un problema estrany en el que el focus, quan s'estava en mode de focus, es mantenia rebotant infinitament entre el document i un camp de text multilínia editable.(#1566)
* En el Microsoft Word 2010 NVDA llegirà ara automàticament els diàlegs de confirmació. (#1538)
* En camps de text editable multilínia en Internet Explorer i d'altres controls MSHTML, la selecció de línies després de la primera s'informa ara de forma correcta. #1590)
* S'ha millorat el desplaçament per paraula en molts casos, incloent el mode de navegació i els controls d'edició de Windows. (#1580)
* L'instal·lador NVDA ja no mostra text il·legible en les versions per Hong Kong de Windows Vista i Windows 7.   (#1596)
* NVDA ja no falla en carregar la versió 5 del sintetitzador del Microsoft Speech API, si la configuració conté paràmetres per aquest sintetitzador però li falla l'ajust de veu. (#1599)
* En camps de text editable multilínia en Internet Explorer i d'altres controls MSHTML, NVDA ja no s'alenteix o es congela quan està activat el Braille. 
* En mode de navegació en Firefox, NVDA ja no rebutja incloure contingut que estigui dins d'un node enfocable que tingui un rol de presentació ARIA.  
* Al Microsoft Word, amb Braille activat, ara es llegeixen correctament les línies de pàgines que van darrera la primera pàgina.   (#1603)
* Al Microsoft Word 2003, les línies de dreta a esquerra poden ser de nou llegides amb el Braille activat.(#627)
* Al Microsoft Word, Verbalitza-ho tot funciona ara correctament quan el document no acaba amb un final de frase.
* Quan s'obre un missatge en text pla en Windows Live Mail 2011, NVDA ubicarà correctament el focus en el missatge del document,  permetent que aquest sigui llegit. 
* NVDA ja no es congela temporalment o bé refusa parlar en els diàlegs Moure/Copiar  de Windows Live Mail. (#574)
* En Outlook 2010, NVDA monitoritzarà ara correctament el focus en la llista de missatges. (#1285)
* S'han resolt alguns problemes de connexió USB amb la línia Braille Lilli. (#241)
* En Internet Explorer i altres controls MSHTML, ja no s'ignoren els espais en mode de navegació en alguns casos (per exemple, darrera un enllaç)  
* En Internet Explorer i altres controls MSHTML, s'han eliminat alguns salts de línia estranys en el mode de navegació Concretament, en els elements HTML que no tenen definit cap estil de visualització, ja no es força un salt de línia. (#1685)
* Si NVDA és incapaç d'inicialitzar-se, la incapacitat de reproduir el so crític d'aturada de Windows ja no amaga el missatge crític d'error en el fitxer de registres.

== Canvis per desenvolupadors ==
* La documentació del desenvolupador pot ser ara generada usant SCons. Vegeu readme.txt a l'arrel de la distribució de codi font per detalls, incloent les dependències associades.
* Els locals poden ara proporcionar descripcions per caràcters. Per detalls vegeu la secció Descripció de Caràcters a la Guia del Desenvolupador. (#55)
* Els desenvolupadors locals poden ara proporcionar informació sobre la pronúncia de puntuació específica i d'altres símbols. Per detalls, vegeu la secció Pronúncia de Símbols en la Guia del desenvolupador. (#332)
* Ara es pot construir NVDAHelper amb diverses opcions de depuració utilitzant la variable NVDA Helper DebugFlags SCons. Veure readme.txt en l'arrel de la distribució de codi font per a més detalls. (#1390)
* El controladors Synth s'han passat a una seqüència de text i a comandaments de veu per parlar en lloc de només text i d'un índex.
* Això permet índex incrustats, canvis de paràmetres, etc.
* Els controladors han d'implementar SynthDriver.speak() en lloc de SynthDriver.speakText() i SynthDriver.speakCharacter().
* Es faran servir els mètodes antics si SynthDriver.speak() no està implementat, però estan obsolets i seran eliminats en una futura versió.
* gui.execute() s'ha eliminat. En el seu lloc s'ha d'suar wx.CallAfter().
* gui.scriptUI s'ha eliminat.
* Per a diàlegs de missatge, useu wx.CallAfter(gui.messageBox, ...).
* Per tots els altres diàlegs, hauríeu d'usar diàlegs wx reals.
* Una nova funció gui.runScriptModalDialog() simplifica l'ús de diàlegs modals a partir de scripts.
* Els controladors Synth ara poden suportar paràmetres booleans. Vegeu SynthDriverHandler.BooleanSynthSetting.
* SCons accepta ara una variable certTimestampServer tot especificant la URL d'un servidor de marcat de temps per a usar-lo per a marcar el temps en signatures Authenticode. (#1644)

= 2011.1.1 =
Aquesta versió corregeix alguns problemes importants, especialment de seguretat, trobats a  NVDA 2011.1.

== Correccions d'errors ==
* L'ítem Fes una donació al menú NVDA apareix ara desactivat quan s'executa l'inici de sessió, el tancament, UAC i d'altres pantalles segures de Windows, ja que és un risc de seguretat (#1419)
* Ara és impossible copiar o enganxar dins de la interfície d'usuari NVDA mentre s'està en escriptoris segurs (tancament de pantalla, pantalla UAC i inici de sessió de Windows) ja que es tracta d'un risc de seguretat.(#1421)
* A Firefox 4, el comandament per a canviar a la memòria virtual intermèdia continent   (NVDA+control+espai) ara funciona com si haguéssim de sortir d'objectes incrustats, com ara contingut Flaix. (#1429)
* Quan la parla de les tecles de comandament està activada, els caràcters en majúscules ja no es llegeixen incorrectament, com si fossin tecles de comandament. (#1422)
* Quan la parla de tecles de comandament està activada, prémer espai amb  modificadors diferents de Maj (com Control i Alt) s'anuncia ara com una tecla de comandament.  (#1424)
* El registre està ara completament desactivat quan s'executen l'inici i el tancament de sessió, l'UAC i d'altres pantalles segures de Windows. (#1435)
* En el mode d'ajuda d'entrada, els gestos s'inicien fins i tot si no es troben lligats a un script (d'acord amb la guia de l'usuari) (#1425)

= 2011.1 =
Aspectes destacats d'aquesta versió inclouen l'informe automàtic de nous textos en mIRC,  PuTTY, Tera Term and SecureCRT; suport per a connectors globals; anunci de vinyetes i numeració en el icrosoft Word; associacions de tecles addicionals per a línies Braille,  incloent tecles per a moure's cap a les tecles anterior i posterior; suport per a diverses línies HumanWare i APH Braille; i informació de colors per alguns controls, incloent controls de text per  IBM Lotus Symphony.

== Noves característiques ==
* Es poden anunciar ara colors per a alguns controls. L'anunci automàtic pot ser configurat en el quadre de diàleg Formatació de documents. Pot ser també informat sota demanda usant el comandament de format de text (NVDA+f)
* Inicialment això està recolzat en els controls de text editable de l'estàndard IAccessible 2 (com en les aplicacions Mozilla), en controls RichEdit (com en el WordPad) i en controls de text IBM Lotus Symphony.
* En memòries intermèdies virtuals ara es pot seleccionar per pàgina (usant Maj+ AvPag i Maj+RePàg) i per paràgraf (fent servir Maj+Control+FletxaAvall i Maj+Control+FletxaAmunt) (#639)
* NVDA ara informa automàticament de noves línies de text en mIRC, PuTTY, Tera Term i  SecureCRT. (#936)
* Els usuaris poden ara afegir noves associacions de tecles o anul·lar les existents per qualsevol dels scripts existents en NVDA, tot proporcionant a cada usuari individual un mapa de gestos d'entrada. (#194)
* Suport per a connectors globals. Els connectors globals poden afegir noves funcionalitats a NVDA que funcionen en totes les aplicacions.  
* Ara se sent un petit bip quan es teclegen caràcters amb la tecla Maj mentre està activada la tecla Bloq Maj. Això es pot desactivar eliminant la selecció d'aquesta nova opció en el quadre de diàleg Paràmetres del teclat. (#663)
* Els salts de pàgina s'anuncien ara quan hom s'està movent línia per línia en el Microsoft Word. (#758)
* Les vinyetes i els nombres s'anuncien ara quan hom s'està movent línia per línia en el Microsoft Word  (#208)  
* Està disponible un comandament per a commutar a mode de Repós en una determinada aplicació activa (NVDA+Maj+s). El mode de Repós (prèviament conegut com a mode d'autoveu) desactiva totes les funcionalitats de lectura de NVDA per una aplicació en particular. Es molt útil per aplicacions que proporcionen la seva pròpia parla i/o les seves característiques de lectura de pantalla. Prem de nou aquest comandament per a desactivar el mode de Repós.
* S'han afegit algunes associacions addicionals de tecles Braille. Vegeu la secció Dispositius Braille Suportats en la Guia de l'Usuari per a més detalls. (#209)
* Per la comoditat dels desenvolupadors aliens, es poden ara recarregar els mòduls d'app així com els connectors globals sense necessitat de reiniciar NVDA. Useu Eines  Torna a carregar els connectors en el menú NVDA o NVDA+Control+F3 . (#544)
* NVDA recorda ara la posició en la que s'estava quan es retorna a una pàgina web que hagi estat visitada abans. Això es dóna fins que se surt del navegador o de NVDA (#132)
* Les línies Braille Handy Tech poden ara usar-se sense instal·lar el controlador universal Handy Tech.  (#854)
* Afegit suport per diverses línies Braille Baum, HumanWare and APH. (#937)
* Ara es reconeix la barra d'estat en Media Player Classic Home Cinema.
* La línia Braille Freedom Scientific Focus 40 Blue es pot fer servir ara quan s'inicia una connexió via Bluetooth. (#1345)

== Canvis ==
* Ja no es reporta per defecte la informació de la posició en alguns casos on normalment era incorrecta, per exemple, en molts menús, en la barra d'aplicacions actives, en l'Àrea de Notificació, etc... Tanmateix, es pot activar com una opció addicional en el quadre de diàleg Presentació d'objectes. 
* L'ajuda del teclat ha estat renombrada com "ajuda d'entrada", per tal que reflecteixi que es maneguen entrades que s'entren des de fonts diferents al teclat.
* L'ajuda d'entrada ja no informa de la localització d'un codi de script via parla i Braille donat que això és críptic i irrellevant per a l'usuari. Tanmateix, es registra per a desenvolupadors i usuaris avançats.
* Quan NVDA detecta que s'ha congelat intercepta les claus modificadores NVDA fins i tot encara que passi totes les altres tecles al sistema. Això impedeix que el usuari commuti Bloq Maj, etc., si prem una tecla modificadora NVDA sense adonar-se que NVDA s'ha congelat. 
* Si les tecles es mantenen premudes després de fer servir el comandament per passar a la propera tecla, totes les tecles (incloent les repeticions de tecles) s'ignoren fins que s'allibera la darrera tecla.  
* Si una tecla modificadora NVDA es prem dues vegades i la segona vegada que es prem es deixa premuda s'ignorarà, i també s'ignoraran totes les repeticions de tecles.
* Les tecles de volum amunt, volum avall i silenci apareixen ara reportades en l'ajuda d'entrada. Això pot ser útil si l'usuari no té clar de per a què serveixen aquestes tecles.  
* La tecla d'accés directe per al cursor de revisió en el menú de preferències NVDA ha canviat de r a c per tal d'eliminar el conflicte amb l´ítem Paràmetres del Braille. 

### Correccions d'errors

* Quan s'afegeix una nova entrada de veu al diccionari, el títol del diàleg és ara "Afegeix entrada de diccionari" enlloc de "Edita entrada de diccionari" (#924)
* En els quadres de diàleg dels diccionaris de veu, el contingut de les columnes Expressió regular i Distingeix Majúscules i minúscules, es presenta ara en el llenguatge configurat en NVDA enlloc de aparèixer sempre en anglès. 
* A AIM, la informació de posició es dona ara en vistes d'arbre.  
* En els controls lliscants en el quadre de diàleg Paràmetres de Veu,   la fletxa amunt/pàgina amunt/inici ara incrementa la configuració i la fletxa avall / pàgina avall / Fi, la disminueix. Abans s'esdevenia just el contrari, fet que no era lògic  i era inconsistent amb l'anell de configuracions del sintetitzador.   (#221)
* En les memòries intermèdies virtuals, amb el disseny de pantalla desactivat, ja no apareixen estranyes línies en blanc.  
* Si la tecla modificadora NVDA es prem dues vegades ràpidament però hi ha premuda una tecla intervinent, la tecla modificadora NVDA ja no es té en compte en la segona premuda.
* Les tecles de puntuació s'anuncien en l'ajuda d'entrada, fins i tot quan la parla de la puntuació està desactivada.  (#977)
* En el quadre de diàleg Paràmetres de teclat, els noms de les diferents disposicions de teclat es presenten ara en el llenguatge en què NVDA està configurat enlloc d'aparèixer sempre en anglès. (#558)
* Corregit un problema segons el qual alguns ítems es presentaven com a buits en documents l'Adobe Reader, per exemple els enllaços en la taula de continguts de la Guia de l'Usuari del  Apple iPhone IOS 4.1.
* El botó "Utilitza els paràmetres desats a la pantalla d'inici de sessió i a altres pantalles de seguretat", ubicat en el quadre de diàleg Paràmetres Generals funciona ara si es fa servir de forma immediata a una nova instal·lació de NVDA però abans que aparegui una pantalla segura. Abans, NVDA informava que la còpia s'havia realitzat correctament però no tenia cap efecte.  (#1194)
* Ja no és possible tenir dos quadres de diàleg NVDA oberts de forma simultània. Això soluciona un problema segons el qual un diàleg depèn d'un altre diàleg obert; per exemple, quan es canvia el sintetitzador mentre es manté obert el quadre de diàleg Paràmetres de veu.  (#603)
* En sistemes amb UAC activat, el botó "Utilitza els paràmetres desats a la pantalla d'inici de sessió i a altres pantalles de seguretat", ubicat en el quadre de diàleg Paràmetres Generals, ja no falla després de la UAC si el compte de l'usuari conté un espai.   (#918)
* En Internet Explorer i en altres controls MSHTML controls, NVDA usa ara la URL com a darrer recurs per a determinar el nom d'un enllaç en lloc de presentar enllaços buits. (#633)
* NVDA ja no ignora el focus en els menús d' AOL Instant Messenger (#655)
* S'anuncia l'etiqueta correcta per errors corrector ortogràfic del Microsoft Word  (per exemple, "No al diccionari", "Error gramatical", puntuació). Amb anterioritat tots s'anunciaven com error de gramàtica. (#883)
* Teclejar en el Microsoft Word mentre s'està fent servir una línia Braille no hauria de causar ja text il·legible per teclejar. També s'ha solucionat una congelació estranya quan es premia una tecla d'enrutament Braille en els documents Word. (#1212). Tanmateix, una limitació és que el text aràbic ja no pot ser llegit en Word 2003 i posteriors mentre s'està usant un dispositiu Braille. 
* Quan es prem la tecla esborrar en un camp editable el text/cursor d'un dispositiu Braille s'actualitza ara correctament per a reflectir el canvi. (#947)
* Els canvis en pàgines dinàmiques de documents Gecko2 (per exemple, Firefox 4) mentre hi ha obertes múltiples pestanyes, són ara acuradament reflectits per NVDA. Anteriorment només es reflectien els canvis en la primera pestanya. (Error Mozilla 610985)
* NVDA pot ara anunciar adequadament els suggeriments per a errors en gramàtica i puntuació en el quadre de diàleg de correcció ortogràfica del Microsoft Word   (#704)
* En Internet Explorer i altres controls MSHTML, NVDA ja no presenta els ancoratges de destí com a enllaços buits en la seva memòria intermèdia virtual. En lloc d'això aquests ancoratges apareixen ocults, com hauria de ser (#1326)
* La navegació d'objectes al voltant / dins de finestres de llistes estàndards ja no apareix trencada i asimètrica. 
* A Firefox i en altres controls basats en Gecko, NVDA ja no s'atura en un submarc si aquest acaba de carregar-se abans que la resta del document.  
* NVDA anuncia ara de forma adequada el següent caràcter quan s'esborra un caràcter amb TeclatNúmSuprimir. (#286)
* En la pantalla d'inici de Windows XP, el nom de l'usuari es llegeix de nou quan es canvia l'usuari seleccionat.
* Corregits els problemes que hi havia en llegir text en consoles de comandament Windows quan estava habilitat Informa dels números de línia.
* El quadre de diàleg Llista d'elements per a memòries intermèdies virtuals pot ser ara utilitzat per usuaris amb visió. Tots els controls es poden veure a la pantalla.  (#1321)
* La llista d'entrades al quadre de diàleg Diccionari de veus és ara més llegible per als usuaris amb visió. La llista es prou ampla ara com per mostrar totes les columnes a la pantalla. (#90)
* En línies Braille ALVA BC640/BC680, NVDA ara ja fa cas de les tecles de pantalla que encara estan premudes després que s'hagi alliberat una altra tecla.
* l'Adobe Reader X ja no es bloqueja després de sortir de les opcions de document no etiquetat i abans que aparegui el diàleg de processament   (#1218)
* NVDA ara canvia al controlador de dispositiu Braille adequat quan es torna a la configuració guardada. (#1346)
* Es llegeix de nou correctament l'assistent de projectes de Visual Studio 2008. (#974)
* NVDA ja no deixa de funcionar completament en aplicacions que continguin caràcters no ASCII en el seu nom no executable. (#1352)
* Quan es llegeix per línia en AkelPad amb l'ajust de paraula activat, NVDA ja no llegeix el primer caràcter de la següent línia en finalitzar la línia activa.
* En l'editor de codi de Visual Studio 2005/2008 NVDA ja no llegeix el text sencer darrera cadascun dels caràcters teclejats  (#975)
* Corregit l'error on alguns dispositius Braille no es tancaven correctament quan se sortia de NVDA o bé quan es canviava el dispositiu. 
* El focus inicial ja no s'anuncia dues vegades quan s'inicia NVDA d (#1359)

== Canvis per desenvolupadors ==
* SCons es fa servir ara per preparar l'arbre font i crear construccions binàries, arxius portables, instal·ladors, etc... Vegeu  readme.txt  a l'arrel de la distribució font per detalls. 
* Els noms de tecla usats per NVDA (incloent els mapes de tecla) s'han fet més amigables/lògics; per exemple FletxaAmunt, enlloc de ExtèsAmunt i TeclNumAvPag enlloc del que hi havia abans. Vegeu el mòdul vkCodes per obtenir una llista. 
* Totes les entrades de l'usuari es representen ara per una instància  inputCore.InputGesture. (#601)
* Cada font d'entrada de subclasse és abastada per la classe ase InputGesture class. ??
* Les pulsacions de tecles del teclat del sistema es troben abastades per la classe keyboardHandler.KeyboardInputGesture class.
* Les pulsacions de botons, rodes i altres controls sobre un dispositiu Braille es troben abastats per subclasses de la classe braille  BrailleDisplayGesture. Aquestes subclasses són proporcionades per cadascun dels controladors del dispositiu Braille.
* Els gestos d'entrada salten cap a ScriptableObjects usant el mètode ScriptableObject.bindGesture() o bé una instància o un dictat __gestures sobre la classe que mapeja identificadors gest als noms d'script. Per detalls vegeu baseObject.ScriptableObject.
* Els mòduls d'app ja no tenen fitxers de clau de mapa. Tots els gestos de associació han de ser fets en la mateixa aplicació del mòdul. 
* Tots els escrits ara tenen una instància InputGesture en lloc d'una pulsació de tecla.
* KeyboardInputGestures pot ser enviat al SO fent servir el mètode send() del gest 
* Per a enviar una pulsació arbitrària de tecla cal crear un KeyboardInputGesture tot fent servir KeyboardInputGesture.fromName() i després usant el mètode send().
* Els locals poden ara proporcionar un fitxer de mapa de gestos per tal d'afegir noves associacions o sobreescriure les associacions existents per scripts en qualsevol lloc de NVDA.  (#810)
* Els mapes de gestos locals haurien d'estar ubicats a locale\LANG\gestures.ini, sent LANG el codi del llenguatge.
* Per a detalls del format de fitxer, vegeu inputCore. 
* El nou LiveText i el Terminal NVDAObject behaviors faciliten reportar de forma automàtica nou text. Per a detalls, vegeu aquestes classes a NVDAObjects.behaviors. (#936)
* La classe de superposició NVDAObjects.windows.DisplayModelLiveText pot ser utilitzada per a objectes que han de recuperar text escrit a la pantalla.
* Vegeu els mòduls d'aplicació mIRC i Putty per exemples d'ús.
* Ja no hi ha un mòdul d'aplicació _default. Els mòduls d'aplicació haurien de tenir en el seu lloc la subclasse  appModuleHandler.AppModule (classe base AppModule).
* Afegit suport per connectors globals que poden associar globalment scripts, manegar events NVDAObject i triar les classes de superposició NVDAObject (#281). Per detalls, vegeu globalPluginHandler.GlobalPlugin.
* En objectes SynthDriver, els atributs disponibles* per configuració de cadenes (e.g. availableVoices i availableVariants)  són ara OrderedDicts teclejats per ID enlloc de llistes.
* El synthDriverHandler.VoiceInfo ara incorpora un argument opcional de llengua que especifica l'idioma de la veu. .
* Els objectes SynthDriver proporcionen ara un atribut d'idioma que especifica el llenguatge de la veu activa.  
* La implementació de la base fa servir el llenguatge especificat en els objectes  VoiceInfo objects a availableVoices. Això és convenient per la major part de sintetitzadors que suporten un llenguatge per veu.  
* Els controladors de dispositius Braille  s'han millorat per permetre botons, rodes i d'altres controls a ser associats a scripts NVDA.  
* Els controladors poden proporcionar una entrada global de mapes de gestos per afegir associacions per scripts en qualsevol lloc en NVDA.  
* Els controladors també poden proporcionar els seus propis scripts per millorar funcions específiques de visualització.  
* La propietat 'selfVoicing' en les classes AppModule ha estat renombrada com 'sleepMode'.
* El mòdul d'events d'aplicacions _appLoseFocus i  event_appGainFocus han estat ara renombrats  a  event_appModule_loseFocus i event_appModule_gainFocus, respectivament, amb la finalitat de fer la convenció de noms consistent en mòduls d'app i interceptors d'arbre.  
* Tots els controladors de dispositius Braille haurien ara de fer servir    braille.BrailleDisplayDriver enlloc de braille.BrailleDisplayDriverWithCursor.
* El cursor es gestiona ara fora del controlador
* Els controladors existents necessiten ara canviar la seva declaració de classe en conseqüència i renombrar el seu mètode _display per visualitzar.

## 2010.2

Notables característiques d'aquesta versió són: una navegació d'objectes considerablement simplificada; memòries intermèdies virtuals per al contingut l'Adobe Flash; accés a diversos controls que abans eren inaccessibles mitjançant la recuperació de text escrit a la pantalla; revisió plana del text de la pantalla; suport per documents IBM Lotus Symphony; informe dels encapçalaments de files i columnes en el Mozilla Firefox i, millores significatives en la documentació de l'usuari.

### Noves característiques

* La navegació pels objectes amb el cursor de revisió s'ha simplificat molt. El cursor de revisió ara exclou objectes que no són útils a l'usuari.; per exemple, objectes que només es fan servir amb finalitats de disseny i objectes no accessibles.
* En aplicacions que fan servir Java Access Bridge (encloent OpenOffice.org), ara s'informa del format en els controls de text.  (#358, #463)
* Quan es mogui el ratolí sobre les cel·les del Microsoft Excel, NVDA  ho anunciarà de forma adequada. 
* En aplicacions que fan servir Java Access Bridge, el text d'un quadre de diàleg s'anuncia quan apareix el quadre de diàleg.  (#554)
* Una memòria intermèdia virtual es pot fer servir quan es navega en continguts l'Adobe Flash Player. Ja es suporta la navegació d'objectes i la interacció directe amb els controls (tot activant el mode de focus). (#453)
* Els controls de text editable, encloent el l'editor de codi, són ara accessibles a Eclipse IDE. Es pot estar usant Eclipse 3.6 o posterior.  (#256, #641)
* NVDA pot ara recuperar la major part del text escrit a la pantalla. (#40, #643)
* Això permet la lectura de controls que no exposin la informació de forma més directa o fiable.  
* Els controls que s'han fet accessibles amb aquesta característica són : alguns ítems de menú que mostren icones (per exemple el menú "Obrir amb" de Xindows XP) (#151), camps de text editables en aplicacions Windows Live (#200), la llista d'errors a Outlook Express (#582), el control de text editable a TextPad (#605), les llistes a Eudora, molts controls a Australian E-tax i la barra de fórmules del Microsoft Excel
* Suport per a l'editor de codi al Microsoft Visual Studio 2005 i 2008. Com a mínim es requereix Visual Studio Standard; no funciona en les edicions Express. (#457)
* Suport per documents IBM Lotus Symphony.
* Suport experiment primerenc per a Google Chrome. Si us plau, prengueu nota que el lector de pantalla de Chrome és lluny de ser complet i cal fer encara feina addicional amb NVDA.  Caldrà que es disposi d'una compilació recent de Chrome per provar-ho. 
* L'estat de les tecles de commutació (Bloq Maj, Bloq Núm i Bloq Despl) es mostra ara en Braille quan es premen. (#620)
* Els Globus d'ajuda es mostren ara en Braille quan escau. (#652)
* S'ha afegit un controlador per la línia Braille MDV Lilli. (#241)
* Ara  s'anuncia la selecció d'una fila o columna sencera en el Microsoft Excel, amb les tecles de drecera Maj+Espai i Control+Espai, (#759)
* Ara s'anuncien els encapçalaments de files i columnes. Això es pot configurar des del quadre de diàleg Formatació de documents. 
* Això és suportat actualment per documents de aplicacions Mozilla, com Firefox (versió 3.6.11 i posteriors) i   Thunderbird (version 3.1.5 i posteriors). (#361)
* S'han introduït comandaments per revisions planes: (#58)
* NVDA+TeclNum7 commuta a revisió plana, tot col·locant el cursor de revisió a la posició de l'objecte principal, tot permetent la revisió de la pantalla (o d'un document si n'hi ha un) amb els comandaments de revisió de text.
* NVDA+TeclNum1 mou el cursor de revisió dins de l'objecte representat pel text a la posició del cursor de revisió, tot permetent la navegació per l'objecte a partir d'aquest punt.
* Els paràmetres actius de l'usuari NVDA poden ser copiats per a ser usats en pantalles segures de Windows, com les d'inici de sessió o UAC, tot prement un botó en el quadre de diàleg Paràmetres Generals.
* Suport per al Mozilla Firefox 4.
* Suport per al Microsoft Internet Explorer 9.

### Canvis

* S'han eliminat momentàniament els següents comandaments : el sayAll per a l'objecte de navegació (NVDA+TeclNumSuma; el objecte de navegació posterior en el flux (NVDA+Maj+TeclNúm6) i l'objecte de navegació anterior en el flux (NVDA+Maj+TeclNum4). L'eliminació dels comandament s'ha fet per eliminar errors i per alliberar les tecles per afegir altres possibles funcions. 
* En el quadre de diàleg Sintetitzador de NVDA, només es mostra el nom de visualització del sintetitzador. Abans apareixia prefixat el nom del controlador, el qual només és rellevant a nivell intern.  
* En aplicacions incrustades o en memòries intermèdies virtuals dins d'un altra memòria intermèdia virtual (per exemple, l'Adobe Flash) es pot ara prémer NVDA+Control+Espai per sortir de l'aplicació incrustada o de la memòria intermèdia virtual i anar cap el document contenidor. Abans es feia servir per això NVDA+espai. Ara NVDA+espai es fa servir només per commutar els modes de navegació i de focus a les memòries intermèdies virtuals.
* Si el visor de veu (activat amb el menú Eines) rep el focus (per exemple si es clica dins) el nou text no apareixerà en el control fins que el focus s'allunyi. Això permet la selecció de text amb major facilitat (per exemple, per copiar).
* El Visor de registre i la Consola Phyton es maximitzen quan estan activats.
* Quan el focus en un full de càlcul del Microsoft Excel o Similar afecta a més d'una cel·la, s'anuncia el rang de selecció i no només la cel·la activa. (#763)
* El guardat de la configuració i el canvi d'opcions sensibles ara està desactivat quan s'inicia sessió amb UAC i d'altres pantalles segures de Windows.
* El sintetitzador eSpeak s'ha actualitzat a la versió 1.44.03.
* Si NVDA està ja iniciat, l'activació de l'accés directe NVDA en l'escriptori (que inclou prémer Control+Alt+N) reiniciarà  NVDA.
* S'ha eliminat el text informatiu sota les caselles relatives al ratolí en el quadre de diàleg Opcions del ratolí i s'ha reemplaçat amb una casella Habilita el seguiment del ratolí que respon milló a la commutació del script del seguiment del ratolí
* S'ha actualitzat la distribució de teclat d'ordinador portàtil de forma que ja enclou tots els comandaments disponibles en l'escriptori i treballa correctament en teclats de configuració no anglesa.  (#798, #800)
* S'han fet millores i actualitzacions significatives en la documentació de l'usuari, tot encloent documentació sobre els comandament dels teclats d'ordinador portàtil i sobre la sincronització de la Guia de referència ràpida de comandaments de teclat amb la Guia de l'usuari (#455)
* El traductor Liblouis Braille s'ha actualitzat a la versió  2.1.1. Cal destacar que soluciona alguns problemes relacionats amb el Braille xines així com amb caràcters que es troben poc definits per la taula de transliteració. (#484, #499)

### Correccions d'errors

* A µTorrent, el ítem enfocat en la llista de torrents no apareix reportat de forma repetida ni tampoc roba el focus quan un menú està obert.  
* A µTorrent, ara s'informa dels noms dels fitxers en la llista de continguts Torrent.   
* En les aplicacions Mozilla, ara ja es detecta correctament el focus quan s'atura sobre una taula buida o un arbre.  
* En les aplicacions Mozilla ara el "no verificat" s'informa correctament en controls amb caselles com ara les cel·les d'una taula que tinguin caselles.   (#571)
* En les aplicacions Mozilla el text dels quadres de diàleg ARIA implementats correctament ja no s'ignoren i s'informen de forma correcta quan apareix el quadre de diàleg. . (#630)
* En Internet Explorer i altres controls MSHTML el atribut de nivell ARIA apareix ara representat correctament. 
* En Internet Explorer i altres controls MSHTML, el rol d'ARIA pot escollir-se per damunt d'altres tipus d'informació amb la finalitat de donar una experiència ARIA més correcta i predicible.  
* S'ha aturat un estrany accident a Internet Explorer quan es navega per marcs o iMarcs. 
* En documents del Microsoft Word es possible llegir de nou les línies de dreta a esquerra (com en el text àrab). (#627)
* S'ha reduït molt el retard quan es mostren grans quantitats de text en una consola de comandaments Windows en un sistema de 64 bits. (#622)
* Si l'Skype ja s'ha inicialitzat quan s'inicia NVDA ja no serà necessari reiniciar l'Skype per assegurar-ne l'accessibilitat. Això pot ser també vàlid per altres aplicacions que analitzen l'indicador de seguiment de lectura de pantalla.
* En aplicacions del Microsoft Office, NVDA ja no es penja quan està activada la parla en segon pla  (NVDA+b) o quan es navega per alguns objectes de la barra d'eines. (#616)
* S'ha corregit la pronuncia incorrecta de números que contenien un zero després d'un separador; per exemple 1.023. (#593)
* l'Adobe Acrobat Pro i Reader 9 ja no es pengen quan es tanca un fitxer o quan es fan algunes altres tasques. (#613)
* Ara s'anuncia la selecció quan es prem Control+a amb la finalitat de seleccionar tot el text en alguns controls de text editable, com ara en el Microsoft Word. (#761)
* En els controls Scintilla (per exemple en  Notepad++), el text ja no es selecciona de forma incorrecta quan NVDA mou el cursor, per exemple, durant un SayAll. (#746)
* Ara és de nou possible revissar els continguts de les cel·les en el Microsoft Excel amb el cursor de revisió. 
* NVDA pot de nou llegir per línia en alguns camps textArea problemàtics d'Internet Explorer 8. (#467)
* Windows Live Messenger 2009 ja no es tanca immediatament si s'inicia sessió mentre NVDA s'està executant.  (#677)
* En navegadors web ja no cal prémer TAB per a interactuar amb un objecte incrustat (com els continguts Flaix) un cop premut retorn en l'objecte incrustat o bé quan es retorna cap aquest des d'una altra aplicació.  (#775)
-En controls Scintilla (e.g. Notepad++), l'inici de les línies llargues ja no apareix truncat quan questes marxen ora de la pantalla. A més, aquestes línies llargues es mostraran correctament en Braille quan se seleccionin.
* A Loudtalks, ja és possible accedir a la llista de contactes.
* La URL dels documents i  "MSAAHTML Registered Handler" ja no s'informen falsament a Internet Explorer i en altres controls MSHTML. (#811)
* En les vistes d'arbre de Eclipse IDE, l´´item prèviament enfocat ja no s'anuncia incorrectament quan el focus es mou cap un nou ítem.  
* NVDA funciona ara correctament en un sistema on el directori de treball actual hagi estat esborrat del camí de cerca DLL (mitjançant la configuració de l'entrada de registre CWDIllegalInDllSearch a 0xFFFFFFFF). Cal destacar que això no és rellevant a la major part dels usuaris. 
* Quan els comandaments de navegació de les taules es fan servir fora d'una taula en el Microsoft Word, ja no es diu "vora de la taula" després de "no taula" . (#921)
* Quan els comandaments de navegació de les taules. no es poden moure a causa que s'està en el límit d'una taula al Microsoft Word, "límit de la taula" ja no es diu en anglès sinó en el llenguatge en que NVDA està configurat.  (#921)
* A Outlook Express, Windows Mail and Windows Live Mail, ja s'informa de l'estat de les caselles de verificació en les llistes de normes dels missatges.(#576)
* La descripció de les normes de missatge ara es pot llegir a   Windows Live Mail 2010.

= 2010.1 =
Aquesta versió se centra principalment en la correcció d'errors i en la millora de l'experiència de l'usuari, incloent algunes correccions importants d'estabilitat. 

== Noves característiques ==
* NVDA ja no falla en iniciar-se en un sistema que no tingui dispositius de sortida d'àudio. Òbviament, en aquest cas caldrà usar per a la sortida un dispositiu Braille o el sintetitzador Silence, en conjunció amb el Visor de veu  
* Una casella per informar dels marcs s'ha afegit al diàleg Formatació de documents que et permet configurar si NVDA hauria d'anunciar els marcs en els documents web. Per compatibilitat amb les versions prèvies, l'opció apareix activada per defecte.  
* Si "Verbalitza les tecles d'ordres"  està activat, NVDA anunciarà ara els noms de les tecles multimèdia (per exemple, reprodueix, atura, inici, etc...) quan aquestes es premin en una part dels teclats. (#472)
* NVDA anuncia ara la paraula que s'esborra quan es prem  control+retrocés in controls que ho suporten. (#491)
* Les tecles de cursor poden ser usades en la finestra de format Web per navegar i llegir el text.  (#452)
* Ara es suporta la llista d'entrades dins de la llibreta d'adreces del Microsoft Office Outlook.
* NVDA suporta ara millor documents editables incrustats en Internet Explorer (mode disseny) (#402)
* Un nou script (nvda+shift+numpadMinus) et permet ara moure el focus del sistema cap al objecte en curs de navegació.
* Nous scripts per bloquejar i desbloquejar els botons dret i esquerra del ratolí.  Això és útil per realitzar les operacions d'arrossegar i deixar anar. Maj+TeclNumDivisió per bloquejar/desbloquejar el botó esquerra i Maj+TeclNumMultiplicar per bloquejar i desbloquejar el dret.
* Noves taules de traducció braille: Alemany 8 punts ordinador braille, Alemany grau 2, Finlandès 8 punts ordinador Braille, Xinès (Hong Kong, Cantonès, Xinès (Taiwan, Mandarí).(#344, #369, #415, #450)
* Ara és possible desactivar la creació de l'accés directe de l'escriptori (i, per tant, la tecla d'accés directe) quan s'instal·la NVDA. (#518)
* NVDA pot usar ara IAccessible2 quan es trobi present en aplicacions de 64 bits. (#479)
* Millorat el suport per regions vives a les aplicacions Mozilla. (#246)
* La  NVDA Controller Client API es subministra ara per permetre que les aplicacions controlin NVDA; per exemple, per a parlar text, silenciar, mostrar un missatge en Braille, etc.   
* Els missatges d'informació i error es llegeixen ara en la pantalla d'inici de sessió en  Windows Vista i Windows 7. (#506)
* l'Adobe Reader suporta ara formularis PDF interactius desenvolupats amb l'Adobe LiveCycle. (#475)
* A Miranda IM, NVDA llegeix de forma automàtica els missatges entrants en el xat si està activat que informi dels canvis dinàmics del contingut. A més, s'han afegit també comandaments per a informar dels tres missatges més recents (NVDA+control+número). (#546)
* Ara el contingut dels camps d'entrada de text apareixen suportats en l'Adobe Flash. (#461)

== Canvis ==
* Ja no s'informa del missatge extremadament detallat d'ajuda del teclat en el menú d'inici de Windows 7. 
* El sintetitzador Display ha estat reemplaçat per un nou visor de veu. Per a activar-lo, escolliu  Visor de veu des del menú Eines. El visor de veu pot ser usat independentment del sintetitzador de veu que esteu fent servir. (#44)
* Els missatges de la línia Braille seran automàticament descartats si l'usuari prem una tecla que impliqui un canvi, com ara el moviment del focus. Prèviament el missatge s'hauria mantingut sempre actiu durant el temps que hagués estat determinat. 
* La decisió sobre si el Braille ha de vincular-se al focus o al cursor de revisió   (NVDA+control+t) es pot ara configurar des del diàleg de paràmetres del Braille i, ara es salva també en la configuració de l'usuari.
* S'ha actualitzat el sintetitzador de veu eSpeak a la versió 1.43.
* El traductor liblouis Braille s'ha actualitzat a la versió 1.8.0.
* En les memòries virtuals, la informació dels elements quan es mouen per caràcter o paraula s'ha millorat molt. Prèviament, es donava una gran quantitat d'informació irrellevant i l'informe era molt diferent al que es feia quan el moviment era per línia. (#490)
* La tecla Control simplement atura la veu com altres tecles, en lloc de pausar-la. Per a pausar/reiniciar la parla, cal usar la tecla Maj.  
* Els recomptes de files i columnes de les taules ja no es reporten quan canvia el focus de l'informe, ja que aquesta informació és molt densa i normalment no és útil.   

== Correccions d'errors ==
* NVDA ja no s'atura en començar si  el suport UI Automation sembla estar disponible però s'atura en inicialitzar-se per alguna raó.  (#483)
* Ja no s'informa, com de vegades, del contingut sencer de la fila d'una taula quan es mou el focus dins d'una cel·la en les aplicacions Mozilla. (#482)
* NVDA  ja no triga molt de temps en l'expansió d'ítems en vista d'arbre que continguin una gran quantitat de sub-items.  
* Quan es llisten les aplicacions SAPI 5, NVDA intenta ara detectar veus amb errors i excloure-les dels diàlegs de paràmetres de veu i del anell de configuracions del sintetitzador. Prèviament, quan hi havia només una veu problemàtica, el controlador SAPI5 de NVDA de vegades fallava en inicialitzar-se. 
* Les memòries intermèdies virtuals ara fan cas de l'opció de configuració "Informa de les tecles de drecera de l'objecte" que es pot trobar en el diàleg de presentació de l'objecte.   (#486)
* En les memòries intermèdies virtuals, les coordenades fila/columna ja no es llegeixen de forma incorrecta per a les files i les columnes quan els reports de taules estan desactivats. 
* En les memòries intermèdies virtuals les coordenades es llegeixen ara correctament quan es deixa una taula i després es torna a entrar en la mateixa cel·la de la taula sense visitar-ne cap altra primer. Per exemple, quan es prem FletxaAmunt i després FletxaAvall en la primera cel·la d'una taula. 
* Les línies en blanc dels documents del Microsoft Word i els controls d'edició en el Microsoft HTML es mostren ara adequadament en línies Braille. Prèviament NVDA mostrava la frase actual a la 

pantalla, no la línia actual per aquestes situacions. (#420)
* S'han fet correccions múltiples de seguretat quan s'executa NVDA a l ‘inici de sessió de Windows i d'altres escriptoris segurs.  (#515)
* La posició del cursor s'actualitza ara correctament quan es fa un Verbalitza-ho tot que surt del final de la pantalla en camps d'edició estàndard de Windows i en documents del Microsoft Word.
* En memòries intermèdies virtuals, ja  no s'inclou text de forma incorrecta en imatges que estan dins de links i en clicables que estan marcats com irrellevants per als lectors de pantalla.
* Correccions a la disposició del teclat dels ordinadors portàtils.
* Quan el Braille ha de revisar una finestra de consola DOS que ha estat enfocada, el cursor de revisió pot ara navegar de forma adequada pel text en la consola.
* En treballar amb  TeamTalk3 o TeamTalk4 Classic, la barra de progrés metro VU en la finestra principal, ja no s'anuncia com si s'estigués actualitzant. A més els caràcters especials poden ser llegits adequadament en la finestra entrant de xat.
* Els ítems ja no s'anuncien dues vegades en el menú d'inici de sessió de Windows 7. (#474)
* En activar enllaços de la mateixa pàgina en Firefox 3.6 el cursor es mou apropiadament al virtualBuffer cap al lloc correcte de la pàgina.
* Solucionat el problema pel qual algun text de documents PDF no es reproduïa en l'Adobe Reader. 
* NVDA ja no llegeix de forma incorrecta determinats números separats per un guió; per exemple 500-1000. (#547)
* A Windows XP, NVDA ja no fa que Internet Explorer es congeli quan es commuten caselles de verificació a Windows Update. (#477)
* Quan es fa servir el sintetitzador incorporat eSpeak l'emissió simultània de parla i xiulets ja no causa de forma intermitent congelacions en alguns sistemes. Això era molt evident, per exemple, quan es copiaven grans quantitats de dades al Windows Explorer.
* NVDA ja no avisa que un document Firefox està ocupat (per exemple, a causa d'una actualització o d'un refresc) si el document està en segon pla. Això també feia que la barra d'estat de l'aplicació activa fos anunciada de forma errònia.
* Quan es canvia la distribució del teclat Windows (amb Control+Maj or Alt+Maj), s'informa del nom complet de la nova distribució, tant de forma parlada com en Braille. Prèviament només s'informava de forma parlada i les distribucions alternatives no s'anunciaven de cap manera  (per exemple, Dvorak).
* Si l'opció d'informar de les taules està desactivada, la informació de la taula ja no es llegeix quan es canvia el focus. 
* Ara es pot accedir a alguns estàndards en controls en vista d'arbre en aplicacions de 64 bits.  (per exemple, la vista d'arbre dels continguts en l'ajuda del Microsoft HTML). (#473)
* S'han solucionat alguns problemes amb la càrrega de missatges que contenien caràcters no-ASCII. Això podia causar falsos errors en alguns casos en sistemes no anglesos. (#581)
* La informació Quant a NVDA ara apareix en l'idioma configurat per l'usuari enlloc de sempre aparèixer en anglès.   (#586)
* Ja no es troben problemes quan es  fa servir l'anell de configuracions del sintetitzador una vegada s'ha canviat la veu a una altra que té menys opcions que la veu anterior.  
* A l'Skype 4.2, els noms dels contactes ja no es parlen dues vegades al llistat de contactes.
* S'han solucionat alguns problemes potencialment importants relatius a la pèrdua de memòria en la Interfície Gràfica d'Usuari i en les memòries intermèdies virtuals. (#590, #591)
* S'ha treballat al voltant d'un error desagradable en alguns sintetitzadors SAPI 4, que estava causant a NVDA errors freqüents i bloquejos. (#597)

## 2009.1

Els aspectes més destacats d'aquesta versió inclouen suport per a edicions de Windows de 64 bits; suport molt millorat per a documents del Microsoft Internet Explorer i l'Adobe Reader; suport per Windows 7; lectura de l'inici de sessió de Windows, pantalla de control+alt+supr i Control d'Accés d'Usuari (UAC); i la possibilitat d'interactuar amb contingut web en l'Adobe Flash i Sun Java. Hi ha hagut també correccions importants d'estabilitat i millores generals de l'experiència de l'usuari. 

### Noves característiques

* Suport oficial per a edicions Windows de 64 bits! (#309)
* S'ha afegit un control de sintetitzador per al sintetitzador Newfon. A destacar que aquest requereix una versió especial de Newfon. (#206)
* En les memòries intermèdies virtuals, el modus de focus i el d'exploració es poden ara informar amb sons enlloc de parla. Això s'habilita per defecte. Pot ser configurat des del diàleg de memòries intermèdies virtuals. (#244)
* NVDA ja no atura la parla quan es premen les tecles de control de volum al teclat, tot permetent a l'usuari canviar el volum i escoltar immediatament els resultats. (#287)
* S'han reescrit completament els documents de suport per al Microsoft Internet Explorer i l'Adobe Reader. Aquest suport ha estat unificat amb el suport bàsic usat per al Mozilla Gecko, de forma que ara hi ha disponibles en aquests documents característiques com la representació ràpida de la pàgina, la navegació ràpida extensiva, la llista d'enllaços, la selecció de text, el mode auto focus i el suport braille.
* Millora del suport per al control de selecció de la data trobat al diàleg de propietats Data / Hora de Windows Vista.
* Millora del suport per al menú d'inici del Modern XP / Vista (específicament per a tots els programes i menús de lloc). Es proporciona ara un nivell adequat d'informació.
* La quantitat de text que s'anuncia quan es mou el ratolí es pot ara configurar des del diàleg de configuració del ratolí. Es pot triar entre paràgraf, línia, paraula o caràcter.
* S'anuncien errors d'ortografia sota el cursor al Microsoft Word.
* Hi ha suport per al corrector ortogràfic del Microsoft Word 2007. Pot existir suport parcial per a les versions prèvies del Microsoft Word.
* Suport millorat per Windows Live Mail. Ara es poden llegir els missatges en text pla i poden usar els generadors de missatges en text pla i en HTML.
* A Windows Vista, si l'usuari es desplaça a l'escriptori segur (ja sigui per que apareix un diàleg UAC o per que es prem  control + alt + suprimir), NVDA anunciarà el fet que l'usuari es troba ara en l'escriptori segur.
* NVDA pot anunciar el text sota el ratolí dins de la consola DOS de Windows.
* Suport per a l'automatització UI via el client API per a automatització UI disponible a Windows 7,  així com correccions per millorar l'experiència de NVDA a Windows 7.
* NVDA pot ser configurat per iniciar-se automàticament després d'iniciar sessió en Windows. L'opció és al menú Paràmetres Generals.
* NVDA pot llegir pantalles segures de Windows com ara l'inici de sessió de Windows, les pantalles de control+alt+suprimir i de Control de Comptes d'Usuari (UAC) a Windows XP i posteriors. La lectura de l'inici de sessió de Windows es pot configurar des del menú Paràmetres generals.(#97)
* S'ha afegit un controlador per al dispositiu Braille Optelec _ALVA serie BC6
* Quan s'exploren documents web, ara es possible prémer n o shift+n, respectivament, per a saltar endavant i endarrere dels diversos blocs d'enllaços.
* Quan s'exploren documents web, ara s'informen les marques ARIA i és possible moure's entre elles amb d o shift+d, respectivament. (#192)
* El menú Llista d'Enllaços disponible quan s'exploren documents webs ha esdevingut ara un menú de la Llista d'elements que pot mostrar enllaços, encapçalaments i punts de referència. Els encapçalaments i punts de referència es presenten de forma jeràrquica.(#363)
* El nou menú Llista d'Elements, conté un camp "Filtrar per" que permet filtrar la llista fins obtenir només aquells ítems que incloguin el text que ha estat escrit. (#173)
* Les versions portables de NVDA ara miren dins del directori 'userConfig' localitzat dins el directori NVDA, per a la configuració de l'usuari. Igual com per a la versió d'instal·lació, això manté la configuració de l'usuari separada del mateix NVDA.
* Els mòduls d'aplicacions personalitzades, els controladors de dispositius Braille i els controladors dels sintetitzadors poden ara ser emmagatzemats en el directori de configuració d'usuari. (#337)
* Les memòries intermèdies virtuals es presenten ara en segon pla, permetent a l'usuari interactuar amb el sistema en certa mesura durant el procés d'extracció. L'usuari serà notificat si el document que s'està extraient pren més d'un segon de temps.
* Si NVDA detecta que s'ha aturat per alguna raó, passarà automàticament totes les pulsacions a fi que l'usuari tingui majors possibilitats de recobrar el sistema. 
* Suport per  arrossegar i deixar anar ARIA al Mozilla Gecko. (#239)
* El títol del document i la línia seleccionada es parlen ara quan es mou el focus dins de la memòria intermèdia virtual. Això fa que el comportament quan es mou el focus dins de les memòries intermèdies virtuals sigui consistent amb els objectes normals de documents.(#210)
* En les memòries intermèdies virtuals és possible ara interactuar amb objectes embeguts (com contingut l'Adobe Flash i Sun Java) tot prement retorn sobre l'objecte. Si aquest és accessible, aleshores és pot tabular al seu voltant com en qualsevol altre aplicació. Per retornar el focus al document cap prémer NVDA + espai. (#431)
* En les memòries intermèdies virtuals, useu o i shift + o, (respectivament) per moure-us del següent a l'anterior objecte incrustat.
* NVDA pot accedir ara completament a les aplicacions que s'executen com administradores en Windows Vista i posteriors. Cal instal·lar una versió oficial de NVDA per que això funcioni. No funciona en versions portables i snapshots. (#397)

== Canvis ==
* NVDA ja no anuncia "NVDA iniciat" quan s'inicia.
* Els sons d'inici i sortida es reprodueixen ara usant el dispositiu de sortida d'àudio configurat a NVDA, enlloc del dispositiu de sortida d'àudio per defecte de Windows. (#164)
* La barra de progrés d'informes ha estat millorada. En especial, ara es pot configurar NVDA per anunciar-se via parla i xiulets al mateix temps.
* Algunes funcions genèriques com ara panell, aplicació i marc, ja no es reporten llevat que el control no tingui nom. 
* El comandament de revisió de còpia (NVDA+f10) copia el text des de la marca inicial i a fi d'incloure la posició de la revisió en curs, més que d'excloure aquesta posició. Això permet copiar el darrer caràcter en una línia, el que abans no era possible.  (#430)
* El script navigatorObject_where script (ctrl+NVDA+numpad5) ha estat eliminat. Aquesta combinació de tecles no funcionava en alguns teclats, ni tampoc sembla que fos trobat gaire útil.
* El script navigatorObject_currentDimentions ha  estat reassignat com NVDA+numpadDelete. L'antiga combinació de tecles no funcionava en alguns teclats. Aquest script permet ara informar de la alçada i la llargada del objecte enlloc de les coordenades superior i inferior.
* Millora del rendiment (especialment en portàtils) quan es produeixen molts xiulets en ràpida successió, per exemple quan hi ha moviments ràpids del ratolí amb les coordenades d'àudio habilitades. (#396)
* El so d'error de NVDA ja no es reprodueix en versions intermèdies o finals. Cal notar, però, que els errors encara es registren.

== Correccions d'errors ==
* Quan NVDA s'executa des d'una ruta DOS 8.3. però es troba instal·lat en una ruta amb un nom més llarg (per exemple progra~1 versus Fitxers de programa) NVDA identificarà correctament que es tracta d'una còpia instal·lada i carregarà correctament la configuració de l'usuari.
* Ara funciona correctament la parla dels títols de la finestra que està en primer pla amb NVDA+t .
* El Braille ja no mostra informació inútil, com panells no etiquetats, en el seu context focus.  
* Ja no s'anuncia informació inútil quan es canvia el focus en aplicacions Java o Lotus, com ara panells arrel, panells en capes i panells de desplaçament.
* S'ha fet molt més usable el camp de recerca per paraules clau a l'ajuda de Windows (CHM). A causa de errades en aquest control, la paraula clau no podia ser llegida i funcionava com si canviés contínuament.
* Informa dels números correctes de pàgina en el Microsoft Word si la numeració de pàgina s'ha ubicat específicament en el document.
* Millor suport per als camps d'edició en els diàlegs del Microsoft Word (per exemple el diàleg de Fonts). Ara és possible navegar per aquests controls amb les tecles de cursor.
* Millor suport per a consoles DOS. En concret NVDA pot llegir ara el contingut de determinades consoles que abans NVDA pensava que estaven en blanc. Prémer control+pausa ja no acaba NVDA.
* En Windows Vista i superior, l'instal·lador NVDA ara inicia NVDA amb privilegis normals d'usuari quan se li demana que executi NVDA sobre la finestra finalitzar.
* El retrocés es manega ara correctament quan es parlen paraules escrites.  (#306)
* Ja no es reporta incorrectament el "Menú Inici" en determinats contextos del explorador de Windows / interfície de Windows. (#257)
* NVDA manega ara correctament les etiquetes ARIA al Mozilla Gecko quan no hi ha cap altre contingut útil. (#156)
* NVDA ja no habilita de  forma incorrecta el mode focus per a camps de text editable, els quals actualitzen el seu valor quan el focus canvia; per exemple https://tigerdirect.com/. (#220)
* NVDA intenta ara recuperar-se d'algunes situacions que abans el feien aturar-se completament. NVDA pot trigar més de 10 segons a detectar i recuperar-se d'una aturada. 
* Quan l'idioma NVDA està en "Usuari per defecte", cal usar la configuració d'idioma de pantalla de l'usuari de Windows, enlloc de la configuració local de Windows. (#353)
* NVDA reconeix ara l'existència de controls en AIM 7.
* La clau d'accés entre comandaments ja no s'encalla si es manté premuda una tecla. Prèviament, NVDA s'aturava acceptant comandaments i si això passava havia de ser reinicialitzat. (#413)
* La barra de tasques ja no s'ignora quan rep el focus, cosa que sol passar quan es surt d'una aplicació. Anteriorment, NVDA es comportava com si el focus no havia canviat en absolut.
* Quan es llegeixen camps de text en aplicacions que fan servir el Java Access Bridge (incloent OpenOffice.org), NVDA funciona ara correctament si està habilitat que s'informi dels números de línia. 
* El comandament de revisió de còpies (NVDA+f10) manega adequadament la situació en cas que s'usi en una posició abans de la marca d'inici. Amb anterioritat això podia causar problemes com ara caigudes a Notepad++.
* Un cert caràcter de control 0x1) ja no causa un comportament estrany eSpeak (com ara canvis en el volum i el to) quan es troba en el text. (#437)
* El comandament d'informe de selecció de text (NVDA+Maj+FletxaAmunt) ara informa adequadament que no hi ha selecció en objectes que no suporten la selecció de text.
* S'ha solucionat el problema segons el qual, quan es premia la tecla retorn en determinats botons o enllaços Miranda-IM, NVDA es penjava. (#440)
* La línia o selecció actual es respecta ara adequadament quan es lletreja o es copia l'objecte actual del navegador.
* S'ha treballat al voltant d'un error de Windows que estava causant problemes en ser parlat després del nom d'enllaços de control a l'explorador de Windows i als diàlegs de l'Internet Explorer. (#451)
* S'ha solucionat un problema amb el comandament d'informe de data i hora (NVDA+f12). Anteriorment, l'informe de la data apareixia truncat en alguns sistemes. (#471)
* S'ha solucionat el problema segons el qual el indicador de lector de pantalla del sistema era de vegades esborrat de forma inapropiada després d'interactuar amb pantalles segures de Windows. Això podia causar problemes en aplicacions que comproven l'indicador de lector de pantalla. Això podia causar problemes en aplicacions que comprovaven la bandera del lector de pantalla, com ara  l'Skype, l'Adobe Reader i Jart. (#462)
* En quadres combinats d'Internet Explorer 6, ara s'informa de l'ítem actiu quan canvia. (#342)

## 0.6p3

### Noves característiques

* Quan la barra de fórmules del Microsoft Excel és inaccessible a NVDA, es proporciona un quadre de diàleg per a l'edició quan l'usuari prem F3 sobre una cel·la.
* Suport per formatar controls de text en IAccessible2, incloent aplicacions Mozilla.
* Allà on sigui possible es pot informar ara dels errors d'ortografia. Això es pot configurar des del menú Preferències, opció Formatació de documents. .
* NVDA es pot configurar per que soni arreu o només en les barres de progrés visibles. Alternativament, pot ser configurat per parlar dels valors de la barra de progrés cada 10 %.
* Els enllaços es poden ara identificar en els controls richEdit. 
* El ratolí es pot moure ara al caràcter que hi ha sota el cursor de revisió en la major part dels controls de text editables. Abans el ratolí només es podia moure al centre del control.
* A les memòries intermèdies virtuals, el cursor de revisió revisa ara el text de la memòria intermèdia i no  només el text intern del navegador d'objectes (fet que sovint no és útil al usuari). Això vol dir que es pot navegar de forma jeràrquica per la memòria intermèdia virtual utilitzant la navegació d'objectes i el cursor de revisió es mourà cap aquest lloc a la memòria intermèdia. 
* Es fan servir alguns estats addicionals sobre els controls de Java.
* Si el comandament títol (NVDA+t) es prem dues vegades, es lletreja el títol. Si es prem 3 vegades es copia al porta-retalls. 
* L'ajuda del teclat llegeix ara els noms de les tecles modificadores quan es premen separadament. 
* Ara es poden traduir els noms de tecla que figuren amb l'ajuda del teclat. 
* S'ha afegit suport per al camp de text reconegut a SiRecognizer. (#198)
* Suport per a dispositius Braille!
* S'ha afegit un comandament (NVDA+c) per a informar del text que hi ha al porta-retalls de Windows. (#193)
* En les memòries intermèdies virtuals, si NVDA canvia de forma automàtica a mode focus, es pot usar la tecla d'escapada per tornar al mode d'exploració. Es pot fer servir també NVDA+espai.
* En les memòries intermèdies virtuals quan canvia el focus o es mou el signe d'intercalació, NVDA pot canviar automàticament al mode focus o al mode d'exploració si és apropiat per al control sota el signe d'intercalació.  Això es configura des del quadre de diàleg de les memòries intermèdies virtuals. (#157)
* S'ha reescrit el controlador sintetitzador SAPI4 que reemplaça els controladors sapi4serotek i sapi4activeVoice i hauria de solucionar els problemes generats per aquests controladors.
* L'aplicació NVDA inclou ara un manifest, que vol dir que ja no s'executa en mode de compatibilitat en Windows Vista.
* El fitxer de configuració i els diccionaris d'idiomes es guarden ara en el directori de dades d'aplicació d'usuari si NVDA va ser instal·lat usant l'instal·lador. Això és necessari per Windows Vista i permet que usuaris diferents tinguin diferents configuracions de NVDA.
* S'ha afegit suport per la informació de la posició dels controls IAccessible2.
* S'ha afegit la possibilitat de copiar text del porta-retalls utilitzant el control de revisió. NVDA+f9 estableix l'inici del marcat en la posició actual del cursor de revisió. NVDA+f10 recupera el text entre l'inici del marcat i la posició actual del cursor de revisió i el copia al porta-retalls.(#240)
* S'ha afegit suport per alguns controls d'edició en el programari de TV Pinacle.
* Quan s'anuncia el text seleccionat per seleccions llargues (512 caràcters o més), NVDA ara diu el nombre de caràcters seleccionats, enlloc de dir la selecció completa.  (#249)

== Canvis ==
* Si el dispositiu de sortida d'àudio està configurat per a usar el dispositiu per defecte de Windows (Microsoft Sound Mapper), NVDA canviarà ara el nou dispositiu eSpeak per defecte i avisarà quan canviï el dispositiu per defecte. Per exemple, NVDA canviarà a un dispositiu d'àudio USB si aquest esdevé el dispositiu per defecte una vegada sigui connectat.
* Es millora el rendiment de eSpeak amb alguns controladors d'àudio de Windows Vista.
* L'informe d'enllaços, encapçalaments, taules, llistes i cites en bloc, es pot configurar ara des del diàleg de Formatació de Documents. De forma prèvia a la configuració d'aquests paràmetres, per a les memòries intermèdies virtuals, s'hauria de fer servir el diàleg de configuració de les memòries intermèdies virtuals. Ara tots els documents comparteixen aquesta configuració. 
* RATE és ara la configuració per defecte en l'avís de la configuració del sintetitzador de veu. 
* Millorada la càrrega i descàrrega de appModules.
* El comandament títol (NVDA+t) ara informa només del títol enlloc de l'objecte sencer. Si l'objecte en primer pla no té nom, s'utilitza el nom de procés de l'aplicació.
* En lloc que la memòria intermèdia virtual passi endins i en fora, NVDA ara informa del mode focus (passar per dins) i del mode d'exploració (passar per fora).
* Les veus estan ara emmagatzemades dins del fitxer de configuració per ID enlloc de per un índex. Això fa que els paràmetres de veu siguin més fiables entre sistemes entre canvis de configuració. Els paràmetres de veu no es conservaran en configuracions antigues i això pot donar error la primera vegada que es faci servir un sintetitzador. (#19)
* El nivell d'una vista jeràrquica s'anuncia primer si ha canviat des del ítem enfocat prèviament per a totes les vistes jeràrquiques. Abans això només passava en vistes jeràrquiques natives de Windows. (SysTreeView32) 

== Correccions d'errors ==
* El darrer tros d'àudio ja no es talla quan es fa servir NVDA amb eSpeak sobre un servidor d'escriptori remot
* S'han solucionat els problemes que hi havia amb algunes veus quan es guardaven els diccionaris de parla.
* S'ha eliminat el retard que es produïa en grans documents de text pla a les memòries intermèdies virtuals del Mozilla Gecko quan es movien per unitats diferents del caràcter (paraula, línia, etc.) cap al final de grans documents de text pla en les memòries intermèdies virtuals de Mozilla Gecko. (#155)
* Si està activada la lectura de paraules escrites, s'anuncia la paraula quan es prem "retorn".
* S'han corregit alguns problemes de conjunts de caràcters en documents richedit.
* El visor de registre NVDA ara fa servir richedit enlloc de només editar per a visualitzar el registre. Això millora la lectura per paraules amb NVDA. 
* S'han corregit alguns temes relacionats amb objectes incrustats en controls richedit. 
* NVDA ara llegeix els números de pàgina al Microsoft Word. (#120)
* S'ha corregit el problema segons el qual, quan es tabulava cap a una casella marcada en la memòria intermèdia virtual al Mozilla Gecko i es marcava la tecla espai, no s'anunciava que la casella es desmarcava.
* Ara s'informa correctament de caselles parcialment marcades en aplicacions Mozilla. 
* Si la selecció de text s'expandeix o es contreu en totes dues direccions, la lectura es fa com un únic tros, no com dos. 
* Quan es llegeix amb el ratolí, el text en camps editables al Mozilla Gecko, hauria de ser llegit ara. 
* El Verbalitza-ho tot no hauria de causar que es bloquegessin certs sintetitzadors SAPI5.
* Solucionat un problema que implicava que els canvis en la selecció de text no eren llegits en els controls estàndards d'edició de Windows abans que es canviés el primer focus després de l'inici de NVDA.
* S'ha solucionat el seguiment del ratolí en objectes Java. (#185)
* NVDA ja no informa de les vistes d'arbre Java quan els elements no tenen fills i estan plegats.
* S'anuncia l'objecte amb focus quan una finestra Java arriba al primer pla. Prèviament només s'anunciava el nivell superior de l'objecte Java. 
* El controlador del sintetitzador eSpeak ja no atura completament la parla després d'un error simple. 
* Solucionat el problema segons el qual els paràmetres de veu actualitzats (velocitat, to, etc.) no es salvaven quan la veu era canviada des del grup d'opcions del sintetitzador.
* Millorada la parla dels caràcters i les paraules escrits.
* Alguns textos nous que prèviament no es llegien en aplicacions de consola de text (com en alguns jocs d'aventura), ara ja parlen.
* NVDA ignora ara els canvis de focus en finestres que no estan en primer pla. Abans, un focus que no estava en primer pla podia ser tractat com si hi hagués un canvi de focus real. 
* Millorada la detecció del focus quan es deixaven els menús contextuals. Prèviament, NVDA sovint no reaccionava quan es deixava un menú contextual.
* NVDA ara anuncia quan s'activa el menú contextual en el menú Inici.
* El tradicional menú Inici ara s'anuncia com menú Inici enlloc de menú de l'Aplicació. 
* Millorada la lectura d'alertes com les que s'han trobat al Mozilla Firefox. El text no s'hauria de llegir múltiples vegades i tampoc d'altra informació estranya. (#248)
* El text enfocable en camps de només lectura ja no s'inclourà quan es recupera el text dels diàlegs. Això soluciona, per exemple, la lectura automàtica de tota la llicència d'ús en els instal·ladors.
* NVDA ja no anuncia la desselecció de text en sortir d'alguns controls d'edició. (exemple: barra d'adreces d'Internet, camps d'adreces de correu a Thunderbird 3).
* Quan s'obre el text pla dels correus a Outlook Express, el focus es col·loca correctament en el missatge, preparat per que l'usuari ho llegeixi. Abans, l'usuari havia de prémer TAB o clicar sobre el missatge a fi de poder usar les tecles de cursor per poder-lo llegir.
* Solucionats diferents problemes amb la funció "tecles de comandament de la parla" .
* NVDA pot ara llegir més de 65535 caràcters en controls d'edició estàndard (per exemple en un fitxer gran de Notepad).
* Millorada  la lectura de línies en els camps d'edició en MSHTML (en missatges editables en Outlook Express i en camps d'entrada de dades a Internet Explorer).
* NVDA ha deixat de vegades d'aturar-se quan s'edita text en OpenOffice. (#148, #180)

## 0.6p2

* Millorada la veu ESpeak per defecte en NVDA
* S'ha afegit una disposició de teclat per ordinadors portàtils. Les disposicions de teclats es poden configurar des del menú Paràmetres de teclat. (#60)
* S'ha afegit suport per agrupar elements en controls SysListView32, que es troben principalment a Windows Vista. (#27)
* S'informa de l'estat comprovat dels elements en vista d'arbre en els controls SysTreeview32.
* S'han afegit tecles d'accés directe per a molts dels diàlegs de configuració NVDA. 
* S'ha activat suport per IAccessible2 en aplicacions com Mozilla Firefox, quan s'executa NVDA des d'un mitjà portàtil, sense que calgui registrar fitxers DLL específics. 
* S'ha reparat un bloqueig amb la llista d'enllaços a les memòries intermèdies virtuals en aplicacions Gecko.  (#48)
* NVDA ja no hauria de bloquejar aplicacions Mozilla Gecko com ara Firefox i Thunderbird si NVDA s'executa amb més privilegis que l'aplicació Mozilla Gecko. Per exemple, si NVDA s'executa com administrador.
* Els diccionaris de parla (abans, diccionaris de l'Usuari) poden ser ara sensibles o no a les majúscules, i els patrons poden ser opcionalment expressions regulars. (#39)
* L'ús de un mode de format de pantalla per a documents de la memòria virtual es pot configurar ara des d'un diàleg de configuració. 
* Ja no s'informa com a enllaços de les etiquetes que no tinguin href en documents Gecko. (#47)
* El comandament de cerca de NVDA ara recorda quina va ser la darrera cerca entre totes les aplicacions. (#53)
* Solucionats problemes a les memòries intermèdies virtuals allà on no s'anunciava l'estat "marcat" en algunes caselles i botons de ràdio. 
* El mode de pas per la memòria intermèdia virtual és ara específic de cada document més que general per tot NVDA. (#33)
* Corregit cert alentiment amb els canvis d'enfocament i la incorrecta interrupció de la parla que de vegades passava quan es feia servir NVDA en un sistema que havia estat en espera o bé era més aviat lent. 
* Millorat el suport per als quadres combinats al Mozilla Firefox. En concret, quan es navega al seu voltant ja no es repeteix, i quan se surt d'ells els controls anteriors ja no s'anuncien innecessàriament. Així mateix els comandaments de memòria intermèdia virtual ara treballen quan s'està focalitzat en un que està en una memòria intermèdia virtual. 
* Millorada la precisió en localitzar la barra d'estat en diverses aplicacions. (#8)
* Afegida a NVDA la eina interactiva de la consola Python per a permetre als desenvolupadors veure i manipular parts internes de NVDA quan aquest s'està executant. 
* Els scripts Verbalitza-ho tot, Informa de la selecció i Informa de la línia activa treballen ara correctament en el mode de pas a memòria intermèdia virtual. (#52)
* S'han eliminat els scripts d'augment i disminució de taxes. Els usuaris hauran de fer servir els scripts d'opcions del sintetitzador (control+nvda+fletxes) o el diàleg Paràmetres de veu
* Es millora el rang i l'escala dels xiulets de la barra de progrés. 
* S'han afegit més tecles ràpides per a les noves memòries intermèdies virtuals:  l per llista, i per element de llista, e per camp d'edició, b per botó, x per caselles, r per botó de ràdio, g per gràfic, q per sagnat, c per desplegables, de l'1 al 6 per als respectius nivells d'encapçalament, s per separadors, m per "marc". (#67, #102, #108)
* Si es cancel·la la càrrega d'un nou document al Mozilla Firefox, ara l'usuari pot continuar la memòria intermèdia virtual del document anterior sempre i quan aquest no hagi estat ja destruït. (#63)
* La navegació per paraules a les memòries intermèdies virtuals és ara més acurada si les paraules no contenen accidentalment text de més d'un camp. (#70)
* S'ha millorat la qualitat del seguiment del focus i de l'actualització del focus quan es navega per les a les memòries intermèdies virtuals al Mozilla Gecko .
* S'ha afegit un script findPrevious script (Maj+NVDA+f3) per al seu ús a les noves memòries intermèdies virtuals.
* S'ha millorat la lentitud en els diàlegs del Mozilla Gecko (a Firefox i Thunderbird). (#66)
* S'ha afegit la possibilitat de veure el fitxer actual de registres per NVDA. Es pot trobar al menú NVDA --> Eines
* Alguns scripts, com els que diuen l'hora i la data prenen ara l'idioma configurat; la puntuació i l'ordre de les paraules reflecteixen ara el llenguatge
* El desplegable d'idioma en el diàleg de Paràmetres generals mostra ara els noms complets dels idiomes per major facilitat d'ús.
* Quan es revisa text en el objecte de navegació actual, el text sempre està actualitzat si canvia dinàmicament. Per exemple, quan es revisa un text d'un element de la llista en l'Administrador de Tasques. (#15)
* Quan hom es mou amb el ratolí, s'anuncia el paràgraf de text que hi ha sota el ratolí i no la totalitat del text o només la paraula marcada. Les coordenades d'àudio o l'anunci de les funciones de l'objecte és opcional, per defecte estan desactivades.
* En el Microsoft Word es dóna suport per a la lectura de text amb el ratolí. 
* Solucionat un error que causava selecció de text quan se sortia de la barra de menú en algunes aplicacions com Wordpad 
* A Winamp, ja no s'anuncia el títol de la pista de forma reiterada quan es canvien les pistes o quan es pausa/reprèn/atura la reproducció  
* A Winamp s'ha afegit la possibilitat d'anunciar l'estat dels controls de repetició aleatòria i de repetició quan s'intercanvien. Funciona en la finestra principal i en l'editor de llistes de reproducció. 
* Millorada la possibilitat d'activar determinats camps en les memòries intermèdies virtuals del Mozilla Gecko. Pot incloure gràfics clicables, enllaços que contenen paràgrafs i altres estructures estranyes. 
* S'ha corregit un retard inicial en obrir diàlegs NVDA en alguns sistemes. (# 65)
* S'ha afegit un suport específic per a l'aplicació Total Commander
* S'ha corregit un error al controlador sapi4serotek, on l'entonació es podia quedar encallada en un determinat valor, com ara romandre alta després de llegir una lletra majúscula. (#89)
* S'anuncia el text clicable i també altres camps clicables en les memòries intermèdies virtuals al Mozilla Gecko. Per exemple, un camp que tingui un atribut HMTL "onclick". (#91)
* Quan s'està desplaçant al voltant de les memòries intermèdies virtuals del Mozilla Gecko, es desplaça el camp actual per a veure -- això és molt útil per que les persones vidents tinguin una idea d'on es troba l'usuari en el document. (#57)
* Afegit suport bàsic per tal que les regions ARIA mostrin events en aplicacions activades en IAccessible2. Això és útil en l'aplicació IRC Chatzilla on es llegiran de forma automàtica els nous missatges. 
* S'han fet algunes lleus millores per ajudar a usar les aplicacions web activades ARIA, per exemple Google Docs
* Ja no s'afegeixen línies extres en blanc al tex quan es copia aquest des d'una memòria intermèdia virtual
* La tecla d'espai ja no activa un enllaç de la llista d'enllaços. Ara es pot fer servir com altres lletres per a començar a escriure el nom d'un determinat enllaç al qual es vulgui anar. 
* El script moveMouseToNavigator (NVDA+tecla numérica /) ara mou el ratolí al centre del objecte navegador i no a la part superior esquerra
* S'han afegit scripts per a clicar els botons dret i esquerra del ratolí (tecla numèrica / i tecla numèrica Inici respectivament)
* Millorat l'accés a la safata del sistema de Windows. Afortunadament el focus ja no hauria de semblar que retorna contínuament a un determinat ítem. Recordatori: per arribar a la safata del sistema useu el comandament Windows --> Tecla de Windows+b. (#10)
* S'ha millorat el rendiment i s'ha deixat d'anunciar text addicional quan es manté premuda una  tecla de cursor en un camp d'edició i aquest arriba a la fi. 
* S'ha suprimit  la possibilitat per NVDA que el usuari esperi mentre es parlen determinats missatges. S'han solucionat alguns bloquejos amb determinats sintetitzadors de veu. (#117)
* S'ha afegit suport per al sintetitzador de veu Audiologic Tts3, una contribució de Gianluca Casalino. (#105)
* Possibilitat de millorar el rendiment quan es navega al voltant de documents en el Microsoft Word.
* Millora de la precisió quan es llegeix text d'alertes en aplicacions Mozilla Gecko.
* S'han aturat possibles accidents quan s'intenta salvar la configuració sobre versions no angleses de Windows. (#114)
* S'afegeix un diàleg de benvinguda NVDA. Aquest diàleg s'ha dissenyat per proporcionar informació essencial als nous usuaris i permetre que BlocMaj sigui configurat com una tecla modificadora NVDA. Aquest diàleg s'iniciarà per defecte quan s'iniciï NVDA, llevat que sigui desactivat. 
* S'ha fixat el suport bàsic per l'Adobe Reader de forma que és possible llegir documents en les versions 8 i 9
* Solucionats alguns errors que podien esdevenir-se quan es mantenen premudes les tecles de baixada abans que NVDA s'iniciés completament. 
* Si l'usuari ha configurat NVDA per salvar la configuració en el moment de la sortida, assegureu-vos que la configuració es guarda correctament quan s'apaga o tanca la sessió de Windows. 
* Afegit un so al logo NVDA a l'inici de la instal·lació, contribució de Victer Tsaran
* NVDA hauria de eliminar-se netament de la safata d'entrada quan es surt de l'instal·lador i d'altres.
* Les etiquetes per controls estàndards en diàlegs NVDA (com els botons Acceptar i Cancel·lar) haurien de mostrar-se en el llenguatge que NVDA té per defecte, no només en anglès.
* La icona NVDA s'hauria d'usar ara com a accés directe en el menú inici de l'Escriptori, més que com una icona de l'aplicació per defecte. 
* Es llegeixen cel·les en MS Excel quan hom es mou amb Tab i Maj+Tab.  (#146)
* S'ha arreglat alguna doble parla en determinades llistes de l'Skype. 
* S'ha millorat el seguiment del cursor en aplicacions Java i IAccessible2; per exemple en Open Office i Lotus Symphony, NVDA espera adequadament el cursor per moure's en els documents en lloc de llegir accidentalment la paraula o línia equivocada al final d'alguns paràgrafs. (#119)
* Suport pels controls AkelEdit trobats a Akelpad 4.0
* NVDA ja no es bloqueja a Lotus Symphony en passar del document a la barra de menú.
* NVDA ja no es congela en les applets d'Afegir/Eliminar programes de Windows XP quan es llança un desinstalador.  (#30)
* NVDA ja no es congela quan s'obre Spybot Search and Destroy

= 0.6p1 =

== Accés al contingut web amb noves memòries intermèdies virtuals en procés (fins ara per aplicacions Mozilla Gecko incloent Firefox3 i Thunderbird3) ==
* Els temps de càrrega han millorat gairebé per un factor de trenta (ja no cal esperar per que la majoria de les pàgines web es carreguin a la memòria intermèdia)
* S'ha afegit una llista d'enllaços(NVDA+f7)
* Millorar el diàleg de cerca (control+nvda+f) de forma que permet una cerca que no te en compte majúscules i minúscules. S'han solucionat també alguns problemes de focus amb aquest diàleg.
* Ara és possible seleccionar i copiar text en les noves memòries intermèdies virtuals
* Per defecte, les noves memòries intermèdies virtuals representen el document en un format de pantalla (els enllaços i els controls no estan en línies separades llevat que siguin veritablement visuals). Aquesta funció es pot canviar amb NVDA+v.
* Es possible moure's pels paràgrafs amb control+fletxa amunt i control + fletxa avall.
* Millorat el suport per al contingut dinàmic.
* S'ha millorat molt la precisió de lectura de línies i camps quan es navega amunt i avall. 

== Internacionalització ==
* Mentre corre NVDA ara és possible teclejar caràcters accentuats que reposen sobre un "caràcter mort".
* NVDA informa ara quan es canvia la distribució de teclat (prement alt+shift).
* La característica que anuncia la data i l'hora ara agafa les opcions locals i de llenguatge configurades al sistema. 
* Afegida traducció al txec (per Tomas Valusek amb ajuda de Jaromir Vit)
* Afegida traducció al vietnamita per Dang Hoai Phuc
* Afegida traducció a l'africà (af_ZA), per Willem van der Walt.
* Afegida traducció al rus per Dmitry Kaslin
* Afegida traducció al polonès per Dorota Czajka i amics.
* Afegida traducció al japonès per Katsutoshi Tsuji.
* Afegida traducció al tailandès per Amorn Kittikhun Rata
* Afegida traducció al croat Mario Percinic i Hrvoje Katic
* Afegida traducció al gallec per Juan C. Buno
* Afegida traducció a l'ucraïnès per Aleksey Sadovoy

== Parla ==
* NVDA ara ve amb 1.33, que conté moltes millores, entre les quals podem esmentar la millora dels idiomes, variants conegudes i capacitat de parlar més ràpid.
* El diàleg de configuració de veu permet ara canviar la variant d'un sintetitzador si el suporta. La variant usualment és una lleugera variació de la veu en curs (eSpeak suporta variants).
* Afegida la possibilitat de canviar la inflexió d'una veu en el diàleg de configuració de veu, sempre i quan el sintetitzador ho suporti. (eSpeak suporta inflexions).
* Afegida la possibilitat de desactivar la parla que dóna informació sobre la posició d'un objecte (per exemple, 1 of 4). Aquesta opció es pot trobar en el diàleg de configuració Presentació d'objectes.
* NVDA pot ara xiular quan hi ha una lletra majúscula. Això es pot activar i desactivar amb una casella que es troba al diàleg de Paràmetres de veu. També s'ha afegit la possibilitat de canviar de to per a les Majúscules a fi de configurar si NVDA hauria de canviar el seu to normal per a les majúscules.  Així ara pots canviar el to, dir Maj, o xiular les majúscules. 
* Afegida la possibilitat de pausar la parla en NVDA (com s'havia fet en Voice Over als Mac). Quan NVDA està parlant es pot prémer el control o les tecles de majúscula per silenciar la parla, però si aleshores es torna a teclejar la tecla de majúscula (sempre que no s'hagi premut cap altre tecla) la parla continuarà exactament on s'ha aturat. 
* Afegit un synthDriver virtual que envia text a una finestra enlloc de parlar via un sintetitzador de veu. Això hauria de ser més agradable per als desenvolupadors vidents que no estan acostumats a usar la síntesi de veu però que volen saber el que diu NVDA. Segurament encara hi ha alguns errors pel que qualsevol feedback serà molt benvingut.
* NVDA ja no informa per defecte de la puntuació. Es pot activar la parla de la puntuació amb NVDA+p
* eSpeak parla ara per defecte una mica més lent, cosa que hauria de facilitar-ne l'ús a aquells que instal·len o fan servir NVDA per primera vegada, 
* S'han afegit diccionaris de veu a NVDA. Això permet que NVDA llegeixi determinats textos de forma diferent. Hi ha tres diccionaris : per defecte, de veu i temporals. Les entrades que s'afegeixin al diccionari per defecte restaran per sempre a NVDA. Els diccionaris de veu són específics del sintetitzador i de la veu que estiguin actius en un determinat moment. I els diccionaris temporals serveixen per aquells moments en que s'està fent una determinada tasca i es vol fer una regla però no es desitja que sigui permanent (desapareixerà quan es tanqui NVDA). Per ara les normes són expressions regulars, no només text normal.
* Els sintetitzadors poden usar ara qualsevol dispositiu de sortida d'àudio en el sistema, tot seleccionant el dispositiu de sortida en desplegable ubicat en el diàleg Sintetitzador abans de triar el sintetitzador que es desitja. 

== Rendiment ==
* Quan s'editen missatges amb els controls d'edició en MSHTML, NVDA ja no ocupa una enorme quantitat de memòria del sistema. 
* Millorat el rendiment quan es revisa text dins de molts controls que no tenen en l'actualitat un cursor real. Per exemple, historial de MSN Messenger, ítems en vista d'arbre, ítems en vista de llistat, etc.
* Millorat el rendiment en documents d'edició complexa.
* NVDA ja no hauria de funcionar lentament en la memòria del sistema sense raó. 
* Corregits els errors que es donaven quan s'intentava focalitzar sobre una finestra de consola DOS tres o més vegades. NVDA tenia tendència a bloquejar-se completament.

== Comandaments de teclat ==
* NVDA+shift+Teclat numèric 6 and NVDA+shift+teclat numèric 4 permeten navegar cap als objectes anteriors i posteriors respectivament. Això vol dir que es pot navegar en una aplicació fent servir només aquestes dues tecles sense que calgui preocupar-se d'anar cap al pare o baixar fins al primer fill quan et mous per la jerarquia de l'objecte.  Per exemple, en un navegador web com Firefox es pot navegar pels objectes d'un document fent servir només aquestes dues tecles. Si el següent o l'anterior en el flux et porta amunt i fora d'un objecte o bé avall i dins d'un objecte, determinats xiulets indiquen la direcció.
* Ara es poden configurar els paràmetres de veu sense que calgui obrir el diàleg de Paràmetres de veu, tot fent servir l'anell de paràmetres del sintetitzador.  L'anell d'opcions del sintetitzador és un grup d'ajustos de veu. Es pot recórrer prement Control + NVDA + dreta i control + NVDA + esquerra. Per canviar un control de l'ús d'ajust + NVDA + amunt i control + NVDA + avall.
* S'ha afegit un comandament per informar de la selecció en curs en camps d'edició (NVDA+Maj+FletxaAmunt).
* Bastants comandaments que parlen text a NVDA (com el que informa de la línia en curs etc) poden ara lletrejar el text si es prem dues vegades ràpidament.
* També, si una d'aquestes tecles es fa servir prement la tecla dues vegades sense prémer cap altra tecla, s'enviarà la tecla al sistema operatiu, com si haguessis premut la tecla sense que NVDA estès actiu. Per convertir alguna d'aquestes tecles en tecla modificadora NVDA, cal marcar la casella corresponent en el diàleg Paràmetres de teclat (el que s'acostumava a anomenar diàleg d'eco de teclat. 

== Suport a aplicacions ==
* S'ha millorat el suport per documents Firefox3 i Thunderbird3. Els temps de càrrega han millorat en gairebé un factor de trenta, es fa servir per defecte un format de pantalla (cal prémer nvda+v per canviar entre aquest i l'absència de format de pantalla), s'ha afegit una llista d'enllaços (nvda+f7), el diàleg de cerca (control+nvda+f) no distingeix entre majúscules i minúscules, hi ha molt millor suport per al contingut dinàmic i ara és possible seleccionar i copiar text.  
* A les finestres d'historial de MSN Messenger i Windows Live Messenger és ara possible seleccionar i copiar text.
* S'ha millorat el suport per l'aplicació Audacity
* S'ha afegit suport per uns pocs controls text/edició a l'Skype.
* S'ha millorat el suport per a l'aplicació Miranda de missatgeria instantània.  
* S'han solucionat alguns problemes de focus quan s'obrien missatges en html i en text pla a l'Outlook Express. 
* Els camps de missatge dels grups de notícies  es troben ara marcats correctament a Outlook Express 
* NVDA pot ara llegir les adreces als camps de missatge de Outlook Express   (Per a/de/cc etc)
* NVDA hauria de ser ara més acurat en anunciar els següents missatges en Outlook Express quan s'esborra un missatge de la llista de missatges.  

== APIs i eines ==
* Millorada la navegació d'objectes per objectes MSAA. Si una finestra té un menú de sistema, barra de títol o barres de desplaçament ara es pot navegar cap a elles.  
* S'ha afegit suport per a l'API d'accessibilitat IAccessible2. A banda de la possibilitat de anunciar més tipus de control, això també permet a NVDA accedir al cursor en aplicacions com Firefox 3 i Thunderbird 3, tot permetent navegar, seleccionar o editar text.  
* S'ha afegit suport per als controls d'edició de Scintilla (aquests controls es poden trobar a a Notepad++ o Tortoise SVN).
* S'ha afegit suport per aplicacions Java (via el Java Access Bridge). Això permet proporcionar suport bàsic per Open Office (si Java està activat) i per qualsevol altra aplicació independent de Java. Recordeu que els applets de java pot ser que ara no funcionin en un navegador web.

### Ratolí

-Millorat el suport a la lectura del que hi ha sota el punter del ratolí quan es mou.  Ara és  molt més ràpid i dóna també la possibilitat que, en alguns controls Java i Iaccessible2 i en alguns camps estàndards d'edició, es pugui llegir la  paraula actual i no només  l'objecte actual. Això pot ser usat per algunes persones amb discapacitat visual que només volen llegir una petita part del text amb el ratolí .  

* S'ha afegit una nova opció de configuració, que es pot trobar al diàleg de Paràmetres del ratolí.  La reproducció d'àudio quan es mou el ratolí, si és comprova, reprodueix un xiulet a 40 m quan el ratolí es mou , amb el seu to (entre  220 i 1760 hz) representant l'eix y i el volum esquerre/dret representant l'eix x  Això permet que una persona cega tingui una idea aproximada d'on està el ratolí i del seu moviment. Aquesta opció també depèn que l'opció "Emet les coordenades per àudio quan el ratolí es mogui", estigui activada. Això vol dir que si necessiteu desactivar totes dues coses (xiulets i anunci d'objectes) només cal prémer NVDA+m. Els xiulets seran més forts o més febles depenent de com n'és de brillant la pantalla en el moment.    

== Presentació i interacció d'objectes ==
* Millorat el suport per als controls treeview més comuns. NVDA ara diu quants ítems hi ha en la branca quan aquesta s'expandeix. També anuncia el nivell quan es mou dins i fora de les branques. I anuncia, el nombre de l'ítem actual i el nombre d'ítems d'acord amb la branca actual, no d'acord amb la vista d'arbre sencera.   
* S'ha millorat el que s'anuncia quan canvia el focus quan hom es mou al voltant d'aplicacions o en el sistema operatiu. Ara, enlloc de només sentir el control del qual s'està sentint informació, s'escolta informació sobre qualsevol control en el que aquest control estigui posicionat. Per exemple si tu tabules i actives un botó dins d'un grup d'opcions el grup d'opcions també s'anunciarà.
* NVDA intenta 	ara informar dels missatges existents dins dels quadres de diàleg  que apareixen. Això funciona correctament la major part del temps, bé que pot haver bastant diàlegs que no estiguin tant ben fets com haurien d'estar.
* S'ha afegit "Informa de la posició de l'objecte" al diàleg de configuració "Presentació d'objectes". Això permet als usuaris que ho desitgin desactivar l'opció per tal que NVDA deixi d'informar d'una bona quantitat de descripcions extra sobre determinats controls, com passa en aplicacions Java.
* NVDA anuncia de forma automàtica el text seleccionat en controls d'edició quan el focus es mou cap a ells. Si no hi ha cap text seleccionat, aleshores anuncia només la línia actual com de costum. 
* NVDA és ara més curós quan emet xiulets per indicar canvis en la barra de progrés en les aplicacions. Ja no embogeix en aplicacions Eclipse com ara Lotus Notes / Symphony i Accessibility Probe

== Interfície d'usuari ==
* Eliminada la finestra d'interfície NVDA i reemplaçada amb un simple menú emergent.   
* El diàleg de NVDA Paràmetres de la interfície d'usuari ha passat a anomenar-se ara Paràmetres Generals. Ara també conté un paràmetre extra: un desplegable per a determinar el nivell de registre en el qual els missatges haurien d'anar cap el fitxer de registres NVDA. Cal notar que el fitxer de registres NVDA s'anomena ara nvda.log i no debug.log.
* Eliminada la casella sobre informar dels noms de grup d'objectes  del diàleg Presentació d'objectes. L'informa dels noms de grup es gestiona ara de forma diferent. 

## 0,5

* NVDA té ara un sintetitzador incorporat anomenat eSpeak, desenvolupat per Jonathan Duddington. Es molt sensible, ocupa poc espai i ofereix suport per a diferents llenguatges. Es poden fer servir encara els sintetitzadors Sapi però es farà servir per defecte eSpeak. 
* eSpeak no depèn de cap software en especial per a la seva instal·lació, de forma que pot ser usat conjuntament amb NVDA en qualsevol ordinador, en una unitat flaix USB o en qualsevol altre dispositiu.  . 
* Per més informació sobre eSpeak, o per localitzar altres versions aneu a https://espeak.sourceforge.net/.
* Corregit un error segons el qual s'anunciava un caràcter erroni quan es premia suprimir en els panells editables de Internet Explorer / Outlook Express.
* S'ha afegit suport per més camps editables a l'Skype.
* Els VirtualBuffers només es carreguen quan el focus és sobre la finestra que necessita ser carregada. Això soluciona alguns problemes que s'esdevenien quan el panell de previsualització s'activava en Outlook Express.
* S'han afegit arguments de línia de comandaments a NVDA:
 * -m, --mínim: no reproduir sons d'inici/sortida i no mostrar la interfície en l'arrencada si està establert que així es faci. 
 * -q, --sortir: sortir de qualsevol altra instància en execució de NVDA i després sortir de NVDA.
 * -s, --stderr-file fileName: especificar on ha de col·locar NVDA errors i excepcions no capturades. 
 * -d, --debug-file fileName: especificar on ha de col·locar NVDA missatges de depuració.
 * -c, --config-file: especificar un fitxer de configuració alternatiu.  
 * -h, -ajuda: mostrar un missatge d'ajuda que llista tots els arguments de línia de comandament
* Corregit un error segons el qual els símbols de puntuació no es traduïen al llenguatge correcte quan s'usava un llenguatge diferent de l'anglès i quan estava activada la Verbalització dels caràcters escrits.
* Afegits fitxers amb el llenguatge eslovac gràcies a Peter Vagner 
* Afegit un diàleg de configuració de la memòria intermèdia virtual i un diàleg de Formatació de documents, per  Peter Vagner.
* Afegida la traducció francesa, gràcies a Michel Such 
* Afegit un script per a encendre i apagar els xiulets de la barra de progrés. Contribució de Peter Vagner.
* Fets més missatges per tal que NVDA sigui traduïble a d'altres idiomes. Això inclou descripcions de scripts quan s'està en l'ajut de teclat.  
* Afegit un diàleg de cerca als virtualBuffers (internet Explorer and Firefox). Prement  control+f sobre una pàgina, s'obre un quadre de diàleg en el qual es pot escriure algun text per buscar. Prement "retorn" se cercarà per aquest text i s'ubicarà el cursor del  virtualBuffer sobre aquesta línia. Si és prem F3 també cercarà la següent ocurrència del text.
* Quan s'activa "Verbalitza els caràcters escrits" s'haurien de verbalitzar més caràcters. Tècnicament s'haurien de verbalitzar els caràcters ASCII del 32 al 255  
* Canviat el nom d'alguns tipus de control per a una millor lectura. Text Editable és ara Editar, Esquema és ara Vista d'arbre i el Polsador és ara Botó.  
* Quan es navega al voltant dels elements d'una llista en una llista, o al voltant d' ítems en vista d'arbre el tipus de control (ítem de llista o ítem de vista d'arbre) ja no s'anuncia per incrementar la velocitat de navegació.
* L'anunci emergent (per indicar que un menú té un submenú) és ara anunciada com a submenú.
* Quan algun idioma faci servir CONTROL i ALT  (o ALT GR) per a entrar un caràcter especial, NVDA ara anunciarà aquests caràcters com si "Verbalitza els caràcters escrits" estès activat.  
* Solucionats alguns problemes amb la revisió de controls estàtics de text. 
* Afegida la traducció per al xinès tradicional, gràcies a Coscell Kao.
* Reestructurada una part important del codi NVDA, que hauria ara de solucionar diversos problemes amb la interfície d'usuari NVDA (incloent els diàlegs de configuració).  
* Afegit suport Sapi4 per NVDA. Normalment hi ha dos controladors Sapi4, un basat en un codi contribuït per Serotek Corporation i un altre que usa interfície ActiveVoice de ActiveVoice.com. Ambdós controladors estan en funcionament, per la qual cosa es pot veure quin treballa millor. 
* Ara quan s'intenti carregar una nova còpia de NVDA mentre s'estigui usant una còpia antiga, la còpia antiga es tancarà. Això soluciona un problema important que es donava quan l'ús simultani de diferents còpies de NVDA feia que el sistema fos molt poc usable.
* Canviat el títol de la interfície d'usuari NVDA des de Interfície NVDA a NVDA. 
* Corregit un error en Outlook Express segons el qual es generava un error quan es premia la tecla de retrocés al principi d'un missatge editable.  
* Rui Batista ha afegit un pedaç que afegeix un script per reportar l'estat actual de la bateria en ordinadors portàtils (insertar+maj+b).
* Afegit un controlador de sintetitzador anomenat Silence. Es tracta d'un controlador que no parla res, permetent que NVDA romangui totalment silenciós tot el temps. Eventualment això hauria de poder ser usat amb suport Braille quan en tinguem.  
* Afegida la configuració capitalPitchChange  per a sintetitzadors gràcies a J.J. Meddaugh
* Afegit pedaç de J.J. Meddaugh que fa commutar els informes d'objectes que hi ha sota el ratolí més que altres scripts de commutació (dient on/off més que canviant tota la declaració).
* Afegida traducció a l'espanyol (es). Contribució de Juan C. buo.
* Afegit fitxer per al llenguatge hongarès per part de Gczy.
* Afegit fitxer per al llenguatge portuguès per part de Rui Batista.
* Quan es canvia la veu en el menú Paràmetres de veu es mostren ara les barres de desplaçament de to, inflexió i volum d'acord amb el sintetitzador que es fa servir, més que forçant el sintetitzador a adaptar-se als vells valors. Això soluciona problemes que feien que sintetitzadors com Eloquence o Viavoice semblessin parlar molt més de pressa que altres sintetitzadors.
* S'ha corregit un error pel qual, quan s'estava en una finestra de consola DOS, s'aturava tota la parla o, fins i tot es penjava totalment NVDA.  
* Si hi ha suport per un llenguatge en particular, NVDA mostra ara de forma automàtica la seva interfície i anuncia els seus missatges en el llenguatge que Windows té configurat per defecte. Es pot triar manualment un determinat idioma  des del diàleg de Paràmetres d'interfície d'usuari.   
* S'ha afegit el script  'toggleReportDynamicContentChanges' (insert+5). Això permet commutar si el nou text o d'altres canvis dinàmics han de ser anunciats de forma immediata. Fins ara això només funcionava en la finestra de consola DOS.  
* S'ha afegit el script  'toggleCaretMovesReviewCursor' (insert+6). Això permet commutar si el cursor de revisió ha de ser immediatament reubicat quan es mou el cursor del sistema.  Això és útil en finestres de consola DOS quan s'intenta llegir informació quan la finestra s'està actualitzant.   
* S'ha afegit el script  'toggleFocusMovesNavigatorObject' (insert+7). Això permet commutar quan l'objecte de navegació ha de ser reubicat sobre l'objecte amb focus en el moment que canvia. 
* S'ha afegit alguna documentació traduïda a diferents llenguatges. Fins ara hi havia francès, espanyol i finlandès.  
* Eliminada alguna documentació de desenvolupador de la distribució binària de NVDA. Ara només es manté en la versió font.  
* Solucionat un possible error en Windows Live Messenger i MSN Messenger segons el qual la navegació amunt i avall per la llista de contactes causava errors.  
* Els nous missatges es mostren de forma automàtica en converses que facin servir Windows Live Messenger (només disponible per a versions en anglès)
* La finestra de l'historial d'una conversa en Windows Live Messenger pot ser ara llegida usant les tecles de cursor (només disponible per a versions en anglès) 
* S'ha afegit el script  'passNextKeyThrough' (insert+f2). Si es prem aquesta tecla, aleshores la següent tecla que es premi passarà a ser controlada per Windows. Això és útil si has de prémer una determinada tecla en una aplicació però NVDA fa servir aquesta tecla per alguna altra cosa.
* NVDA ja no es congela més d'un minut quan obre documents molt grans en MS Word.  
* Solucionat un error quan es sortia d'una taula en MS Word i després s'hi tornava. Això feia que les columnes/files no es llegissin, encara que es retornés exactament a la mateixa cel·la.  
* Quan s'iniciï NVDA amb un sintetitzador que no existeixi o que no funcioni, el sintetitzador Sapi5 intentarà carregar-se en el seu lloc i, si això no funciona, aleshores la parla romandrà en silenci.  
* La ràtio d'increment i disminució dels scripts no pot estar per damunt de 100 o per sota de 0.
* Si hi ha un error amb el llenguatge quan es tria dins del diàleg de Paràmetres de la Interfície d'Usuari, un missatge alerta del fet a l'usuari. 
* NVDA pregunta ara si ha de salvar la configuració i reiniciar si l'usuari acaba de canviar el llenguatge en el diàleg de Paràmetres de la Interfície d'Usuari.  Cal reiniciar NVDA per tal que el canvi de llenguatge tingui efecte totalment. 
* Si un sintetitzador no pot ser carregat, quan es tria des del diàleg "Sintetitzador", un missatge alerta l'usuari d'aquest fet.
* Quan es carrega un sintetitzador per primera vegada, NVDA deixa el sintetitzador que esculli la veu més adequada així com els paràmetres de velocitat i volum, més que forçar-lo a acceptar els valors predeterminats que NVDA creu correctes. Això soluciona un problema amb els sintetitzadors Sapi4 Eloquence i ViaVoice que  començaven a parlar massa ràpid la primera vegada.

