// App.jsx
import React from "react";

const prayers = [
  {
    title: "Modlitwa o pokój",
    text: "Panie, uczyń z nas narzędzia Twojego pokoju. Niech tam, gdzie jest nienawiść, siejemy miłość...",
  },
  {
    title: "Modlitwa o miłosierdzie",
    text: "Panie, spraw, abyśmy umieli przebaczać tak, jak Ty nam przebaczasz każdego dnia.",
  },
];

const facts = [
  "Prawdziwe imię papieża Franciszka to Jorge Mario Bergoglio.",
  "Jest pierwszym papieżem jezuitą i pierwszym z Ameryki Południowej.",
  "Został wybrany na papieża 13 marca 2013 roku.",
  "Wybrał imię 'Franciszek' na cześć św. Franciszka z Asyżu.",
  "Zrezygnował z tradycyjnej papieskiej rezydencji, mieszkając w Domu Świętej Marty.",
];

const quotes = [
  "„Nie lękajcie się marzyć o wielkich rzeczach.”",
  "„Kościół powinien być jak szpital polowy po bitwie.”",
  "„Niech nikt nie myśli, że nie jest ważny.”",
  "„Miłosierdzie to drugie imię miłości.”",
];

const gallery = [
  "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Pope_Francis_in_2015.jpg/800px-Pope_Francis_in_2015.jpg",
  "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Pope_Francis_South_Korea_2014.jpg/800px-Pope_Francis_South_Korea_2014.jpg",
  "https://upload.wikimedia.org/wikipedia/commons/thumb/1/1e/Pope_Francis_Prays.jpg/800px-Pope_Francis_Prays.jpg",
];

export default function App() {
  return (
    <div className="bg-gray-50 text-gray-800 font-sans">
      <header className="bg-white shadow p-6 text-center">
        <h1 className="text-4xl font-bold text-gray-700">Papież Franciszek</h1>
        <p className="text-gray-500 mt-2 text-lg">Życie, nauka i modlitwa</p>
      </header>

      <main className="p-6 max-w-5xl mx-auto space-y-12">
        <section>
          <h2 className="text-2xl font-semibold mb-2">Biografia</h2>
          <p className="leading-relaxed">
            Papież Franciszek, urodzony jako Jorge Mario Bergoglio 17 grudnia 1936 r. w Buenos Aires, jest
            pierwszym papieżem z Ameryki Południowej oraz jezuitą na Stolicy Piotrowej. Słynie z prostoty,
            bezpośredniości, troski o najbiedniejszych oraz dążenia do pokoju i ekologii.
          </p>
        </section>

        <section>
          <h2 className="text-2xl font-semibold mb-2">Ciekawostki</h2>
          <ul className="list-disc list-inside space-y-1">
            {facts.map((fact, idx) => (
              <li key={idx}>{fact}</li>
            ))}
          </ul>
        </section>

        <section>
          <h2 className="text-2xl font-semibold mb-2">Modlitwy papieża Franciszka</h2>
          <div className="space-y-4">
            {prayers.map((prayer, idx) => (
              <div key={idx} className="bg-white p-4 rounded shadow">
                <h3 className="font-bold text-lg">{prayer.title}</h3>
                <p className="mt-1 text-gray-700">{prayer.text}</p>
              </div>
            ))}
          </div>
        </section>

        <section>
          <h2 className="text-2xl font-semibold mb-2">Cytaty papieża Franciszka</h2>
          <ul className="space-y-2 text-gray-700 italic">
            {quotes.map((quote, idx) => (
              <li key={idx} className="pl-4 border-l-4 border-blue-300">{quote}</li>
            ))}
          </ul>
        </section>

        <section>
          <h2 className="text-2xl font-semibold mb-2">Galeria zdjęć</h2>
          <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
            {gallery.map((url, idx) => (
              <img key={idx} src={url} alt={`papież-${idx}`} className="rounded shadow" />
            ))}
          </div>
        </section>
      </main>

      <footer className="bg-white text-center p-4 text-sm text-gray-500 mt-10">
        &copy; 2025 Strona o papieżu Franciszku. Wykonanie: Marta Żabolicka VI TO
      </footer>
    </div>
  );
}
