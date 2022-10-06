<template>
  <h1>Calculater</h1>
  <table>
    <thead>
      <tr>
        <th>Remuneración Mensual</th>
        <th>Gratificaciones</th>
        <th>Gratificaciones Extra. Ocasionales</th>
        <th>Total Mensual</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><input type="text" v-model="remEnero" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiEnero" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasEnero" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesEnero"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remFebrero" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiFebrero" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasFebrero" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesFebrero"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remMarzo" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiMarzo" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasMarzo" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesMarzo"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remAbril" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiAbril" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasAbril" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesAbril"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remMayo" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiMayo" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasMayo" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesMayo"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remJunio" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiJunio" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasJunio" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesJunio"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remJulio" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiJulio" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasJulio" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesJulio"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remAgosto" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiAgosto" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasAgosto" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesAgosto"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remSeptiembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiSeptiembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasSeptiembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesSeptiembre"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remOctubre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiOctubre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasOctubre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesOctubre"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remNoviembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiNoviembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasNoviembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesNoviembre"></td>
      </tr>
      <tr>
        <td><input type="text" v-model="remDiciembre" v-on:keyup="sumarRem"></td>
        <td><input type="text" v-model="gratiDiciembre" v-on:keyup="sumarGrati"></td>
        <td><input type="text" v-model="ocasDiciembre" v-on:keyup="sumarOcas"></td>
        <td><input type="text" v-model="totalMesDiciembre"></td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
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

</template>

