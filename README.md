```jsx
import React from "react";

const profile = {
  name: "Khaled Alharbi",
  role: "Full-Stack Developer",
  age: 21,
  location: "United Arab Emirates",
  hobbies: ["Programming", "Football"],
  languages: ["Arabic", "English"],
  techStack: [
    "TypeScript",
    "React",
    "Next.js",
    "Tailwind",
    "Node.js",
    "NestJS",
    "MySQL",
    "Python",
  ],
};

const Section = ({ title, items }) => (
  <p>
    <strong>{title}:</strong> {items.join(" • ")}
  </p>
);

export default function AboutMe() {
  const { name, role, age, location, hobbies, languages, techStack } = profile;

  return (
    <div className="card">
      <h1>👨‍💻 About Me</h1>

      <p>
        Hello, I'm <strong>{name}</strong> — {role} ({age}) based in {location}.
      </p>

      <Section title="Hobbies" items={hobbies} />
      <Section title="Languages" items={languages} />
      <Section title="Tech Stack" items={techStack} />
    </div>
  );
}
```
