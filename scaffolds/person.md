% name: Person
% def: post_date=$(date +%Y-%m-%d)
% def: author='/about'
% def: collection_name='Details'
% def: person_state='OR'
% def: person_country='US'
---
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
sets:
    default:
        name: ${collection_name}
        showCount: true
        showMenu: true
content:
    items: '@self.children'
taxonomy:
    category: 
        - ${category}
    tag: 
        - ${tag}
show_gallery: false
data:
    person:
        '@type': Person
        givenName: ${person_first}
        familyName: ${person_last}
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


