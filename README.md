**Einleitung**
Das Marktumfeld, in dem sich Banken heute bewegen, ist gekennzeichnet durch Produkte und Leistungen, die zunehmend austauschbar werden. Im Umfeld von immer schnelleren Innovationszyklen, Fintech-Startups und Digitalisierung gilt eine gezielte und passgenaue Ansprache der Kunden heute als Erfolgsrezept, um neue Kunden zu gewinnen und die Kundenbindung zu erhöhen.

Die Eigenschaften, die Kunden charakterisieren und ihre Bedürfnisse sind allerdings vielschichtig und lassen sich nicht auf einfache Charakteristika, wie Kontostand, Umsatz, Alter oder Geschlecht reduzieren. Multivariate Analysemethoden, wie die Clusteranalyse, berücksichtigen diese Vielfältigkeit der Merkmale und helfen dabei, die Realität möglichst genau abzubilden.

Mit steigender Menge und Verfügbarkeit von Kundendaten gewinnen Data Mining-Techniken daher immer größere Bedeutung- sowohl in der Kundensegmentierung als auch im Costumer Relationship Management.

Forschungsfrage: Welche Kundentypen (Segmente) können wir aufgrund der Daten unterscheiden?

**Clustering Methode / Theorie**
Die Clusteranalyse gehört zu den Methoden des unüberwachten Lernens (unsupervised learning) und bezieht sich auf die Identifizierung von natürlichen Datengruppen (Partitionen) von Objekten (Clustern), die sich einander sehr ähnlich sind, sich aber stark von den Objekten in anderen Clustern unterscheiden. Die wahre Anzahl der Cluster ist dabei unbekannt.

Um die Ähnlichkeit der Objekte quantifizieren zu können, wird ein Distanzmaß dist (x,y) beziehungsweise ein Ähnlichkeitsmaß simil (x,y) verwendet. Einige Beispiel für Distanzfunktionen sind die Hamming-Distanz, Euklidische Distanz, Manhattan- und Maximum-Distanz (Cleve & Lämmel, 2020).

Die Anzahl der Datenpunkte und Attribute determinieren die Anpassungsgüte und Laufzeit des Clustering-Modells ebenso wie die Anzahl der Cluster, die Wahl der Ähnlichkeits- oder Distanzmaße sowie der Clustermethode (Müller & Lenz, 2013).

Clustering-Methoden (Han & Kamber, 2006):

Partitioning Methods (centroid based oder Schwerpunkt-basiertes Clustering)
Hierarchical Methods (Hierarchisches Clustering)
Density-based Methods (Dichte-basiertes Clustering)
Grid-Based Methods
Model-Based Methods
Constraint-based Methods
Clustering of High-Dimensional Data
Outlier Analysis
Zur Partitionierung unserer Kreditkarten- Daten wird der kMeans Algorithmus als eine der bekanntesten centroid-basierten Techniken zum Clustern großer Datensätze eingesetzt. Die K-Means-Clustermethode partitioniert den Datensatz auf Grundlage einer initial festgelegten Cluster-Anzahl, wobei die Wahl der richtigen Anzahl an Clustern entscheidenden Einfluss auf das Ergebnis hat. Wählt man eine zu geringe Anzahl von Clustern, werden zu unähnliche Objekte dem gleichen Cluster zugeordnet. Eine zu hohe Anzahl von Clustern führt zur Einordnung sehr ähnlicher Objekte in unterschiedliche Cluster.

Es stehen unterschiedliche Methoden zur Initialisierung der Startpartition und damit verbundenen Zahl an Clustern (k) zur Verfügung, wie die Elbow-Technik oder der Silhouette-Score.

Nachdem die initiale Anzahl an Centroiden, also Clusterzentren k gewählt wurde, wird jeder Datenpunkt (n) dem nächstgelegen Centroiden zugeordnet. Dieses Verfahren wird solange wiederholt, bis die jeweilige Distanzfunktion ein lokales Optimum erreicht und kein Datenpunkt mehr einem anderen Cluster zugeordnet werden kann.

**Kreditkarten-Datensatz**

Source: 			https://www.kaggle.com/arjunbhasin2013/ccdata
Licence: 			CC0: Public Domain
Dataset Owner: 		Arjun Bhasin
Expected update frequency	Not specified
Last updated			2018-03-02
Date created			2018-03-02
Current version		Version 1


Beschreibung:
Es soll eine Kundensegmentierung entwickelt werden, um eine Marketingstrategie festzulegen. 
Der Beispieldatensatz fasst das Nutzungsverhalten von etwa 9000 aktiven Kreditkarteninhabern während der letzten 6 Monate zusammen. Die Datei ist auf Kundenebene mit 18 Verhaltensvariablen.

CUSTID : Identification of Credit Card holder (Categorical)
BALANCE : Balance amount left in their account to make purchases (
BALANCEFREQUENCY : How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
PURCHASES : Amount of purchases made from account
ONEOFFPURCHASES : Maximum purchase amount done in one-go
INSTALLMENTSPURCHASES : Amount of purchase done in installment
CASHADVANCE : Cash in advance given by the user
PURCHASESFREQUENCY : How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
ONEOFFPURCHASESFREQUENCY : How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
PURCHASESINSTALLMENTSFREQUENCY : How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
CASHADVANCEFREQUENCY : How frequently the cash in advance being paid
CASHADVANCETRX : Number of Transactions made with "Cash in Advanced"
PURCHASESTRX : Number of purchase transactions made
CREDITLIMIT : Limit of Credit Card for user
PAYMENTS : Amount of Payment done by user
MINIMUM_PAYMENTS : Minimum amount of payments made by user
PRCFULLPAYMENT : Percent of full payment paid by user
TENURE : Tenure of credit card service for user
