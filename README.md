# AFANDI-NEWS import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { LucideSearch } from "lucide-react";

const newsArticles = [
  {
    id: 1,
    title: "Pasar Forex Menguat di Awal Pekan",
    excerpt: "Indeks dolar AS mengalami kenaikan seiring dengan rilis data ekonomi terbaru...",
    image: "https://source.unsplash.com/600x400/?business,finance",
  },
  {
    id: 2,
    title: "Bitcoin Sentuh Level Tertinggi Bulan Ini",
    excerpt: "Harga Bitcoin kembali menunjukkan tren bullish dengan kenaikan signifikan...",
    image: "https://source.unsplash.com/600x400/?crypto,bitcoin",
  },
  {
    id: 3,
    title: "Strategi Trading Forex untuk Pemula",
    excerpt: "Mengenal strategi dasar dalam trading forex agar bisa meraih profit konsisten...",
    image: "https://source.unsplash.com/600x400/?trading,stocks",
  },
];

export default function AfandiNews() {
  return (
    <div className="max-w-4xl mx-auto p-4">
      <header className="flex justify-between items-center mb-6">
        <h1 className="text-2xl font-bold">AFANDI NEWS</h1>
        <div className="relative">
          <Input type="text" placeholder="Cari berita..." className="pr-10" />
          <LucideSearch className="absolute right-2 top-2 text-gray-500" size={20} />
        </div>
      </header>
      <div className="grid gap-4">
        {newsArticles.map((article) => (
          <Card key={article.id} className="flex overflow-hidden">
            <img src={article.image} alt={article.title} className="w-40 h-auto object-cover" />
            <CardContent className="p-4">
              <h2 className="text-lg font-semibold">{article.title}</h2>
              <p className="text-sm text-gray-600">{article.excerpt}</p>
              <Button className="mt-2">Baca Selengkapnya</Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
