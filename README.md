<h1 align="center"> Sentiment Analysis using Caikit and Hugging Face </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff">
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=000">

</div>

<h2 align="center"> Dokumentasi Sentiment Analysis using Caikit and Hugging Face </h2> 

berikut merupakan bentuk dari direktori yang akan dibuat:
<code>
⠠ ⠠ text-sentiment/                     # top-level package directory
⠠ ⠠ start_runtime.py                # a wrapper to start the Caikit runtime as a gRPC server. The runtime will load the model at startup
⠠ ⠠ client.py                       # client which calls the Caikit runtime to perform inference on the model it is serving to perform text sentiment analysis
⠠ ⠠ requirements.txt                # specifies library dependencies
⠠ ⠠ models/                         # a directory that contains the Caikit metadata of the model and any artifacts required to run the model
⠠ ⠠ ⠠ text_sentiment/config.yml   # metadata that defines the Caikit text sentiment model
⠠ ⠠ text_sentiment/                 # a directory that defines Caikit module(s) that can include algorithm(s) implementation that can train/run an AI model
⠠ ⠠ ⠠ config.yml                  # configuration for the module and model input and output
⠠ ⠠ ⠠ __init__.py                 # makes the data_model and runtime_model packages visible
⠠ ⠠ ⠠ data_model/                 # a directory that contains the data format of the Caikit module
⠠ ⠠ ⠠ ⠠ classification.py       # data class that represents the AI model attributes in code
⠠ ⠠ ⠠ ⠠ __init__.py             # makes the data model class visible in the project
⠠ ⠠ ⠠ runtime_model/              # a directory that contains the Caikit module of the model
⠠ ⠠ ⠠ ⠠ hf_module.py            # a class that bootstraps the AI model in Caikit so it can be served and used (infer/train)
⠠ ⠠ ⠠ ⠠ __init__.py             # makes the module class visible in the project
</code>

- tahap pertama: menginstal virtual environment
<code>pip install --user virtualenv</code>
- tahap kedua: update versi pip jika perlu
<code>python -m pip install --upgrade pip</code>
- tahap ketiga: membuat direktori yang diperlukan menggunakan mkdir dan cd
<code>mkdir *nama direktori yang ingin dibuat*</code>
<code>cd *nama direktori yang ingin dituju*</code>
- tahap keempat: mengisi direktori tersebut dengan file dan mengisi file tersebut dengan kode juga sesuai dengan contoh
- tahap kelima: membuat virtual environment dan mengaktivasinya
<code>virtualenv -p python3 env</code>
<code>source env/bin/activate</code>
- tahap keenam: menginstal semua dependency sesuai dengan keperluan yang ada di requirements.txt
<code>pip install -r requirements.txt</code>
- tahap ketujuh: mulai runtime server
<code>python start_runtime.py</code>
- tahap kedelapan: membuka terminal baru dan menjalankan client.py
<code>cd /home/project/text-sentiment/
source env/bin/activate
python client.py</code>

<h2 align="center"> Hasil Sentiment Analysis using Caikit and Hugging Face </h2> 
- <strong>Sentiment Analysis</strong> seperti namanya menganalisis sentimen atau perasaan pada teks input prompt. Dari prompt yang diberikan akan diberikan label negatif atau positif juga akan memberikan suatu nilai kepercayaan. Pada bagian ini akan membicarakan tentang output dari hasil eksekusi program analisis sentimen yang menggunakan model <a href="https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english">Hugging Face DistilBERT base uncased finetuned SST-2</a>.

- <strong>I am not feeling well today!</strong>
  diberikan label negatif karena pada kalimat memiliki kata "not" yang dilanjuti "feeling" sehingga dari prompt tersebut model memberikan label negatif.
  <br>
- <strong>Today is a nice sunny day</strong>
  diberikan label positif karena pada kalimat menggunakan kata "nice", yang dari katanya sendiri berarti "baik" sehingga menjadi faktor yang besar dalam keputusan model memberikan label positif.
  <br>
- <strong>My dog is really cute</strong>
  diberikan label positif karena pada kalimat menggunakan kata "cute", yang memiliki arti yang positif lalu karena kata sebelumnya "really" yang berarti sangat maka model memberikan label positif dengan nilai yang sangat tinggi.
  <br>
- <strong>I'm graduating today</strong>
  diberikan label positif karena pada kalimat menggunakan kata "graduating", mungkin termasuk salah satu kata yang masuk ke label positif saat model di training.
  <br>
- <strong>I like to game all night</strong>
  diberikan label positif karena pada kalimat menggunakan kata "like", menurut saya itu salah satu faktor besar mengapa model yang digunakan memberikan label positif, karena saat training model pasti telah menemukan kata tersebut yang tergolong label positif.
  <br>
- <strong>He called in sick to work</strong>
  diberikan label negatif karena pada kalimat menggunakan kata "sick", yang merupakan salah satu kata yang sering digunakan dan saat training model ada diberikan label "negatif" kepada kata "sick" yang berarti sakit.
