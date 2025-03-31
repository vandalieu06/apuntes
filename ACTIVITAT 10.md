# ACTIVITAT 10

Aquest codi el que es una funcio encarggeda de crear un taula a partir de un diseny predefinit per DefaultTableModel que està incorporat en les eines de java.swing.taula.* 

```java
public void createTable(){
    // Creem la taula amb um model predefinit amb el nom de les columnes que hi hauran
    modelTaula = new DefaultTableModel(
        new String[]{"Nom", "Email", "Tipus", "Curs/Departament", "Nota Mitjana/Assignatures"}, 0
    );
    taula = new JTable(modelTaula);
    JScrollPane scrollPane = new JScrollPane(taula);
    gestioFrame.add(scrollPane, BorderLayout.CENTER);
}
```
