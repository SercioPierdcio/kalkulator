# kalkulator


        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
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

