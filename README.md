# Coduri DRG.
JSON Coduri Drg/ICD-10 cu detalii in romana si grupate pe categorii.
Codurile urmaresc standardele internationale si fiecare diagnostic are detalii particulare. 
Ultima actualizare: 14.03.2021

Structura:

```
root (chapters): [
   {
      name: 'string',
      codes: 'string',
      sets: [
        {
          name: 'string',
          codes: 'string',
          classifications: [
            {
              name: 'string',
              code: 'string',
              name_latin: 'string' - NULLABLE,
              data: {
                //informatii suplimentare care pot sau nu exista, este incurajat ca aceste informatii sa fie NULLABLE
                sex:
                code: - same as classification -
                name: - same as classification -
                cod999: {
                  code: 
                  name:
                }
                age_max:
                age_min:
                chapter: {
                  name: - same as parent chapter -
                  codes: - same as parent chapter -
                },
                comment:
                icd_set: {
                  name: - same as parent set -
                  codes: - same as parent set -
                },
                excluding,
                including:
                morbidity: {
                  code:
                  name:
                },
                age_reject:
                name_latin: - same as classification -
                sex_reject:
                rare_disease:
                bg_drug_count:
              }
            },
            ...
          ]
        },
        ...
      ]
   },
    ...
]

```
