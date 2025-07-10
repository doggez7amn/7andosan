<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Traphouse Utmaningar</title>
  <style>
    html, body {
      height: 100%;
      margin: 0;
      background: #0f0f0f;
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      color: #fff;
    }

    .container {
      max-width: 500px;
      text-align: center;
      padding: 20px;
    }

    .question-box {
      margin-top: 30px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 30px;
      min-height: 120px;
      font-size: 1.3em;
      line-height: 1.4;
      transition: all 0.3s ease;
      box-shadow: 0 4px 20px rgba(0,0,0,0.4);
    }

    button {
      background: #ff0077;
      border: none;
      color: white;
      padding: 20px 40px;
      font-size: 1.5em;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 8px 20px rgba(255, 0, 119, 0.5);
    }

    button:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 30px rgba(255, 0, 119, 0.7);
    }

    @media (max-width: 600px) {
      button {
        padding: 15px 30px;
        font-size: 1.2em;
      }

      .question-box {
        font-size: 1.1em;
        padding: 20px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <button id="generateBtn">TRYCK HÄR</button>
    <div id="question" class="question-box">Här kommer frågorna upp…</div>
  </div>

  <script>
    const questions = [
      "Vem här vill du hångla med just nu?",
      "Berätta om din värsta sexupplevelse.",
      "Vem här skulle du helst ligga med om du måste välja?",
      "Visa ditt senaste DM till någon du flirtar med.",
      "Ta av ett klädesplagg.",
      "Drick tre klunkar och skicka en sexig selfie till någon.",
      "Kyss personen till höger om dig.",
      "Visa din senaste sökhistorik.",
      "Berätta om ditt största turn-on.",
      "Gör en lapdance på någon i 30 sekunder.",
      "Låt någon annan scrolla 10 bilder bakåt i ditt kameraalbum.",
      "Raka eller vaxa en valfri kroppsdel.",
      "Låt någon annan skriva en text till ditt senaste ragg.",
      "Ring ditt ex och säg 'Jag saknar dig'.",
      "Gör en sexy pose på golvet.",
      "Vem här tror du är bäst i sängen?",
      "Berätta en sexfantasi du vill testa.",
      "Ta en shot och visa ditt senaste ligg.",
      "Lägg upp en thirst trap-story nu.",
      "Ge någon en hickey.",
      "Låt någon annan välja vem du ska krama länge.",
      "Låt någon måla något på din kropp med läppstift.",
      "Vem här vill du helst duscha med?",
      "Ge någon en erotisk massage i 1 minut.",
      "Gör 'twerk' i 30 sekunder.",
      "Vem här tror du är sämst på att kyssa?",
      "Ge en footjob-simulering på en annans ben i 10 sek.",
      "Gör en fake orgasm-ljudshow.",
      "Beskriv ditt senaste ligg i detalj.",
      "Kyss någon på halsen.",
      "Välj någon som får ge dig en 'truth or dare'-fråga direkt.",
      "Gör en body shot på någon.",
      "Visa din senaste nudes (eller en random selfie om du vägrar, och ta dubbla shots).",
      "Smek någons hår i 30 sek.",
      "Flirta aggressivt med valfri person i 1 minut.",
      "Skicka en 'jag tänker på dig 😈' till någon du inte borde.",
      "Vem här skulle du vilja se naken?",
      "Beskriv din favoritställning.",
      "Ta av två plagg, eller drick 5 klunkar.",
      "Ge någon i rummet en 'dirty look' och håll den i 15 sek.",
      "Berätta om ett sexuellt misstag du gjort.",
      "Välj någon att gå in i ett annat rum och snacka 'dirty talk' med i 1 minut.",
      "Gör en slow-motion kyss på din hand.",
      "Vem här vill du spendera natten med?",
      "Berätta om din första orgasm.",
      "Skriv 'saknar att mysa med dig' till ditt senaste ligg.",
      "Gör ett 'strip tease'-move i 15 sekunder.",
      "Låt någon annan välja vad du ska ta av dig.",
      "Ge en komplimang till alla i rummet.",
      "Klia någons rygg sensuellt i 30 sek.",
      "Bita någon lätt på örat.",
      "Gör en stön-ljud-tävling med någon.",
      "Skicka 'vill du ligga?' till någon i din kontaktlista.",
      "Visa senaste bilden på din snap memories.",
      "Ge någon en kyss på kinden — med ögonkontakt hela tiden.",
      "Låt någon sätta läppstift på dig.",
      "Ge någon en 'dirty' komplimang.",
      "Berätta din hemligaste kink.",
      "Smaka på någons drink — sensuellt.",
      "Gör en catwalk i bara underkläder (eller så mycket du vågar).",
      "Drick så många klunkar som antalet personer i rummet.",
      "Vem här vill du helst väcka mitt i natten?",
      "Gör en 'bedroom eyes'-blick till alla.",
      "Skicka 'vill du ses ikväll?' till ett gammalt ragg.",
      "Beskriv vad du vill någon ska göra med dig just nu.",
      "Ta en shot för varje ex du haft.",
      "Vem här vill du slicka på?",
      "Gör en 'air grind' i 10 sek.",
      "Visa senaste 'röda hjärtat'-snap du skickade.",
      "Låt någon rita ett hjärta på din mage.",
      "Låt någon annan hålla dig i midjan i 20 sek.",
      "Gör en 'booty shake' till musik.",
      "Berätta när du var som kåtast.",
      "Vem här tror du är vildast i sängen?",
      "Låt någon flirta med dig öppet i 30 sek.",
      "Ge någon en smekning över låret.",
      "Berätta något du aldrig vågat säga till någon.",
      "Ge en 'förförande blick' till kameran (om ni filmar).",
      "Ta en selfie och skicka till din crush nu.",
      "Berätta vem du vill smaka på just nu.",
      "Säg en sak du älskar att få gjort mot dig i sängen.",
      "Låt någon viska något snuskigt i ditt öra.",
      "Ge någon en 'spank' på rumpan.",
      "Gör push-ups som om du ligger på någon.",
      "Berätta ditt bästa one-night stand-minne.",
      "Vem här skulle du byta sexliv med?",
      "Ge någon en kyss på pannan (extra intimt).",
      "Ring en kompis och säg 'jag är kåt, vad gör du?'",
      "Drick från någon annans mun (om alla är med på det!).",
      "Vem här vill du slicka vin/öl från kroppen på?",
      "Skriv 'tänker på dig naken' till någon du borde undvika.",
      "Vem här hade du helst stuckit hem med ikväll?",
      "Ta en shot och dra av ett plagg (eller valfritt straff).",
      "Berätta om en gång du blev påkommen.",
      "Gör en body roll till musik.",
      "Låt någon annan rufsa ditt hår ordentligt.",
      "Visa vad du tycker är bästa förspelet.",
      "Ge någon en kyss på näsan.",
      "Gör 'flirty face' framför alla.",
      "Beskriv din drömdate och avsluta med 'och sen kn*llar vi'.",
      "Välj någon att 'vårta' (nypa lätt).",
      "Skicka 'jag vill mer' till en random kontakt.",
      "Håll hand med någon i 1 minut.",
      "Välj någon att dansa sensuellt med.",
      "Berätta vad som får dig att tända direkt.",
      "Drick så många klunkar som antalet personer du legat med (eller max 5).",
      "Vem här vill du duscha med efter festen?",
      "Visa ditt 'dirty talk'-röstprov.",
      "Byt tröja med någon (eller låna något klädesplagg).",
      "Gör en kärleksförklaring till någon du inte är kär i.",
      "Låt någon skriva något snuskigt på din arm.",
      "Skriv 'jag saknar din kropp' till en valfri.",
      "Låt någon hålla om dig bakifrån i 20 sek.",
      "Säg 'fuck me daddy/mommy' till kameran eller någon.",
      "Gör en smekande rörelse på dig själv (över kläderna).",
      "Berätta vem som gett dig bästa sexet någonsin.",
      "Skriv 'vill du ses naken?' till en gammal flört.",
      "Drick en klunk för varje crush du haft senaste året.",
      "Låt någon välja en emoji du måste skicka till tre personer.",
      "Kyss en valfri kroppsdel på någon.",
      "Låt någon kalla dig 'bebis' i 1 minut.",
      "Tänd en låt och dansa solo — fullt ut.",
      "Låt någon hålla din hand på valfri plats i 20 sek.",
      "Visa en gammal nakenchatt (eller drick tre shots).",
      "Låt någon bestämma en 'förbjuden' snap du ska skicka.",
      "Gör 'doggy style'-pose på golvet.",
      "Låt någon dra fingrarna genom ditt hår långsamt.",
      "Visa din favoritlekställning (med kläder på).",
      "Berätta vad du helst vill höra i sängen.",
      "Ge en lång kram till någon och viska 'jag vill ha dig'.",
      "Berätta vem du tycker luktar godast här.",
      "Visa ditt senaste 'dirty meme' du sparat.",
      "Gör en 'sexy crawl' över golvet.",
      "Kyss någon på handen långsamt.",
      "Gör en fake strip-dans på 10 sek.",
      "Ge en 'lick tease' på en finger eller på någon annans arm.",
      "Beskriv din värsta hook-up.",
      "Gör en 'air kiss' till alla i rummet.",
      "Säg högt vad du tänkte på senast du onanerade.",
      "Gör ett 'kiss face' till kameran.",
      "Låt någon klappa dig på rumpan 5 gånger.",
      "Tvinga någon annan att ta en shot (eller dricka själv).",
      "Berätta vad du helst vill bli kallad i sängen.",
      "Skriv 'saknar när vi myste' till någon du ghostat.",
      "Låt någon dra dig nära och hålla kvar.",
      "Visa senaste snuskiga gif du skickade eller såg.",
      "Ge någon en 'nipple twist' (om tillåtet!).",
      "Gör ett 'simulerat ridmove' på en kudde.",
      "Berätta hur många du vill ligga med i rummet.",
      "Gör en 'fuckboy/girl' pose och ta bild."
    ];

    const button = document.getElementById("generateBtn");
    const questionDiv = document.getElementById("question");

    button.addEventListener("click", function () {
      const randomIndex = Math.floor(Math.random() * questions.length);
      questionDiv.innerText = questions[randomIndex];
    });
  </script>
</body>
</html>
