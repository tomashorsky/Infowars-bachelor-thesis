
# InfoWars – Strategická hra o informační válce

InfoWars je vzdělávací strategická hra určená pro skautské prostředí, která se zaměřuje na informační válku, dezinformace a jejich dopady na společnost. Hra kombinuje principy zážitkové pedagogiky, týmovou spolupráci a strategické rozhodování s interaktivní webovou aplikací. Projekt vznikl v rámci mé bakalářské práce **Strategická hra pro skauty s interaktivní webovou aplikací** na FIT ČVUT.

## O hře

Hráči jsou rozděleni do týmů, které se snaží prosadit své názory a ovlivnit veřejné mínění v jednotlivých státech. K tomu využívají různé prostředky informační války, například dezinformační kampaně, manipulativní zprávy nebo deepfake obsah. Jejich rozhodnutí ovlivňují vývoj hry a situaci v jednotlivých státech. 

Hlavním cílem hry je umožnit účastníkům lépe pochopit principy informační války a uvědomit si, jak mohou informace a manipulace ovlivňovat společnost.

## Ukázky aplikace

<table>
  <tr>
    <td align="center" width="33%">
      <img src="docs/images/Obrazovka1.jpeg" height="300" alt="Rozhraní týmu">
    </td>
    <td align="center" width="33%">
      <img src="docs/images/obrazovka4.jpeg" height="300" alt="Manipulační nástroje">
    </td>
    <td align="center" width="33%">
      <img src="docs/images/obrazovka6.jpeg" height="300" alt="Přehled států">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Rozhraní týmu</b></td>
    <td align="center"><b>Manipulační nástroje</b></td>
    <td align="center"><b>Přehled států</b></td>
  </tr>
</table>

## Technologie

- **Backend:** Java 17, Spring Boot
- **Frontend:** Thymeleaf, Bootstrap
- **Databáze:** PostgreSQL
- **Build:** Maven
- **Kontejnerizace:** Docker
- **Testování:** Unit testy a uživatelské testování

## Testování a výsledky

Hra byla několikrát úspěšně odehrána v reálném skautském prostředí a vyzkoušelo si ji více než 40 účastníků.

Během vývoje proběhlo unit testování aplikace a následně také uživatelské testování při samotné hře.

Získaná zpětná vazba byla převážně pozitivní a potvrdila funkčnost aplikace i využitelnost hry ve skautském vzdělávání. Zároveň poskytla podněty pro další rozvoj.

## Lokální spuštění aplikace

### Požadavky

Pro spuštění aplikace je potřeba:

- Git
- Java JDK 17 nebo novější
- PostgreSQL databáze
- IDE pro vývoj (volitelné, například IntelliJ IDEA)

Projekt obsahuje Maven Wrapper, takže není nutné mít Maven samostatně nainstalovaný.

PostgreSQL lze spustit také pomocí Dockeru podle [oficiálního návodu](https://www.docker.com/blog/how-to-use-the-postgres-docker-official-image/).

### 1. Stažení projektu

Naklonujte repozitář z GitHubu:

```bash
git clone https://github.com/tomashorsky/Infowars-bachelor-thesis.git
cd Infowars-bachelor-thesis
```

### 2. Připojení k databázi

Před spuštěním aplikace je potřeba nakonfigurovat připojení k PostgreSQL databázi. Nastavení připojení upravte v souboru: `src/main/resources/application.properties`

Ujistěte se, že databáze běží a připojovací údaje odpovídají vašemu lokálnímu prostředí.

### 3. Sestavení a spuštění aplikace

Aplikaci lze spustit přímo z IDE nebo sestavit pomocí Maven Wrapperu.

Sestavení bez spuštění testů:

```bash
./mvnw clean package -DskipTests
```

Spuštění aplikace:

```bash
java -jar target/InfoWars-1.0.0.jar
```

Po úspěšném spuštění bude aplikace dostupná na adrese:

http://localhost:8080/admin/games

### 4. Spuštění testů

Při správně nakonfigurovaném testovacím prostředí lze testy spustit příkazem:

```bash
./mvnw test
```

## Nastavení herních proměnných

Výchozí nastavení hry se nachází v souboru:

`src/main/resources/application.yaml`

V tomto souboru lze upravovat například:
- Výchozí stav jednotlivých států
- Počáteční názory a hodnoty týmů
- Další parametry ovlivňující průběh hry

Projekt zahrnuje celý proces vývoje – od analýzy a návrhu hry přes implementaci webové aplikace až po testování v reálném prostředí.
