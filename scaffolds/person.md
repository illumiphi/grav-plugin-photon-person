% name: Person
% def: post_date=$(date +%m/%d/%Y)
% def: author='/about'
% def: collection_name='Details'
% def: person_state='OR'
% def: person_country='US'
---
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
content:
    title: ${collection_name}
    items: '@self.children'
taxonomy:
    category: 
        - people
    tag: 
data:
    person:
        '@type': Person
        givenName: ${person_first}
        familyName: ${person_last}
        email: ${person_email}
        telephone: ${person_phone}
        url: ${person_url} 
        location:
            address:
                streetAddress: ${person_street}
                addressLocality: ${person_city}
                addressRegion: ${person_state}
                postalCode: ${person_zip}
                addressCountry: ${person_country}
---

${summary}

===


