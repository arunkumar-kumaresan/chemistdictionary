<template>
  <v-container class="pa-10">
    <h2>Periodic Table</h2>
    <br>
    <div style="overflow-x:auto;">
      <table id="periodic-tab" align="center" width="100%">
        <tbody>
        <tr>
          <td class="element-empty unknown">
            <span class="caption">Group</span>
            <v-divider></v-divider>
            <span class="caption">Period</span>
          </td>
          <td class="element-empty unknown">
            <span>1</span>
          </td>
          <td class="element-empty unknown">
            <span>2</span>
          </td>
          <td class="element-empty unknown">
            <span>3</span>
          </td>
          <td class="element-empty unknown">
            <span>4</span>
          </td>
          <td class="element-empty unknown">
            <span>5</span>
          </td>
          <td class="element-empty unknown">
            <span>6</span>
          </td>
          <td class="element-empty unknown">
            <span>7</span>
          </td>
          <td class="element-empty unknown">
            <span>8</span>
          </td>
          <td class="element-empty unknown">
            <span>9</span>
          </td>
          <td class="element-empty unknown">
            <span>10</span>
          </td>
          <td class="element-empty unknown">
            <span>11</span>
          </td>
          <td class="element-empty unknown">
            <span>12</span>
          </td>
          <td class="element-empty unknown">
            <span>13</span>
          </td>
          <td class="element-empty unknown">
            <span>14</span>
          </td>
          <td class="element-empty unknown">
            <span>15</span>
          </td>
          <td class="element-empty unknown">
            <span>16</span>
          </td>
          <td class="element-empty unknown">
            <span>17</span>
          </td>
          <td class="element-empty unknown">
            <span>18</span>
          </td>
        </tr>
        <tr>
          <td class="element-empty unknown">
            <span>1</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Hydrogen</span>
            <span class="element-z">1</span>
            <span class="element-symbol">H</span>
          </td>
          <td class="element-empty" colspan="16"></td>
          <td class="element noblegas">
            <span class="element-name">Helium</span>
            <span class="element-z">2</span>
            <span class="element-symbol">He</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>2</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Lithium</span>
            <span class="element-z">3</span>
            <span class="element-symbol">Li</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Beryllium</span>
            <span class="element-z">4</span>
            <span class="element-symbol">Be</span>
          </td>
          <td class="element-empty" colspan="10"></td>
          <td class="element metalloid">
            <span class="element-name">Boron</span>
            <span class="element-z">5</span>
            <span class="element-symbol">B</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Carbon</span>
            <span class="element-z">6</span>
            <span class="element-symbol">C</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Nitrogen</span>
            <span class="element-z">7</span>
            <span class="element-symbol">N</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Oxygen</span>
            <span class="element-z">8</span>
            <span class="element-symbol">O</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Fluorine</span>
            <span class="element-z">9</span>
            <span class="element-symbol">F</span>
          </td>
          <td class="element noblegas">
            <span class="element-name">Neon</span>
            <span class="element-z">10</span>
            <span class="element-symbol">Ne</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>3</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Sodium</span>
            <span class="element-z">11</span>
            <span class="element-symbol">Na</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Magnesium</span>
            <span class="element-z">12</span>
            <span class="element-symbol">Mg</span>
          </td>
          <td class="element-empty" colspan="10"></td>
          <td class="element post-transition-metal">
            <span class="element-name">Aluminium</span>
            <span class="element-z">13</span>
            <span class="element-symbol">Al</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Silicon</span>
            <span class="element-z">14</span>
            <span class="element-symbol">Si</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Phosphorous</span>
            <span class="element-z">15</span>
            <span class="element-symbol">P</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Sulfur</span>
            <span class="element-z">16</span>
            <span class="element-symbol">S</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Chlorine</span>
            <span class="element-z">17</span>
            <span class="element-symbol">Cl</span>
          </td>
          <td class="element noblegas">
            <span class="element-name">Argon</span>
            <span class="element-z">18</span>
            <span class="element-symbol">Ar</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>4</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Pottasium</span>
            <span class="element-z">19</span>
            <span class="element-symbol">K</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Calcium</span>
            <span class="element-z">20</span>
            <span class="element-symbol">Ca</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Scandium</span>
            <span class="element-z">21</span>
            <span class="element-symbol">Sc</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Titanium</span>
            <span class="element-z">22</span>
            <span class="element-symbol">Ti</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Vanadium</span>
            <span class="element-z">23</span>
            <span class="element-symbol">V</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Chromium</span>
            <span class="element-z">24</span>
            <span class="element-symbol">Cr</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Manganese</span>
            <span class="element-z">25</span>
            <span class="element-symbol">Mg</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Iron</span>
            <span class="element-z">26</span>
            <span class="element-symbol">Fe</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Cobalt</span>
            <span class="element-z">27</span>
            <span class="element-symbol">Co</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Nickel</span>
            <span class="element-z">28</span>
            <span class="element-symbol">Ni</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Copper</span>
            <span class="element-z">29</span>
            <span class="element-symbol">Cu</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Zinc</span>
            <span class="element-z">30</span>
            <span class="element-symbol">Zn</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Gallium</span>
            <span class="element-z">31</span>
            <span class="element-symbol">Ga</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Germanium</span>
            <span class="element-z">32</span>
            <span class="element-symbol">Ge</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Arsenic</span>
            <span class="element-z">33</span>
            <span class="element-symbol">As</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Selenium</span>
            <span class="element-z">34</span>
            <span class="element-symbol">Se</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Bromine</span>
            <span class="element-z">35</span>
            <span class="element-symbol">Br</span>
          </td>
          <td class="element noblegas">
            <span class="element-name">Krypton</span>
            <span class="element-z">36</span>
            <span class="element-symbol">Kr</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>5</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Rubidium</span>
            <span class="element-z">37</span>
            <span class="element-symbol">Rb</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Strontium</span>
            <span class="element-z">38</span>
            <span class="element-symbol">Sr</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Yttrium</span>
            <span class="element-z">39</span>
            <span class="element-symbol">Y</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Zirconium</span>
            <span class="element-z">40</span>
            <span class="element-symbol">Zr</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Niobium</span>
            <span class="element-z">41</span>
            <span class="element-symbol">Nb</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Molybdenum</span>
            <span class="element-z">42</span>
            <span class="element-symbol">Mo</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Technetium</span>
            <span class="element-z">43</span>
            <span class="element-symbol">Tc</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Ruthenium</span>
            <span class="element-z">44</span>
            <span class="element-symbol">Ru</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Rhodium</span>
            <span class="element-z">45</span>
            <span class="element-symbol">Rh</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Palladium</span>
            <span class="element-z">46</span>
            <span class="element-symbol">Pd</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Silver</span>
            <span class="element-z">47</span>
            <span class="element-symbol">Ag</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Cadmium</span>
            <span class="element-z">48</span>
            <span class="element-symbol">Cd</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Indium</span>
            <span class="element-z">49</span>
            <span class="element-symbol">In</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Tin</span>
            <span class="element-z">50</span>
            <span class="element-symbol">Sn</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Antimony</span>
            <span class="element-z">51</span>
            <span class="element-symbol">Sb</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Tellurium</span>
            <span class="element-z">52</span>
            <span class="element-symbol">Te</span>
          </td>
          <td class="element reactive-nonmetal">
            <span class="element-name">Iodine</span>
            <span class="element-z">53</span>
            <span class="element-symbol">I</span>
          </td>
          <td class="element noblegas">
            <span class="element-name">Xenon</span>
            <span class="element-z">54</span>
            <span class="element-symbol">Xe</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>6</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Caesium</span>
            <span class="element-z">55</span>
            <span class="element-symbol">Cs</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Barium</span>
            <span class="element-z">56</span>
            <span class="element-symbol">Ba</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Lanthanum</span>
            <span class="element-z">57</span>
            <span class="element-symbol">La</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Hafnium</span>
            <span class="element-z">72</span>
            <span class="element-symbol">Hf</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Tantalum</span>
            <span class="element-z">73</span>
            <span class="element-symbol">Ta</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Tungsten</span>
            <span class="element-z">74</span>
            <span class="element-symbol">W</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Rhenium</span>
            <span class="element-z">75</span>
            <span class="element-symbol">Re</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Osmium</span>
            <span class="element-z">76</span>
            <span class="element-symbol">Os</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Iridium</span>
            <span class="element-z">77</span>
            <span class="element-symbol">Ir</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Platinum</span>
            <span class="element-z">78</span>
            <span class="element-symbol">Pt</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Gold</span>
            <span class="element-z">79</span>
            <span class="element-symbol">Au</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Mercury</span>
            <span class="element-z">80</span>
            <span class="element-symbol">Hg</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Thallium</span>
            <span class="element-z">81</span>
            <span class="element-symbol">Ti</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Lead</span>
            <span class="element-z">82</span>
            <span class="element-symbol">Pb</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Bismuth</span>
            <span class="element-z">83</span>
            <span class="element-symbol">Bi</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Polonium</span>
            <span class="element-z">84</span>
            <span class="element-symbol">Po</span>
          </td>
          <td class="element metalloid">
            <span class="element-name">Astatine</span>
            <span class="element-z">85</span>
            <span class="element-symbol">At</span>
          </td>
          <td class="element noblegas">
            <span class="element-name">Radon</span>
            <span class="element-z">86</span>
            <span class="element-symbol">Rn</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty unknown">
            <span>7</span>
          </td>
          <td class="element alkali-metal">
            <span class="element-name">Francium</span>
            <span class="element-z">87</span>
            <span class="element-symbol">Fr</span>
          </td>
          <td class="element alkali-earth-metal">
            <span class="element-name">Radium</span>
            <span class="element-z">88</span>
            <span class="element-symbol">Ra</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Actinium</span>
            <span class="element-z">89</span>
            <span class="element-symbol">Ac</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Rutherfordium</span>
            <span class="element-z">104</span>
            <span class="element-symbol">Rf</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Dubnium</span>
            <span class="element-z">105</span>
            <span class="element-symbol">Db</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Seaborgium</span>
            <span class="element-z">106</span>
            <span class="element-symbol">Sg</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Bohrium</span>
            <span class="element-z">107</span>
            <span class="element-symbol">Bh</span>
          </td>
          <td class="element transition-metal">
            <span class="element-name">Hassium</span>
            <span class="element-z">108</span>
            <span class="element-symbol">Hs</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Meitnerium</span>
            <span class="element-z">109</span>
            <span class="element-symbol">Mt</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Darmstadtium</span>
            <span class="element-z">110</span>
            <span class="element-symbol">Ds</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Roentgenium</span>
            <span class="element-z">111</span>
            <span class="element-symbol">Rg</span>
          </td>
          <td class="element post-transition-metal">
            <span class="element-name">Copernicium</span>
            <span class="element-z">112</span>
            <span class="element-symbol">Cn</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Nihonium</span>
            <span class="element-z">113</span>
            <span class="element-symbol">Nh</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Flerovium</span>
            <span class="element-z">114</span>
            <span class="element-symbol">Fl</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Moscovium</span>
            <span class="element-z">115</span>
            <span class="element-symbol">Mc</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Livermorium</span>
            <span class="element-z">116</span>
            <span class="element-symbol">Lv</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Tennessine</span>
            <span class="element-z">117</span>
            <span class="element-symbol">Ts</span>
          </td>
          <td class="element unknown">
            <span class="element-name">Oganesson</span>
            <span class="element-z">118</span>
            <span class="element-symbol">Og</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty" colspan="19"></td>
        </tr>

        <tr>
          <td class="element-empty" colspan="4"></td>
          <td class="element lanthanide">
            <span class="element-name">Cerium</span>
            <span class="element-z">58</span>
            <span class="element-symbol">Ce</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Praseodymium</span>
            <span class="element-z">59</span>
            <span class="element-symbol">Pr</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Neodymium</span>
            <span class="element-z">60</span>
            <span class="element-symbol">Nd</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Promethium</span>
            <span class="element-z">61</span>
            <span class="element-symbol">Pm</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Samarium</span>
            <span class="element-z">62</span>
            <span class="element-symbol">Sm</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Europium</span>
            <span class="element-z">63</span>
            <span class="element-symbol">Eu</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Gadolinium</span>
            <span class="element-z">64</span>
            <span class="element-symbol">Gd</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Terbium</span>
            <span class="element-z">65</span>
            <span class="element-symbol">Tb</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Dysprosium</span>
            <span class="element-z">66</span>
            <span class="element-symbol">Dy</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Holmium</span>
            <span class="element-z">67</span>
            <span class="element-symbol">Ho</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Erbium</span>
            <span class="element-z">68</span>
            <span class="element-symbol">Er</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Thulium</span>
            <span class="element-z">69</span>
            <span class="element-symbol">Tm</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Ytterbium</span>
            <span class="element-z">70</span>
            <span class="element-symbol">Yb</span>
          </td>
          <td class="element lanthanide">
            <span class="element-name">Lutetium</span>
            <span class="element-z">71</span>
            <span class="element-symbol">Lu</span>
          </td>
        </tr>

        <tr>
          <td class="element-empty" colspan="4"></td>
          <td class="element actinide">
            <span class="element-name">Thorium</span>
            <span class="element-z">90</span>
            <span class="element-symbol">Th</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Protactinium</span>
            <span class="element-z">91</span>
            <span class="element-symbol">Pa</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Uranium</span>
            <span class="element-z">92</span>
            <span class="element-symbol">U</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Neptunium</span>
            <span class="element-z">93</span>
            <span class="element-symbol">Np</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Plutonium</span>
            <span class="element-z">94</span>
            <span class="element-symbol">Pu</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Americium</span>
            <span class="element-z">95</span>
            <span class="element-symbol">Am</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Curium</span>
            <span class="element-z">96</span>
            <span class="element-symbol">Cm</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Berkelium</span>
            <span class="element-z">97</span>
            <span class="element-symbol">Bk</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Californium</span>
            <span class="element-z">98</span>
            <span class="element-symbol">Cf</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Einsteinium</span>
            <span class="element-z">99</span>
            <span class="element-symbol">Es</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Fermium</span>
            <span class="element-z">100</span>
            <span class="element-symbol">Fm</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Mendelevium</span>
            <span class="element-z">101</span>
            <span class="element-symbol">Md</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Nobelium</span>
            <span class="element-z">102</span>
            <span class="element-symbol">No</span>
          </td>
          <td class="element actinide">
            <span class="element-name">Lawrencium</span>
            <span class="element-z">103</span>
            <span class="element-symbol">Lr</span>
          </td>
        </tr>

        </tbody>
      </table>
    </div>
    <br>
    <br>
    <div style="overflow-x:auto;">
      <table>
        <tbody>
        <tr>
          <td class="element-data unknown" colspan="6">Metal</td>
          <td class="element-data metalloid" rowspan="2">Metalloid</td>
          <td class="element-data unknown" colspan="2">Nonmetal</td>
          <td class="element-data unknown" rowspan="2">Unknown chemical properties</td>
        </tr>
        <tr>
          <td class="element-data alkali-metal">Alkali metal</td>
          <td class="element-data alkali-earth-metal">Alkali earth metal</td>
          <td class="element-data lanthanide">Lanthanide</td>
          <td class="element-data actinide">Actinide</td>
          <td class="element-data transition-metal">Transition metal</td>
          <td class="element-data post-transition-metal">Post-transition metal</td>
          <td class="element-data reactive-nonmetal">Reactive nonmetal</td>
          <td class="element-data noblegas">Noble gas</td>
        </tr>
        </tbody>
      </table>
    </div>
  </v-container>
