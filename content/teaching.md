---
title: "Teaching"
eyebrow: "Teaching"
description: "We teach Physical AI in the Space Domain, a 10 ECTS master's course where students build a working CubeSat prototype in SPOK, our LearnLab at IT:U."
layout: teaching
banner: "images/spok-banner.jpg"
# The old SPOK page now redirects here.
aliases: ["/spok-learn-lab/"]

# ── The course ───────────────────────────────────────────────
course:
  title: "Physical AI in the Space Domain"
  level: "Master's course"
  ects: "10 ECTS"
  split: "4 theory · 6 practical"
  text: >
    How do you sense the world from orbit, make sense of the data on board, and send the result back to Earth?
    In this course, students follow the full chain of a space system, from sensing to computation to transmission,
    and apply it to a real mission: designing and building a CubeSat prototype for Earth observation.
  # Optional: link to public course material (leave empty to hide the button)
  materials: ""

modules:
  # color = pastel of the matching research area (mint, lilac, peach, butter)
  - title: "Smart Sensing"
    color: peach
    icon: bolt
    text: "From electronics basics to real sensors in space."
    topics:
      - "Arduino: getting started, electricity basics, Ohm's law, series and parallel circuits"
      - "Raspberry Pi, Sense HAT, and AI Camera: environmental sensing and data logging"
      - "Analysis of real time-series and image data collected on the ISS"
  - title: "Edge AI Computing"
    color: mint
    icon: chip
    text: "Turning raw data into decisions, directly on the device."
    topics:
      - "Exploratory data analysis: cleaning, missing values, visualization"
      - "Introduction to deep learning"
      - "Training deep neural networks with PyTorch"
  - title: "Communication & Telemetry"
    color: lilac
    icon: wifi
    text: "Getting data off the satellite and down to the ground."
    topics:
      - "Serial communication with UART"
      - "Telemetry and data links between the satellite and a ground station"

project:
  title: "The LearnLab project: a CubeSat for Earth observation"
  text: >
    In the practical part, small interdisciplinary teams design and build their own CubeSat prototype.
    The Raspberry Pi 5 with the Sense HAT and AI Camera, as well as a custom-PCB-designed board with
    advanced communication protocols such as the Semtech SX1278 low-power sub-GHz radio transceiver,
    are examples of what students can build. The LearnLab is equipped for many other possibilities too;
    the only limit is their imagination. Students can focus on hardware, software, or the combination of both,
    while working through a Design Thinking process.
  phases:
    - name: "Empathize"
      text: "Understand users, their needs and the mission context."
    - name: "Define"
      text: "Turn insights into a clear problem statement."
    - name: "Ideate"
      text: "Generate and select solution ideas."
    - name: "Prototype"
      text: "Build a working CubeSat prototype."
    - name: "Test"
      text: "Evaluate the prototype and refine the solution."

# ── Where we teach ───────────────────────────────────────────
learnlab:
  name: "SPOK"
  subtitle: "IT:U LearnLab for the space domain"
  quote: >
    Tired of big lecture halls, endless theory, and waiting until the final semester to actually build something with technology?
    At IT:U, learning works differently. Your future classrooms are cutting-edge LearnLabs, where from day one,
    you work in small, interdisciplinary teams on real projects, guided by experts. This is where ideas turn into prototypes,
    and theory becomes something you can see, test, and experience.
  quote_source: "IT:U on its LearnLabs"
  location_title: "At Infineon in Linz"
  location_text: >
    SPOK is located inside Infineon's site in Linz, as part of the new cluster that IT:U has opened there.
    Students learn and build right next to a world leader in semiconductors and power systems.
  # Put the official logo file here (SVG or PNG). The page shows it automatically when the file exists.
  partner_logo: "images/partners/infineon-logo.svg"
  partner_name: "Infineon Technologies"
---

Our educational philosophy is founded on **project-based learning**: students acquire advanced technical skills and problem-solving capabilities by developing real-world projects, bridging the gap between academic theory and industrial application.
Students who want to go further can continue with an internship, a thesis, or a Ph.D. in our lab.
