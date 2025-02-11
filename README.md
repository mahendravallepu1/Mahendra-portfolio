import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { FaBehance, FaDribbble, FaInstagram } from "react-icons/fa";

const projects = [
  { title: "Brand Identity", image: "https://www.lucidadvertising.com/wp-content/uploads/2020/07/Brand_Dev-1.jpg" },
  { title: "Web Design", image: " https://www.sgstechnologies.net/sites/default/files/2021-08/future-webdesign.jpg" },
  { title: "Logo Creation", image: "https://www.letterlogos.com/wp-content/uploads/2023/10/logo-in-business-world.jpg" },
];

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-red-500 p-6">
      <motion.h1 className="text-4xl font-bold text-center mb-6 text-white" initial={{ opacity: 0 }} animate={{ opacity: 1 }}>
        Mahendra Vallepu
      </motion.h1>
      <motion.p className="text-center text-white mb-10" initial={{ opacity: 0 }} animate={{ opacity: 1 }}>
        Graphic Designer | Brand Creator | Visual Artist
      </motion.p>
      <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
        {projects.map((project, index) => (
          <motion.div key={index} whileHover={{ scale: 1.05 }}>
            <Card>
              <img src={project.image} alt={project.title} className="rounded-t-2xl w-full h-48 object-cover" />
              <CardContent>
                <h2 className="text-lg font-semibold">{project.title}</h2>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </div>
      <div className="text-center mt-10">
        <Button className="mr-4">Contact Me: +91 9182339902</Button>
        <a href="#" className="text-xl mx-2"><FaBehance /></a>
        <a href="#" className="text-xl mx-2"><FaDribbble /></a>
        <a href="#" className="text-xl mx-2"><FaInstagram /></a>
      </div>
    </div>
  );
}