</template>

<script>
  export default {
    name: "PeriodicTable"
  }
</script>

<style>
  .element-data {
    text-align: center !important;
    vertical-align: middle;
    width: 120px;
    height: 30px;
  }

  .element {
    border-top: 1px solid;
    border-bottom: 1px solid;
    text-align: center !important;
    vertical-align: middle;
    width: 60px;
    height: 60px;
  }

  .element-empty {
    text-align: center !important;
    vertical-align: middle;
    width: 60px;
    height: 60px;
  }

  .element-name {
    display: block;
    font-size: 0.65em;
  }

  .element-z {
    display: block;
    font-size: 0.6em;
  }

  .element-symbol {
    display: block;
    font-size: 1em;
  }

  #periodic-tab {
    border-collapse: separate;
  }

  .reactive-nonmetal {
    background-color: #f0ff8f;
  }

  .noblegas {
    background-color: #c0ffff;
  }

  .alkali-metal {
    background-color: #ff6666;
  }

  .alkali-earth-metal {
    background-color: #ffdead;
  }

  .metalloid {
    background-color: #cccc99;
  }

  .transition-metal {
    background-color: #ffc0c0;
  }

  .post-transition-metal {
    background-color: #cccccc;
  }

  .unknown {
    background-color: #e8e8e8;
  }

  .lanthanide {
    background-color: #ffbfff;
  }

  .actinide {
    background-color: #ff99cc;
  }

  .element-table td {
    padding: 0.6em;
  }
</style>
