**📘 XML \+ XSLT: Transformació d’un catàleg de CDs**

**1\. 📄 Document XML**

**✔️ Definició**

XML (*eXtensible Markup Language*) és un llenguatge per **emmagatzemar i estructurar dades**.

**✔️ Estructura del document**

* **Declaració inicial**:   


\<?xml version="1.0" encoding="UTF-8"?\>

* **Associació amb XSLT**:   

\<?xml-stylesheet type="text/xsl" href="transforma.xsl"?\>

👉 Indica que el XML es transformarà amb un fitxer XSL.

**✔️ Element arrel**

\<CATALOG\>

Conté tots els CDs.

**✔️ Elements repetitius**

Cada CD està definit per:

\<CD\>  
  \<TITLE\>...\</TITLE\>  
  \<ARTIST\>...\</ARTIST\>  
  \<COUNTRY\>...\</COUNTRY\>  
  \<COMPANY\>...\</COMPANY\>  
  \<PRICE\>...\</PRICE\>  
  \<YEAR\>...\</YEAR\>  
\</CD\>

👉 És una **estructura jeràrquica**:

* CATALOG   
  * CD   
    * TITLE, ARTIST, etc. 

**✔️ Característiques importants**

* Dades estructurades i llegibles   
* Etiquetes definides per l’usuari   
* Permet múltiples registres (llista de CDs) 

**2\. 🎨 XSLT (Transformació)**

**✔️ Definició**

XSLT (*eXtensible Stylesheet Language Transformations*) serveix per:  
👉 Transformar XML en HTML (o altres formats)

**✔️ Estructura bàsica**

\<xsl:stylesheet version="1.0"  
xmlns:xsl="http://www.w3.org/1999/XSL/Transform"\>

👉 Defineix el document com a full d’estils XSLT.

**✔️ Template principal**

\<xsl:template match="/"\>

👉 S’executa sobre l’arrel del document XML.

**✔️ Generació d’HTML**

\<html\>  
\<body\>  
\<h2\>My CD Collection\</h2\>

👉 Es crea una pàgina web.

**✔️ Taula**

\<table border="1"\>  
\<tr bgcolor="\#9acd32"\>  
\<th\>Title\</th\>  
\<th\>Artist\</th\>  
\</tr\>

👉 Capçalera de la taula.

**✔️ Iteració (bucle)**

\<xsl:for-each select="CATALOG/CD"\>

👉 Recorre tots els elements \<CD\>.

**✔️ Ordenació**

\<xsl:sort select="ARTIST"/\>

👉 Ordena els CDs per artista (ordre alfabètic).

**✔️ Extracció de dades**

\<td\>\<xsl:value-of select="TITLE"/\>\</td\>  
\<td\>\<xsl:value-of select="ARTIST"/\>\</td\>

👉 Mostra els valors de cada CD.

**✔️ Resultat final**

* Es genera una **taula HTML**   
* Mostra:   
  * Títol   
  * Artista   
* Ordenada per artista 

**3\. 🔄 Flux de funcionament**

1. XML conté les dades   
2. XSLT defineix com mostrar-les   
3. El navegador:   
   * Llegeix XML   
   * Aplica XSLT   
   * Genera HTML visual 

**4\. 🧠 Conceptes clau (resum examen)**

* XML → dades   
* XSLT → transformació   
* \<xsl:for-each\> → iteració   
* \<xsl:sort\> → ordenació   
* \<xsl:value-of\> → obtenir valor   
* Output → HTML 

**5\. ⚠️ Detalls importants**

* Sense XSLT → XML es veu com a text   
* XSLT permet separar:   
  * Contingut (XML)   
  * Presentació (HTML)

