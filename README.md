<h1 align="center"> Sentiment Analysis using Caikit and Hugging Face </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff">
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=000">

</div>

<h2 align="center"> Dokumentasi Sentiment Analysis using Caikit and Hugging Face </h2> 

- <strong>Sentiment Analysis</strong> seperti namanya menganalisis sentimen atau perasaan pada teks input prompt. Dari prompt yang diberikan akan diberikan label negatif atau positif juga akan memberikan suatu nilai kepercayaan. Pada bagian ini akan membicarakan tentang output dari hasil eksekusi program analisis sentimen yang menggunakan model.

- <strong>I am not feeling well today!</strong>
<br>
  diberikan label negatif karena pada kalimat memiliki kata "not" yang dilanjuti "feeling" sehingga dari prompt tersebut model memberikan label negatif.

- <strong>Today is a nice sunny day</strong>
<br>
  diberikan label positif karena pada kalimat menggunakan kata "nice", yang dari katanya sendiri berarti "baik" sehingga menjadi faktor yang besar dalam keputusan model memberikan label positif.

- <strong>My dog is really cute</strong>
<br>
  diberikan label positif karena pada kalimat menggunakan kata "cute", yang memiliki arti yang positif lalu karena kata sebelumnya "really" yang berarti sangat maka model memberikan label positif dengan nilai yang sangat tinggi.

- <strong>I'm graduating today</strong>
<br>
  diberikan label positif karena pada kalimat menggunakan kata "graduating", mungkin termasuk salah satu kata yang masuk ke label positif saat model di training.

- <strong>I like to game all night</strong>
<br>
  diberikan label positif karena pada kalimat menggunakan kata "like", menurut saya itu salah satu faktor besar mengapa model yang digunakan memberikan label positif, karena saat training model pasti telah menemukan kata tersebut yang tergolong label positif.

- <strong>He called in sick to work</strong>
<br>
  diberikan label negatif karena pada kalimat menggunakan kata "sick", yang merupakan salah satu kata yang sering digunakan dan saat training model ada diberikan label "negatif" kepada kata "sick" yang berarti sakit.
