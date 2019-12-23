---
title: "Angebot anfragen"
date: 2018-01-11T16:03:33-05:00
draft: false
noTitle: true
---

<form id="regForm" action="/action_page.php">
  <h1>Anfrage:</h1>
  <!-- One "tab" for each step in the form: -->
  <div class="tab" for="sinfonima">
    <p>Schritt 1 von 3</p>
    <h2>Start:</h2>
    <div class="switch">
      <p class="form__answer">
        <input type="radio"  name="type" value="sinfonima" id="choice-sinfonima"/>
        <label for="choice-sinfonima" data-sinfonima >
          Akustische Instrumente
        </label>
      </p>
      <p class="form__answer">
        <input type="radio" name="type" value="imsound" id="choice-imsound" />
        <label for="choice-imsound" data-imsound >
          Elektronische Instrumente & Equipment
        </label>
      </p>
    </div>
    <label id="totalValue" class="hidden">
      Gesamtwert der Instrumente
      <input oninput="this.className = ''" name="totalValue" />
    </label>
  </div>
  <div class="tab">
    <p>Schritt 2 von 3</p>
    <h2>Persönliche Informationen:</h2>
    <label>
      Vorname
      <input oninput="this.className = ''" name="vorname" required autofocus/>
    </label>
    <label>
      Nachname
      <input oninput="this.className = ''" name="nachname" required />
    </label>
    <label>
      E-Mail
      <input oninput="this.className = ''" name="email" required />
    </label>
  </div>
  <div class="tab">
    <p>Schritt 3 von 3</p>
    <h2>Instrumente:</h2>
    <div class="instrument-list">
      <div class="single-instrument">
        <label>
          Instrument
          <input oninput="this.className = ''" name="instrument"  />
        </label>
        <fieldset class="switch">
          <label for="Neuwert">
            <input type="radio" name="valueType" value="Neuwert" />
            Neuwert
          </label>
          <label for="Zeitwert" >
            <input type="radio" name="valueType" value="Zeitwert" />
            Zeitwert
          </label>
        </fieldset>
        <label>
          Wert
          <input oninput="this.className = ''" name="value"  />
        </label>
      </div>
      <div class="single-instrument">
        <label>
          Instrument
          <input oninput="this.className = ''" name="instrument"  autofocus />
        </label>
        <div class="switch">
          <p class="form__answer">
            <input type="radio" name="match" id="match_1" value="neuwert" checked>
            <label for="match_1">
                Neuwert
            </label>
          </p>
          <p class="form__answer">
            <input type="radio" name="match" id="match_2" value="zeitwer">
            <label for="match_2">
              Zeitwert
            </label>
          </p>
        </div>
        <label>
          Wert
          <input oninput="this.className = ''" name="value"  />
        </label>
      </div>
    </div>
    <button type="button" data-name="addInstrument">Weiteres Instrument hinzufügen</button> 
  </div>
  
  <div style="overflow:auto;">
    <div style="float:right;">
      <button type="button" id="prevBtn" onclick="nextPrev(-1)">
        Previous
      </button>
      <button type="button" id="nextBtn" onclick="nextPrev(1)">Next</button>
    </div>
  </div>
  <!-- Circles which indicates the steps of the form: -->
  <!-- <div style="text-align:center;margin-top:40px;">
    <span class="step"></span>
    <span class="step"></span>
    <span class="step"></span>
    <span class="step"></span>
  </div> -->
</form>
