<template>
  <h1>Calculater</h1>
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Remuneración Mensual</th>
        <th>Gratificaciones</th>
        <th>Gratificaciones Extra. Ocasionales</th>
        <th>Total Mensual</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td></td>
        <td><input type="text" v-model="remEnero" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiEnero" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasEnero" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesEnero"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxfeb" v-model="checkedfeb" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remFebrero" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiFebrero" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasFebrero" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesFebrero"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxmar" v-model="checkedmar" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remMarzo" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiMarzo" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasMarzo" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesMarzo"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxabr" v-model="checkedabril" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remAbril" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiAbril" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasAbril" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesAbril"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxmay" v-model="checkedmay"  @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remMayo" v-on:keyup="sumarRem" @change="capturarEventoMay" checked></td>
        <td><input type="text" v-model="gratiMayo" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasMayo" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesMayo"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxjun" v-model="checkedjun" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remJunio" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiJunio" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasJunio" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesJunio"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxjul" v-model="checkedjul" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remJulio" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiJulio" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasJulio" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesJulio"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxago" v-model="checkedago" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remAgosto" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiAgosto" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasAgosto" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesAgosto"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxsept" v-model="checkedsept" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remSeptiembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiSeptiembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasSeptiembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesSeptiembre"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxoct" v-model="checkedoct" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remOctubre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiOctubre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasOctubre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesOctubre"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxnov" v-model="checkednov" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remNoviembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiNoviembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasNoviembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesNoviembre"></td>
      </tr>
      <tr>
        <td><input type="checkbox" id="checkboxdic" v-model="checkeddic" @change="capturarEventoCheck" checked></td>
        <td><input type="text" v-model="remDiciembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiDiciembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasDiciembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesDiciembre"></td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td></td>
        <td><span>{{sumaTotalRem}}</span></td>
        <td><span>{{sumaTotalGrati}}</span></td>
        <td><span>{{sumaTotalOcas}}</span></td>
        <td><span>{{sumaTotalMes}}</span></td>
      </tr>
    </tfoot>
  </table>

  <div>
    <ul>
      <li>UIT Periodo 2022: {{UIT}}</li>
      <li>Deducción / Exhoneración de 7 UIT (B) {{deduccion}}</li>
      <li>importe NETO {{importeSujetoDesc}}</li>
    </ul>
  </div>

  <table>
    <thead>
      <tr>
        <td>RANGOS DEDUCIBLES</td>
        <td>IMPORTE NETO ANUAL SUJETO A IRQC DISTRIB. POR TASA</td>
        <td>TASA DEDUCCIÓN</td>
        <td>IRQC ANUAL POR TASA</td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Hasta 5 UIT</th>
        <th>{{importeNetoTasa01}}</th>
        <th>8%</th>
        <th>{{ImpuestoPorTasa01}}</th>
      </tr>
      <tr>
        <th>Más de 5 UIT<br>hasta 20 UIT</th>
        <th>{{importeNetoTasa02}}</th>
        <th>14%</th>
        <th>{{ImpuestoPorTasa02}}</th>
      </tr>
      <tr>
        <th>Más de 20 UIT<br>hasta 35 UIT</th>
        <th>{{importeNetoTasa03}}</th>
        <th>17%</th>
        <th>{{ImpuestoPorTasa03}}</th>
      </tr>
      <tr>
        <th>Más de 35 UIT<br>hasta 45 UIT</th>
        <th>{{importeNetoTasa04}}</th>
        <th>20%</th>
        <th>{{ImpuestoPorTasa04}}</th>
      </tr>
      <tr>
        <th>Más de 45 UIT</th>
        <th>{{importeNetoTasa05}}</th>
        <th>30%</th>
        <th>{{ImpuestoPorTasa05}}</th>
      </tr>
      <tr>
        <th></th>
        <th></th>
        <th></th>
        <th>{{totalImpuestoRenta}}</th>
      </tr>
    </tbody>
  </table>

  <table>
    <thead>
      <tr>
        <td>Periodo</td>
        <td>Descuento Mensual de 5° Categoria</td>
        <td>Situacion</td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Enero</th>
        <th><input type="text" v-model="descEnero" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Febrero</th>
        <th><input type="text" v-model="descFebrero" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Marzo</th>
        <th><input type="text" v-model="descMarzo" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Abril</th>
        <th><input type="text" v-model="descAbril" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Mayo</th>
        <th><input type="text" v-model="descMayo" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Junio</th>
        <th><input type="text" v-model="descJunio" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Julio</th>
        <th><input type="text" v-model="descJulio" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Agosto</th>
        <th><input type="text" v-model="descAgosto" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Septiembre</th>
        <th><input type="text" v-model="descSeptiembre" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Octubre</th>
        <th><input type="text" v-model="descOctubre" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Noviembre</th>
        <th><input type="text" v-model="descNoviembre" v-on:keyup="sumarDesc"></th>
      </tr>
      <tr>
        <th>Diciembre</th>
        <th><input type="text" v-model="descDiciembre" v-on:keyup="sumarDesc"></th>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td>Total</td>
        <td><span> {{sumaTotalDescuento}} </span></td>
        <td></td>
      </tr>
    </tfoot>
  </table>

  <div>
    <ul>
      <li>Exceso</li>
      <li> {{totalImpuestoRenta-sumaTotalDescuento}} </li>
    </ul>
  </div>

