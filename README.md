# kalkulator

<!DOCTYPE html>
<html>
<head>
    <title>Kalkulator</title>
</head>
<body>
    <h1>Kalkulator</h1>
    <form name="kalkulator">
        <input type="text" id="wynik" name="wynik" disabled>
        <br>
        <button type="button" class="cyfra" value="7">7</button>
        <button type="button" class="cyfra" value="8">8</button>
        <button type="button" class="cyfra" value="9">9</button>
        <button type="button" class="operator" value="+">+</button>
        <br>
        <button type="button" class="cyfra" value="4">4</button>
        <button type="button" class="cyfra" value="5">5</button>
        <button type="button" class="cyfra" value="6">6</button>
        <button type="button" class="operator" value="-">-</button>
        <br>
        <button type="button" class="cyfra" value="1">1</button>
        <button type="button" class="cyfra" value="2">2</button>
        <button type="button" class="cyfra" value="3">3</button>
        <button type="button" class="operator" value="*">*</button>
        <br>
        <button type="button" class="cyfra" value="0">0</button>
        <button type="button" class="operator" value="/">/</button>
        <button type="button" id="rownosc" value="=">=</button>
        <button type="button" id="czysc" value="C">C</button>
    </form>


<script>
let wynikPole = document.getElementById('wynik');
        let aktualnyWyraz = '';

        document.querySelectorAll('.cyfra').forEach(button => {
            button.addEventListener('click', () => {
                dodajDoWyrazu(button.value);
            });
        });

        document.querySelectorAll('.operator').forEach(button => {
            button.addEventListener('click', () => {
                dodajDoWyrazu(button.value);
            });
        });

        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        document.getElementById('rownosc').addEventListener('click', oblicz);
        document.getElementById('czysc').addEventListener('click', wyczysc);

        function dodajDoWyrazu(wartosc) {
            aktualnyWyraz += wartosc;
            wynikPole.value = aktualnyWyraz;
        }

        function wyczysc() {
            aktualnyWyraz = '';
            wynikPole.value = '';
        }

        function oblicz() {
            try {
                aktualnyWyraz = eval(aktualnyWyraz);
                wynikPole.value = aktualnyWyraz;
            } catch (e) {
                wynikPole.value = 'Błąd';
            }
        }
</script>

