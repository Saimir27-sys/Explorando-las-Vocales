import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { Download, BookOpen, Puzzle, Volume2 } from "lucide-react";

export default function BlogVocalesMontessori() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-yellow-50 to-blue-50 p-6">
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold mb-2">Explorando las Vocales</h1>
        <p className="text-lg">Aprendizaje activo inspirado en María Montessori</p>
      </header>

      <section className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        {vocales.map((vocal, index) => (
          <motion.div
            key={index}
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ delay: index * 0.1 }}
          >
            <Card className="rounded-2xl shadow-lg">
              <CardContent className="p-6 space-y-4">
                <h2 className="text-3xl font-bold">{vocal.letra}</h2>
                <p className="text-lg">Animal: {vocal.animal}</p>
                <p>Sonido inicial: {vocal.sonido}</p>
                <div className="flex gap-2 flex-wrap">
                  <Button variant="outline" className="rounded-2xl">
                    <BookOpen className="mr-2 h-4 w-4" /> Actividad Montessori
                  </Button>
                  <Button variant="outline" className="rounded-2xl">
                    <Puzzle className="mr-2 h-4 w-4" /> Juego Manipulativo
                  </Button>
                  <Button variant="outline" className="rounded-2xl">
                    <Volume2 className="mr-2 h-4 w-4" /> Escuchar Sonido
                  </Button>
                  <Button className="rounded-2xl">
                    <Download className="mr-2 h-4 w-4" /> Descargar Ficha
                  </Button>
                </div>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      <section className="mt-16">
        <h2 className="text-2xl font-bold mb-4">Estrategias Pedagógicas</h2>
        <div className="grid md:grid-cols-2 gap-6">
          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">María Montessori</h3>
              <p>
                Uso de letras de lija, bandejas sensoriales y asociación fonema‑grafema mediante material concreto.
                Se promueve la autonomía y la exploración libre.
              </p>
            </CardContent>
          </Card>
          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Aprendizaje Basado en el Juego</h3>
              <p>
                Relación vocal‑animal, dramatizaciones, clasificación de imágenes y construcción de mini‑libros.
              </p>
            </CardContent>
          </Card>
          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Enfoque Constructivista</h3>
              <p>
                Actividades donde el estudiante descubre palabras que inician con cada vocal mediante exploración guiada.
              </p>
            </CardContent>
          </Card>
          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Gamificación</h3>
              <p>
                Retos por vocal, insignias descargables y actividades interactivas digitales.
              </p>
            </CardContent>
          </Card>
        </div>
      </section>

      <footer className="mt-16 text-center text-sm">
        <p>Blog educativo creado para docentes y estudiantes | Proyecto de laboratorio pedagógico</p>
      </footer>
    </div>
  );
}

const vocales = [
  { letra: "A a", animal: "Abeja", sonido: "/a/" },
  { letra: "E e", animal: "Elefante", sonido: "/e/" },
  { letra: "I i", animal: "Iguana", sonido: "/i/" },
  { letra: "O o", animal: "Oso", sonido: "/o/" },
  { letra: "U u", animal: "Urraca", sonido: "/u/" },
];
# Explorando-las-Vocales
Explorando las Vocales – Aprendizaje Activo