</template>

<script setup>
  import { ref, onMounted } from 'vue';

  let remEnero = ref(0)
  let remFebrero = ref(0)
  let remMarzo = ref(0)
  let remAbril = ref(0)
  let remMayo = ref(0)
  let remJunio = ref(0)
  let remJulio = ref(0)
  let remAgosto = ref(0)
  let remSeptiembre = ref(0)
  let remOctubre = ref(0)
  let remNoviembre = ref(0)
  let remDiciembre = ref(0)
  let sumaTotalRem = ref(0)

  let gratiEnero = ref(400.00)
  let gratiFebrero = ref(0.00)
  let gratiMarzo = ref(0.00)
  let gratiAbril = ref(0.00)
  let gratiMayo = ref(0.00)
  let gratiJunio = ref(0.00)
  let gratiJulio = ref(300.00)
  let gratiAgosto = ref(0.00)
  let gratiSeptiembre = ref(0.00)
  let gratiOctubre = ref(0.00)
  let gratiNoviembre = ref(0.00)
  let gratiDiciembre = ref(300.00)
  let sumaTotalGrati = ref(0.00)

  let ocasEnero = ref(0.00)
  let ocasFebrero = ref(0.00)
  let ocasMarzo = ref(0.00)
  let ocasAbril = ref(0.00)
  let ocasMayo = ref(0.00)
  let ocasJunio = ref(0.00)
  let ocasJulio = ref(0.00)
  let ocasAgosto = ref(0.00)
  let ocasSeptiembre = ref(0.00)
  let ocasOctubre = ref(0.00)
  let ocasNoviembre = ref(0.00)
  let ocasDiciembre = ref(0.00)
  let sumaTotalOcas = ref(0.00)

  let totalMesEnero = ref(0.00)
  let totalMesFebrero = ref(0.00)
  let totalMesMarzo = ref(0.00)
  let totalMesAbril = ref(0.00)
  let totalMesMayo = ref(0.00)
  let totalMesJunio = ref(0.00)
  let totalMesJulio = ref(0.00)
  let totalMesAgosto = ref(0.00)
  let totalMesSeptiembre = ref(0.00)
  let totalMesOctubre = ref(0.00)
  let totalMesNoviembre = ref(0.00)
  let totalMesDiciembre = ref(0.00)
  let sumaTotalMes = ref(0.00)

  let importeNetoTasa01 = ref(0.00)
  let importeNetoTasa02 = ref(0.00)
  let importeNetoTasa03 = ref(0.00)
  let importeNetoTasa04 = ref(0.00)
  let importeNetoTasa05 = ref(0.00)

  const UIT = 4600
  let deduccion = Number(UIT*7)
  let importeSujetoDesc = ref(0.00)

  let ImpuestoPorTasa01 = ref(0.00)
  let ImpuestoPorTasa02 = ref(0.00)
  let ImpuestoPorTasa03 = ref(0.00)
  let ImpuestoPorTasa04 = ref(0.00)
  let ImpuestoPorTasa05 = ref(0.00)
  let totalImpuestoRenta = ref(0.00)

  let checkedfeb = ref(true)
  let checkedmar = ref(true)
  let checkedabril = ref(true)
  let checkedmay = ref(true)
  let checkedjun = ref(true)
  let checkedjul = ref(true)
  let checkedago = ref(true)
  let checkedsept = ref(true)
  let checkedoct = ref(true)
  let checkednov = ref(true)
  let checkeddic = ref(true)


  let sumarRem = () => {
    capturarEventoCheck()
    sumaTotalRem.value = (Number(remEnero.value)+Number(remFebrero.value)+Number(remMarzo.value)+Number(remAbril.value)+Number(remMayo.value)+Number(remJunio.value)+Number(remJulio.value)+Number(remAgosto.value)+Number(remSeptiembre.value)+Number(remOctubre.value)+Number(remNoviembre.value)+Number(remDiciembre.value)).toFixed(2)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarGrati = () => {
    sumaTotalGrati.value = (Number(gratiEnero.value)+Number(gratiFebrero.value)+Number(gratiMarzo.value)+Number(gratiAbril.value)+Number(gratiMayo.value)+Number(gratiJunio.value)+Number(gratiJulio.value)+Number(gratiAgosto.value)+Number(gratiSeptiembre.value)+Number(gratiOctubre.value)+Number(gratiNoviembre.value)+Number(gratiDiciembre.value)).toFixed(2)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarOcas = () => {
    sumaTotalOcas.value = (Number(ocasEnero.value)+Number(ocasFebrero.value)+Number(ocasMarzo.value)+Number(ocasAbril.value)+Number(ocasMayo.value)+Number(ocasJunio.value)+Number(ocasJulio.value)+Number(ocasAgosto.value)+Number(ocasSeptiembre.value)+Number(ocasOctubre.value)+Number(ocasNoviembre.value)+Number(ocasDiciembre.value)).toFixed(2)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarTotalmeses = () => {
    totalMesEnero.value = (Number(remEnero.value)+Number(gratiEnero.value)+Number(ocasEnero.value)).toFixed(2)
    totalMesFebrero.value = (Number(remFebrero.value)+Number(gratiFebrero.value)+Number(ocasFebrero.value)).toFixed(2)
    totalMesMarzo.value = (Number(remMarzo.value)+Number(gratiMarzo.value)+Number(ocasMarzo.value)).toFixed(2)
    totalMesAbril.value = (Number(remAbril.value)+Number(gratiAbril.value)+Number(ocasAbril.value)).toFixed(2)
    totalMesMayo.value = (Number(remMayo.value)+Number(gratiMayo.value)+Number(ocasMayo.value)).toFixed(2)
    totalMesJunio.value = (Number(remJunio.value)+Number(gratiJunio.value)+Number(ocasJunio.value)).toFixed(2)
    totalMesJulio.value = (Number(remJulio.value)+Number(gratiJulio.value)+Number(ocasJulio.value)).toFixed(2)
    totalMesAgosto.value = (Number(remAgosto.value)+Number(gratiAgosto.value)+Number(ocasAgosto.value)).toFixed(2)
    totalMesSeptiembre.value = (Number(remSeptiembre.value)+Number(gratiSeptiembre.value)+Number(ocasSeptiembre.value)).toFixed(2)
    totalMesOctubre.value = (Number(remOctubre.value)+Number(gratiOctubre.value)+Number(ocasOctubre.value)).toFixed(2)
    totalMesNoviembre.value = (Number(remNoviembre.value)+Number(gratiNoviembre.value)+Number(ocasNoviembre.value)).toFixed(2)
    totalMesDiciembre.value = (Number(remDiciembre.value)+Number(gratiDiciembre.value)+Number(ocasDiciembre.value)).toFixed(2)
    sumaTotalMes.value = (Number(totalMesEnero.value)+Number(totalMesFebrero.value)+Number(totalMesMarzo.value)+Number(totalMesAbril.value)+Number(totalMesMayo.value)+Number(totalMesJunio.value)+Number(totalMesJulio.value)+Number(totalMesAgosto.value)+Number(totalMesSeptiembre.value)+Number(totalMesOctubre.value)+Number(totalMesNoviembre.value)+Number(totalMesDiciembre.value)).toFixed(2)
  }

  let hallarImporteSujetoDesc = () => {
    if(sumaTotalMes.value>=deduccion){
      importeSujetoDesc.value = (Number(sumaTotalMes.value) - Number(deduccion)).toFixed(2)
    }else {
      importeSujetoDesc.value = 0
    }
  }

  let hallarImportePortasa = () => {
    if (importeSujetoDesc.value <= (UIT*5)){
      importeNetoTasa01.value = (Number(importeSujetoDesc.value)).toFixed(2)
      importeNetoTasa02.value = 0.00
      importeNetoTasa03.value = 0.00
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*5) && importeSujetoDesc.value <= (UIT*20)){
      importeNetoTasa01.value = (UIT*5).toFixed(2)
      importeNetoTasa02.value = (Number(importeSujetoDesc.value)-(UIT*5)).toFixed(2)
      importeNetoTasa03.value = 0.00
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*20) && importeSujetoDesc.value <= (UIT*35)){
      importeNetoTasa01.value = (UIT*5).toFixed(2)
      importeNetoTasa02.value = (UIT*15).toFixed(2)
      importeNetoTasa03.value = (Number(importeSujetoDesc.value)-(UIT*20)).toFixed(2)
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*35) && importeSujetoDesc.value <= (UIT*45)){
      importeNetoTasa01.value = (UIT*5).toFixed(2)
      importeNetoTasa02.value = (UIT*15).toFixed(2)
      importeNetoTasa03.value = (UIT*15).toFixed(2)
      importeNetoTasa04.value = (Number(importeSujetoDesc.value)-(UIT*35)).toFixed(2)
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*45)){
      importeNetoTasa01.value = (UIT*5).toFixed(2)
      importeNetoTasa02.value = (UIT*15).toFixed(2)
      importeNetoTasa03.value = (UIT*15).toFixed(2)
      importeNetoTasa04.value = (UIT*10).toFixed(2)
      importeNetoTasa05.value = (Number(importeSujetoDesc.value)-(UIT*45)).toFixed(2)
    }
    
  }

  let hallarImporteNetoPortasa = () => {
    ImpuestoPorTasa01.value = ((Number(importeNetoTasa01.value) * 8)/100).toFixed(2)
    ImpuestoPorTasa02.value = ((Number(importeNetoTasa02.value) * 14)/100).toFixed(2)
    ImpuestoPorTasa03.value = ((Number(importeNetoTasa03.value) * 17)/100).toFixed(2)
    ImpuestoPorTasa04.value = ((Number(importeNetoTasa04.value) * 20)/100).toFixed(2)
    ImpuestoPorTasa05.value = ((Number(importeNetoTasa05.value) * 30)/100).toFixed(2)
    totalImpuestoRenta.value = (Number(ImpuestoPorTasa01.value)+Number(ImpuestoPorTasa02.value)+Number(ImpuestoPorTasa03.value)+Number(ImpuestoPorTasa04.value)+Number(ImpuestoPorTasa05.value)).toFixed(2)
  }

  let capturarEventoCheck = () => {
    if(checkedfeb.value === true){remFebrero.value = remEnero.value}
    if(checkedmar.value === true){remMarzo.value = remFebrero.value}
    if(checkedabril.value === true){remAbril.value = remMarzo.value}
    if(checkedmay.value === true){remMayo.value = remAbril.value}
    if(checkedjun.value === true){remJunio.value = remMayo.value}
    if(checkedjul.value === true){remJulio.value = remJunio.value}
    if(checkedago.value === true){remAgosto.value = remJulio.value}
    if(checkedsept.value === true){remSeptiembre.value = remAgosto.value}
    if(checkedoct.value === true){remOctubre.value = remSeptiembre.value}
    if(checkednov.value === true){remNoviembre.value = remOctubre.value}
    if(checkeddic.value === true){remDiciembre.value = remNoviembre.value}
  }

  let sumaTotalDescuento = ref(0)
  let descEnero = ref(0)
  let descFebrero = ref(0)
  let descMarzo = ref(0)
  let descAbril = ref(0)
  let descMayo = ref(0)
  let descJunio = ref(0)
  let descJulio = ref(0)
  let descAgosto = ref(0)
  let descSeptiembre = ref(0)
  let descOctubre = ref(0)
  let descNoviembre = ref(0)
  let descDiciembre = ref(0)

  let sumarDesc = () => {
    //capturarEventoCheck()
    sumaTotalDescuento.value = (Number(descEnero.value)+Number(descFebrero.value)+Number(descMarzo.value)+Number(descAbril.value)+Number(descMayo.value)+Number(descJunio.value)+Number(descJulio.value)+Number(descAgosto.value)+Number(descSeptiembre.value)+Number(descOctubre.value)+Number(descNoviembre.value)+Number(descDiciembre.value)).toFixed(2)
    //sumarTotalmeses()
    //hallarImporteSujetoDesc()
    //hallarImportePortasa()
    //hallarImporteNetoPortasa()
  }
  

  onMounted(()=>{
    sumarGrati()
    capturarEventoCheck()
  })

</script>

<style scoped>

</style>