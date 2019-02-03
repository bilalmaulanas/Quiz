<template>

  <div class="hello">
  <center>
  <div v-if="show">
    <h1>{{ msg }}</h1>
  <table><hr><center><p><b><i>Jawab soal berikut dengan benar</i></b></p></center><hr><br>
    <div v-for="soalsatu in soal1" v-bind:key="soalsatu.soal1">
      <tr>
           <td><b>{{ soalsatu.no }}.</b> {{ soalsatu.soal }}</td>
      </tr>
      <tr><div class="control">
            <td> &nbsp;&nbsp;&nbsp;&nbsp;<input type="radio" name="soal1" value="a" v-model="picked1">{{soalsatu.jaw_a}}
                 &nbsp;&nbsp;&nbsp;&nbsp;<input type="radio" name="soal1" value="b" v-model="picked1">{{soalsatu.jaw_b}}
                 &nbsp;&nbsp;&nbsp;&nbsp;<input type="radio" name="soal1" value="c" v-model="picked1">{{soalsatu.jaw_c}}
                 &nbsp;&nbsp;&nbsp;&nbsp;<input type="radio" name="soal1" value="d" v-model="picked1">{{soalsatu.jaw_d}}
                 &nbsp;&nbsp;&nbsp;&nbsp;<input type="radio" name="soal1" value="e" v-model="picked1">{{soalsatu.jaw_e}}
            </td></div>
      </tr><br><hr>
    </div><br>
    <div v-for="soalsatu in soal2" v-bind:key="soalsatu.soal2">
      <tr>
           <td><b>{{ soalsatu.no }}.</b> {{ soalsatu.soal }}</td>
      </tr>
      <tr><div class="control">
            <td>&nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal2" value="a" v-model="picked2">{{soalsatu.jaw_a}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal2" value="b" v-model="picked2">{{soalsatu.jaw_b}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal2" value="c" v-model="picked2">{{soalsatu.jaw_c}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal2" value="d" v-model="picked2">{{soalsatu.jaw_d}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal2" value="e" v-model="picked2">{{soalsatu.jaw_e}}
            </td></div>
      </tr><br><hr><br>
    </div>
    <div v-for="soalsatu in soal3" v-bind:key="soalsatu.soal3">
      <tr>
           <td><b>{{ soalsatu.no }}.</b> {{ soalsatu.soal }}</td>
      </tr>
      <tr><div class="control">
            <td>&nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal3" value="a" v-model="picked3">{{soalsatu.jaw_a}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal3" value="b" v-model="picked3">{{soalsatu.jaw_b}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal3" value="c" v-model="picked3">{{soalsatu.jaw_c}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal3" value="d" v-model="picked3">{{soalsatu.jaw_d}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal3" value="e" v-model="picked3">{{soalsatu.jaw_e}}
            </td></div>
      </tr><br><hr><br>
    </div>
     <div v-for="soalsatu in soal4" v-bind:key="soalsatu.soal4">
      <tr>
           <td><b>{{ soalsatu.no }}.</b> {{ soalsatu.soal }}</td>
      </tr>
      <tr><div class="control">
            <td>&nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal4" value="a" v-model="picked4">{{soalsatu.jaw_a}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal4" value="b" v-model="picked4">{{soalsatu.jaw_b}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal4" value="c" v-model="picked4">{{soalsatu.jaw_c}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal4" value="d" v-model="picked4">{{soalsatu.jaw_d}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal4" value="e" v-model="picked4">{{soalsatu.jaw_e}}
            </td></div>
      </tr><br><hr><br>
    </div>
    <div v-for="soalsatu in soal5" v-bind:key="soalsatu.soal5">
      <tr>
           <td><b>{{ soalsatu.no }}.</b> {{ soalsatu.soal }}</td>
      </tr>
      <tr><div class="control">
            <td>&nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal5" value="a" v-model="picked5">{{soalsatu.jaw_a}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal5" value="b" v-model="picked5">{{soalsatu.jaw_b}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal5" value="c" v-model="picked5">{{soalsatu.jaw_c}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal5" value="d" v-model="picked5">{{soalsatu.jaw_d}}
                &nbsp;&nbsp;&nbsp;&nbsp; <input type="radio" name="soal5" value="e" v-model="picked5">{{soalsatu.jaw_e}}
            </td></div>
      </tr><br><hr>
    </div>
    </table>
    </div>
    <div v-else><h1>Finish berhasil mengerjakan</h1>
                <h1>Nilai: {{ nilai() }}</h1>
                <h2>Jumlah benar : {{jumlah_benar() }}</h2>
                <h2>Jumlah salah : {{jumlah_salah() }}</h2></div>
    <button type="button" v-on:click="hideTitle">Submit Jawaban</button>
    <h1></h1>
    </center>
  </div>
</template>


<script>
export default {
  name: 'Bilal',
  data () {
    return {
      msg: 'Selamat Mengerjakan Kuis ini ! ',
      show:true,
      picked1:'',picked2:'',picked3:'',picked4:'',picked5:'',
      soal1:[
      {
        no:'1',
        soal:"Phobos dan Deimos adalah satelit yang dimiliki planet ....",
        jaw_a:"A. Merkurius",
        jaw_b:"B. Jupiter",
        jaw_c:"C. Bumi",
        jaw_d:"D. Saturnus",
        jaw_e:"E. Mars"
      }
      ],
      soal2:[
      {
        no:'2',
        soal:"Erosi yang menimbulkan pelepasan dan pelemparan partikel tanah akibat pukulan butir hujan secara langsung disebut erosi ....",
        jaw_a:"A. Parit",
        jaw_b:"B. Percikan",
        jaw_c:"C. Lembar",
        jaw_d:"D. Tebing",
        jaw_e:"E. Pasir"
      }
    ],
      soal3:[
      {
        no:'3',
        soal:"Perbandingan panjang dan lebar persegi panjang adalah 4 : 3. Jika kelilingnya 84 cm, luasnya adalah ....",
        jaw_a:"A. 234",
        jaw_b:"B. 324",
        jaw_c:"C. 432",
        jaw_d:"D. 452",
        jaw_e:"E. 224"
      }
    ],
      soal4:[
      {
        no:'4',
        soal:"Perjanjian yang dilakukan lebih dari dua negara, yaitu perjanjian ....",
        jaw_a:"A. Multilateral",
        jaw_b:"B. Bilateral",
        jaw_c:"C. Antarnegara",
        jaw_d:"D. Antarbangsa",
        jaw_e:"E. Internasional"
      }
    ],
      soal5:[
      {
        no:'5',
        soal:" Larangan berputus asa dari rahmat Allah terdapat dalam al Quran Surah ....",
        jaw_a:"A. Al-Bayyinah ; 35",
        jaw_b:"B. Al-jumu’ah ; 10",
        jaw_c:"C. Al-Baqarah ; 195",
        jaw_d:"D. Yusuf ; 87",
        jaw_e:"E. Al-Maaidah ; 2"
      }
    ]
    }
  },
  methods: {
    nilai: function(){
      var jaw_1, jaw_2, jaw_3, jaw_4, jaw_5;

      if(this.picked1 == 'e'){ jaw_1 = 20; }else{ jaw_1 = 0;}
      if(this.picked2 == 'b'){ jaw_2 = 20; }else{ jaw_2 = 0;}
      if(this.picked3 == 'c'){ jaw_3 = 20; }else{ jaw_3 = 0;}
      if(this.picked4 == 'a'){ jaw_4 = 20; }else{ jaw_4 = 0;}
      if(this.picked5 == 'd'){ jaw_5 = 20; }else{ jaw_5 = 0;}

      return jaw_1 + jaw_2 + jaw_3 + jaw_4 + jaw_5;

    },
    jumlah_benar: function(){
      return this.nilai() / 20;
    },
    jumlah_salah: function(){
      return 5 - this.jumlah_benar() ;
    },
    hideTitle(){
      this.show = !this.show
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