<script setup>
  import { ref, onMounted } from 'vue';

  let remEnero = ref(5600.60)
  let remFebrero = ref(5600.60)
  let remMarzo = ref(5800.40)
  let remAbril = ref(5800.40)
  let remMayo = ref(5800.40)
  let remJunio = ref(5800.40)
  let remJulio = ref(5800.40)
  let remAgosto = ref(5800.40)
  let remSeptiembre = ref(5800.40)
  let remOctubre = ref(3750.30)
  let remNoviembre = ref(3750.30)
  let remDiciembre = ref(3750.30)
  let sumaTotalRem = ref(3750.30)

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


  let sumarRem = () => {
    sumaTotalRem.value = Number(remEnero.value)+Number(remFebrero.value)+Number(remMarzo.value)+Number(remAbril.value)+Number(remMayo.value)+Number(remJunio.value)+Number(remJulio.value)+Number(remAgosto.value)+Number(remSeptiembre.value)+Number(remOctubre.value)+Number(remNoviembre.value)+Number(remDiciembre.value)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarGrati = () => {
    sumaTotalGrati.value = Number(gratiEnero.value)+Number(gratiFebrero.value)+Number(gratiMarzo.value)+Number(gratiAbril.value)+Number(gratiMayo.value)+Number(gratiJunio.value)+Number(gratiJulio.value)+Number(gratiAgosto.value)+Number(gratiSeptiembre.value)+Number(gratiOctubre.value)+Number(gratiNoviembre.value)+Number(gratiDiciembre.value)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarOcas = () => {
    sumaTotalOcas.value = Number(ocasEnero.value)+Number(ocasFebrero.value)+Number(ocasMarzo.value)+Number(ocasAbril.value)+Number(ocasMayo.value)+Number(ocasJunio.value)+Number(ocasJulio.value)+Number(ocasAgosto.value)+Number(ocasSeptiembre.value)+Number(ocasOctubre.value)+Number(ocasNoviembre.value)+Number(ocasDiciembre.value)
    sumarTotalmeses()
    hallarImporteSujetoDesc()
    hallarImportePortasa()
    hallarImporteNetoPortasa()
  }

  let sumarTotalmeses = () => {
    totalMesEnero.value = Number(remEnero.value)+Number(gratiEnero.value)+Number(ocasEnero.value)
    totalMesFebrero.value = Number(remFebrero.value)+Number(gratiFebrero.value)+Number(ocasFebrero.value)
    totalMesMarzo.value = Number(remMarzo.value)+Number(gratiMarzo.value)+Number(ocasMarzo.value)
    totalMesAbril.value = Number(remAbril.value)+Number(gratiAbril.value)+Number(ocasAbril.value)
    totalMesMayo.value = Number(remMayo.value)+Number(gratiMayo.value)+Number(ocasMayo.value)
    totalMesJunio.value = Number(remJunio.value)+Number(gratiJunio.value)+Number(ocasJunio.value)
    totalMesJulio.value = Number(remJulio.value)+Number(gratiJulio.value)+Number(ocasJulio.value)
    totalMesAgosto.value = Number(remAgosto.value)+Number(gratiAgosto.value)+Number(ocasAgosto.value)
    totalMesSeptiembre.value = Number(remSeptiembre.value)+Number(gratiSeptiembre.value)+Number(ocasSeptiembre.value)
    totalMesOctubre.value = Number(remOctubre.value)+Number(gratiOctubre.value)+Number(ocasOctubre.value)
    totalMesNoviembre.value = Number(remNoviembre.value)+Number(gratiNoviembre.value)+Number(ocasNoviembre.value)
    totalMesDiciembre.value = Number(remDiciembre.value)+Number(gratiDiciembre.value)+Number(ocasDiciembre.value)
    sumaTotalMes.value = Number(totalMesEnero.value)+Number(totalMesFebrero.value)+Number(totalMesMarzo.value)+Number(totalMesAbril.value)+Number(totalMesMayo.value)+Number(totalMesJunio.value)+Number(totalMesJulio.value)+Number(totalMesAgosto.value)+Number(totalMesSeptiembre.value)+Number(totalMesOctubre.value)+Number(totalMesNoviembre.value)+Number(totalMesDiciembre.value)
  }

  let hallarImporteSujetoDesc = () => {
    if(sumaTotalMes.value>=deduccion){
      importeSujetoDesc.value = Number(sumaTotalMes.value) - Number(deduccion)
    }else {
      importeSujetoDesc.value = 0
    }
  }

  let hallarImportePortasa = () => {
    if (importeSujetoDesc.value <= (UIT*5)){
      importeNetoTasa01.value = Number(importeSujetoDesc.value)
      importeNetoTasa02.value = 0.00
      importeNetoTasa03.value = 0.00
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*5) && importeSujetoDesc.value <= (UIT*20)){
      importeNetoTasa01.value = UIT*5
      importeNetoTasa02.value = Number(importeSujetoDesc.value)-(UIT*5)
      importeNetoTasa03.value = 0.00
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*20) && importeSujetoDesc.value <= (UIT*35)){
      importeNetoTasa01.value = UIT*5
      importeNetoTasa02.value = UIT*15
      importeNetoTasa03.value = Number(importeSujetoDesc.value)-(UIT*20)
      importeNetoTasa04.value = 0.00
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*35) && importeSujetoDesc.value <= (UIT*45)){
      importeNetoTasa01.value = UIT*5
      importeNetoTasa02.value = UIT*15
      importeNetoTasa03.value = UIT*15
      importeNetoTasa04.value = Number(importeSujetoDesc.value)-(UIT*35)
      importeNetoTasa05.value = 0.00
    }else if (importeSujetoDesc.value > (UIT*45)){
      importeNetoTasa01.value = UIT*5
      importeNetoTasa02.value = UIT*15
      importeNetoTasa03.value = UIT*15
      importeNetoTasa04.value = UIT*10
      importeNetoTasa05.value = Number(importeSujetoDesc.value)-(UIT*45)
    }
    
  }

  let hallarImporteNetoPortasa = () => {
    ImpuestoPorTasa01.value = (Number(importeNetoTasa01.value) * 8)/100
    ImpuestoPorTasa02.value = (Number(importeNetoTasa02.value) * 14)/100
    ImpuestoPorTasa03.value = (Number(importeNetoTasa03.value) * 17)/100
    ImpuestoPorTasa04.value = (Number(importeNetoTasa04.value) * 20)/100
    ImpuestoPorTasa05.value = (Number(importeNetoTasa05.value) * 30)/100
    totalImpuestoRenta.value = Number(ImpuestoPorTasa01.value)+Number(ImpuestoPorTasa02.value)+Number(ImpuestoPorTasa03.value)+Number(ImpuestoPorTasa04.value)+Number(ImpuestoPorTasa05.value)
  }

  onMounted(()=>{
    sumarGrati()
  })

</script>

<style scoped>

</style>