You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "GRinfranet | IT Infrastructure Service | ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "clients.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | CLIENTS",
      "first_heading": "CLIENTS"
    }
  },
  {
    "path": "cloud-solutions.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | CLOUD SOLUTIONS",
      "first_heading": "CLOUD SOLUTIONS"
    }
  },
  {
    "path": "consulting.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | CONSULTING",
      "first_heading": "CONSULTING"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/595cb6ccb56826a802ed411cef875f0e.css",
    "context": {
      "path": "css/595cb6ccb56826a802ed411cef875f0e.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css",
    "context": {
      "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0008867c004e9ad708060acaa9a53dbb.webp",
    "context": {
      "refs": [
        {
          "alt": "Crimson",
          "title": ""
        },
        {
          "alt": "Crimson",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02c0fe542e291c57e9e1f0fd41ccf1df.webp",
    "context": {
      "refs": [
        {
          "alt": "ELECTROLAB",
          "title": ""
        },
        {
          "alt": "ELECTROLAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02d2206165f4e3c3a02f98c0ac68b4ff.webp",
    "context": {
      "refs": [
        {
          "alt": "Consulting",
          "title": ""
        },
        {
          "alt": "CONSULTING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0453acf1fefeb161666b94b4dcbc0b35.webp",
    "context": {
      "refs": [
        {
          "alt": "NETWORK SECURITY & SERVER STORAGE SOLUTIONS",
          "title": ""
        },
        {
          "alt": "Network Security",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0497d658bc1f5cac3eee248282a2117c.webp",
    "context": {
      "refs": [
        {
          "alt": "HIKVISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/04d58c70bcebbf29d538d127b7f9d204.webp",
    "context": {
      "refs": [
        {
          "alt": "ISAGRO",
          "title": ""
        },
        {
          "alt": "ISAGRO",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0777473433c32a3b2868a71380b9e3d7.webp",
    "context": {
      "refs": [
        {
          "alt": "INTER GOLD",
          "title": ""
        },
        {
          "alt": "INTER GOLD",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f7a18715a7f0c94b68c77f9ec43ae0f.webp",
    "context": {
      "refs": [
        {
          "alt": "Expo",
          "title": ""
        },
        {
          "alt": "Expo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0feedd5e62cb067afc6a7ff776a5760a.webp",
    "context": {
      "refs": [
        {
          "alt": "Shapoorji Pallonji",
          "title": ""
        },
        {
          "alt": "Shapoorji Pallonji",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/101a9ca5b1105951703bcec2786c3a9d.webp",
    "context": {
      "refs": [
        {
          "alt": "THE ADVANTAGE RAHEJA",
          "title": ""
        },
        {
          "alt": "THE ADVANTAGE RAHEJA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/111fcc6d973eadae1f7ec0662590aae7.webp",
    "context": {
      "refs": [
        {
          "alt": "THE DESIGN HOUSE",
          "title": ""
        },
        {
          "alt": "THE DESIGN HOUSE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/184c8f0d8b1515f54f4aac031ac8f759.webp",
    "context": {
      "refs": [
        {
          "alt": "in digital",
          "title": ""
        },
        {
          "alt": "in digital",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1948e346d94e2de6ef4e122d5fa5c651.webp",
    "context": {
      "refs": [
        {
          "alt": "SYSTIMAX",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fc832d4b1c7bddde039b1213a6ec69f.webp",
    "context": {
      "refs": [
        {
          "alt": "FREIGHT WINGS",
          "title": ""
        },
        {
          "alt": "FREIGHT WINGS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/20332f05f86c6b4c73fc8aa7df37063a.webp",
    "context": {
      "refs": [
        {
          "alt": "HCL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/207c817f68991579d0b6448eca7a0bbd.webp",
    "context": {
      "refs": [
        {
          "alt": "AMP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/20b46cd76e5ce953059602a45e90a123.webp",
    "context": {
      "refs": [
        {
          "alt": "AHUJA CONSTRUCTIONS",
          "title": ""
        },
        {
          "alt": "AHUJA CONSTRUCTIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f7f8c2f8c0bde1a6fac075b61ed4cb3.webp",
    "context": {
      "refs": [
        {
          "alt": "RJMDS",
          "title": ""
        },
        {
          "alt": "RJMDS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3359b8743b5bebd3efe33d783bc8b155.webp",
    "context": {
      "refs": [
        {
          "alt": "DIGILINK",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/358d0af53bd7125b839732db6e344dfe.webp",
    "context": {
      "refs": [
        {
          "alt": "PARTNERS",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39f48c78767fd5d1767932af84347042.webp",
    "context": {
      "refs": [
        {
          "alt": "NAMAHA",
          "title": ""
        },
        {
          "alt": "NAMAHA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b342ba027bcd9faa61ea121d29775d7.webp",
    "context": {
      "refs": [
        {
          "alt": "Nanavati",
          "title": ""
        },
        {
          "alt": "Nanavati",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d9143f1c1be2026a25d090fd9ab28fc.webp",
    "context": {
      "refs": [
        {
          "alt": "IP/DVR surveillance cameras",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41a7fac3adcd4abf72d868ea2d2fc21d.webp",
    "context": {
      "refs": [
        {
          "alt": "Nirlon",
          "title": ""
        },
        {
          "alt": "Nirlon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/453a256f0189b5a25c3bbec36e295ac8.webp",
    "context": {
      "refs": [
        {
          "alt": "United India",
          "title": ""
        },
        {
          "alt": "United India",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e935a54fd378fc8c90d6817243bdb8e.webp",
    "context": {
      "refs": [
        {
          "alt": "kores",
          "title": ""
        },
        {
          "alt": "kores",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f4b459ed7b558b4d59d11596f09dc48.webp",
    "context": {
      "refs": [
        {
          "alt": "Asian Star",
          "title": ""
        },
        {
          "alt": "Asian Star",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/508864d2b2a6443e7c5c6b0d4d69dd6f.webp",
    "context": {
      "refs": [
        {
          "alt": "Godrej agrovet",
          "title": ""
        },
        {
          "alt": "Godrej agrovet",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/557cbc9af0fcfe8c32b41b4db7581ba4.webp",
    "context": {
      "refs": [
        {
          "alt": "APC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57067d7f5c2e724a4b1f156ae3513eda.webp",
    "context": {
      "refs": [
        {
          "alt": "ReachLocal",
          "title": ""
        },
        {
          "alt": "ReachLocal",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59c87503d5342a30c1d21058714a202d.webp",
    "context": {
      "refs": [
        {
          "alt": "D-Link",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bcaeb74b55be9956e8414e68352489b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5c19968d6ae535e2ac4ad10f6b71a3b9.webp",
    "context": {
      "refs": [
        {
          "alt": "lenovo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5fe0eb8106ecc61dd33b02d5fa67737b.webp",
    "context": {
      "refs": [
        {
          "alt": "Evonik",
          "title": ""
        },
        {
          "alt": "Evonik",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/606500ced36cc6f4446e43460008df55.webp",
    "context": {
      "refs": [
        {
          "alt": "INDIAN INSTITUTE OF TECHNOLOGY BOMBAY",
          "title": ""
        },
        {
          "alt": "INDIAN INSTITUTE OF TECHNOLOGY BOMBAY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62d829fbf8140da62d0b5ed78cf9c289.webp",
    "context": {
      "refs": [
        {
          "alt": "Cyberoam",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65049f97d74e3790f26453710f389f53.webp",
    "context": {
      "refs": [
        {
          "alt": "ASHIKA",
          "title": ""
        },
        {
          "alt": "ASHIKA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6563e12c3bf18f067837f6d434f2a422.webp",
    "context": {
      "refs": [
        {
          "alt": "CREDR",
          "title": ""
        },
        {
          "alt": "CREDR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/674b9bc1691750fef42ab1a9a189ce2d.webp",
    "context": {
      "refs": [
        {
          "alt": "Pepe Jeans",
          "title": ""
        },
        {
          "alt": "Pepe Jeans",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dc643c4b91ccf8f1d31517945e4fe4f.webp",
    "context": {
      "refs": [
        {
          "alt": "FORTINET",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70a968f83f069319bb30e17daa039caf.webp",
    "context": {
      "refs": [
        {
          "alt": "faith is in the name",
          "title": ""
        },
        {
          "alt": "faith is in the name",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72323ffe83fb592ea790db34c9600a66.webp",
    "context": {
      "refs": [
        {
          "alt": "KASPERSKY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72abfb129be87eff00e809ce1191b8d8.webp",
    "context": {
      "refs": [
        {
          "alt": "Hiranandani",
          "title": ""
        },
        {
          "alt": "Hiranandani",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79a417e6786b1d522dcb700e2edf0f92.webp",
    "context": {
      "refs": [
        {
          "alt": "DANI",
          "title": ""
        },
        {
          "alt": "DANI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a06925025216237afc9d5da8fde7879.webp",
    "context": {
      "refs": [
        {
          "alt": "TRUST GROUP",
          "title": ""
        },
        {
          "alt": "TRUST GROUP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b4ecac988a1e78f5ba0aaf715b6a9b4.webp",
    "context": {
      "refs": [
        {
          "alt": "Dropbox",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b9e2c6db5c520900ef93094a93bec65.webp",
    "context": {
      "refs": [
        {
          "alt": "routemobile",
          "title": ""
        },
        {
          "alt": "routemobile",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c2474fbd37a4aa3e0bb85907932931a.webp",
    "context": {
      "refs": [
        {
          "alt": "UBM",
          "title": ""
        },
        {
          "alt": "UBM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7da8a95dc7e1d072b1ef21580b1f75c1.webp",
    "context": {
      "refs": [
        {
          "alt": "molex",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/830c11d5655b52e55835bc7a64f1fac8.webp",
    "context": {
      "refs": [
        {
          "alt": "IT INFRASTRUCTURE SOLUTIONS",
          "title": ""
        },
        {
          "alt": "IT Infrastructure Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/861f2daed1ed9c3192540bc805886f61.webp",
    "context": {
      "refs": [
        {
          "alt": "HOUSE OF PATELS",
          "title": ""
        },
        {
          "alt": "HOUSE OF PATELS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f2d60fc0fcb990771c79153d7881ac7.webp",
    "context": {
      "refs": [
        {
          "alt": "EKTA world",
          "title": ""
        },
        {
          "alt": "EKTA world",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9be3dabcbc7baaeea23cfb1489615feb.webp",
    "context": {
      "refs": [
        {
          "alt": "Arun Thikrul",
          "title": ""
        },
        {
          "alt": "Vilas Talkar",
          "title": ""
        },
        {
          "alt": "Vishvanath More",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f2132d85ebae86c028feae4a743c84b.webp",
    "context": {
      "refs": [
        {
          "alt": "Expeditors",
          "title": ""
        },
        {
          "alt": "Expeditors",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ff84d9efc5a216b66b103cafce908a5.webp",
    "context": {
      "refs": [
        {
          "alt": "Surveillance",
          "title": ""
        },
        {
          "alt": "IP Video",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2259dea5fe08627287a1be70ae3174f.webp",
    "context": {
      "refs": [
        {
          "alt": "SHEETAL GROUP",
          "title": ""
        },
        {
          "alt": "SHEETAL GROUP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a23bf2847662770bcbb91e1494f2ec51.webp",
    "context": {
      "refs": [
        {
          "alt": "SMS GupShup",
          "title": ""
        },
        {
          "alt": "SMS GupShup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad2a05cacf1c42e08f450d67a5687a02.webp",
    "context": {
      "refs": [
        {
          "alt": "DDECOR",
          "title": ""
        },
        {
          "alt": "DDECOR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae76ffb40dbd2de8dc2202376bdf13cf.webp",
    "context": {
      "refs": [
        {
          "alt": "Cloud Solutions",
          "title": ""
        },
        {
          "alt": "CLOUD SOLUTIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2d2c0040b409f6efe43d8574b832ba7.webp",
    "context": {
      "refs": [
        {
          "alt": "commoditiescontrol",
          "title": ""
        },
        {
          "alt": "commoditiescontrol",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3b46ff5da19b804ec27eff94a83f807.webp",
    "context": {
      "refs": [
        {
          "alt": "hp",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6077020d66f4517dde1826becf76946.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b69a4cfd7145b190f9418275a798f3d8.webp",
    "context": {
      "refs": [
        {
          "alt": "Outsourcing",
          "title": ""
        },
        {
          "alt": "OUTSOURCING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6c2dfb01c4a142e92c62cef17745d12.webp",
    "context": {
      "refs": [
        {
          "alt": "rolta",
          "title": ""
        },
        {
          "alt": "rolta",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b75eb00012de5d8766ca715a58adcc00.webp",
    "context": {
      "refs": [
        {
          "alt": "UPS Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9c91e8ad662e2636d47f01bfdccca96.webp",
    "context": {
      "refs": [
        {
          "alt": "seventyneves",
          "title": ""
        },
        {
          "alt": "seventyseven",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4afa340d61d1f1fc948c2e364625578.webp",
    "context": {
      "refs": [
        {
          "alt": "power grid",
          "title": ""
        },
        {
          "alt": "power grid",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4ba7c422311f603e4dfd9989a05d582.webp",
    "context": {
      "refs": [
        {
          "alt": "KP SANGHVI",
          "title": ""
        },
        {
          "alt": "KP SANGHVI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c587d34f74dc22080b16f2ddba6ae8b5.webp",
    "context": {
      "refs": [
        {
          "alt": "PRADEEP METALS LTD",
          "title": ""
        },
        {
          "alt": "PRADEEP METALS LTD",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c64a4709ddb46259329090f66de0c8d6.webp",
    "context": {
      "refs": [
        {
          "alt": "NAFA",
          "title": ""
        },
        {
          "alt": "NAFA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6da156d95a4e38dc26c29a55837a850.webp",
    "context": {
      "refs": [
        {
          "alt": "JUNIPER",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c93ff2b837da105da095d15c48d42c87.webp",
    "context": {
      "refs": [
        {
          "alt": "XcellHost",
          "title": ""
        },
        {
          "alt": "XcellHost",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9c6c5b6125009c130d8e6102b8e7e03.webp",
    "context": {
      "refs": [
        {
          "alt": "VALRACK",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9d43fab07b72a2121c9df1a9497900d.webp",
    "context": {
      "refs": [
        {
          "alt": "Lan Revamping",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/caa73d2144ec5fae0d899c6d4b3986ce.webp",
    "context": {
      "refs": [
        {
          "alt": "Hinduja hospital",
          "title": ""
        },
        {
          "alt": "Hinduja hospital",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbeafe0004eb9f67b53997565f32b22d.webp",
    "context": {
      "refs": [
        {
          "alt": "Lubrizol",
          "title": ""
        },
        {
          "alt": "Lubrizol",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf41ed7d5746b579ad0d0bb2caf2b300.webp",
    "context": {
      "refs": [
        {
          "alt": "BARISTA",
          "title": ""
        },
        {
          "alt": "BARISTA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfc4a63b55a7a7312fc03fd0fe6d8bc9.webp",
    "context": {
      "refs": [
        {
          "alt": "CISCO",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d002209cffd651854931c0fadfca9f81.webp",
    "context": {
      "refs": [
        {
          "alt": "SHRENUJ",
          "title": ""
        },
        {
          "alt": "SHRENUJ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d054b034436bd2bb0c74225538a3250a.webp",
    "context": {
      "refs": [
        {
          "alt": "envirocare lags",
          "title": ""
        },
        {
          "alt": "envirocare lags",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1bf3d16207d601ccc1fea6d5643c34d.webp",
    "context": {
      "refs": [
        {
          "alt": "NETGEAR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2b67ab6052428152abc398f77164e16.webp",
    "context": {
      "refs": [
        {
          "alt": "DELL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d347013293217f3d6eb22768c579a9ad.webp",
    "context": {
      "refs": [
        {
          "alt": "eBrandz",
          "title": ""
        },
        {
          "alt": "eBrandz",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d589fac09aba5ac4b6bac34b6be9c8f3.webp",
    "context": {
      "refs": [
        {
          "alt": "KBS",
          "title": ""
        },
        {
          "alt": "KBS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5b456b245280774899d9d0803c0c86e.webp",
    "context": {
      "refs": [
        {
          "alt": "CP PLUS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d809c8bc538fb14dd40f662c8f897c1d.webp",
    "context": {
      "refs": [
        {
          "alt": "Tanishq",
          "title": ""
        },
        {
          "alt": "Tanishq",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da37cfecb564018f501b209b5467c893.webp",
    "context": {
      "refs": [
        {
          "alt": "IBM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db60f2e0d75c0c6c5c0d132f8bed6c64.webp",
    "context": {
      "refs": [
        {
          "alt": "KGK",
          "title": ""
        },
        {
          "alt": "KGK",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db7d9f32196aa8ea7cc1a244033892ab.webp",
    "context": {
      "refs": [
        {
          "alt": "LOGIX",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db9f0a73386a9427b3a90afb1b3e469d.webp",
    "context": {
      "refs": [
        {
          "alt": "LAN REVAMPING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc91050af93d2e0d1ea0023bfa74997e.webp",
    "context": {
      "refs": [
        {
          "alt": "CONTINUUM",
          "title": ""
        },
        {
          "alt": "CONTINUUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1e335c8155fea93c7a640574b788e21.webp",
    "context": {
      "refs": [
        {
          "alt": "KHAITAN&CO",
          "title": ""
        },
        {
          "alt": "KHAITAN&CO",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2c19ccbc7117ee7b31376001fed4552.webp",
    "context": {
      "refs": [
        {
          "alt": "Sharon",
          "title": ""
        },
        {
          "alt": "Sharon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea73c30f748d428ea46d7c4521ce261a.webp",
    "context": {
      "refs": [
        {
          "alt": "IIFL",
          "title": ""
        },
        {
          "alt": "IIFL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea861803509b89e10dea7cd6694a8cce.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/eb7e5564d1501361b17d3ca13283a3da.webp",
    "context": {
      "refs": [
        {
          "alt": "prama hikvision",
          "title": ""
        },
        {
          "alt": "prama hikvision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f56ad1e3e46acfd20760328eb655ef39.webp",
    "context": {
      "refs": [
        {
          "alt": "pace",
          "title": ""
        },
        {
          "alt": "pace",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f98934e56875e863e280cdd72642e730.webp",
    "context": {
      "refs": [
        {
          "alt": "DEN",
          "title": ""
        },
        {
          "alt": "DEN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fae1ee03c48f171c404928c1e2ed9d8f.webp",
    "context": {
      "refs": [
        {
          "alt": "TREND",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb2db3c6f6a8f4b795daa45e269c758a.webp",
    "context": {
      "refs": [
        {
          "alt": "GRinfranet",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fee3590df23320bfe296a610bc5e1a71.webp",
    "context": {
      "refs": [
        {
          "alt": "ANANDRATHI",
          "title": ""
        },
        {
          "alt": "ANANDRATHI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | Home",
      "first_heading": "GRinfranet"
    }
  },
  {
    "path": "it-infrastructure-solutions.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | IT INFRASTRUCTURE SOLUTIONS",
      "first_heading": "IT INFRASTRUCTURE SOLUTIONS"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7252270698ab108664c28b3eb0ef720f.js",
    "context": {
      "path": "js/7252270698ab108664c28b3eb0ef720f.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "lan-revamping.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | LAN REVAMPING",
      "first_heading": "LAN REVAMPING"
    }
  },
  {
    "path": "network-security.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | NETWORK SECURITY & SERVER STORAGE SOLUTIONS",
      "first_heading": "NETWORK SECURITY & SERVER STORAGE SOLUTIONS"
    }
  },
  {
    "path": "outsourcing.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | OUTSOURCING",
      "first_heading": "OUTSOURCING"
    }
  },
  {
    "path": "partners.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | PARTNERS",
      "first_heading": "PARTNERS"
    }
  },
  {
    "path": "surveillance.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | SURVEILLANCE",
      "first_heading": "SURVEILLANCE"
    }
  },
  {
    "path": "thank-you.html",
    "context": {
      "title": "GRinfranet IT Infrastructure Service | CONTACT US",
      "first_heading": "THANK YOU"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.