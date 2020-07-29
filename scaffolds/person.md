% name: Person
% def: author='/about'
% def: collection_name='Details'
% def: person_state='OR'
% def: person_country='US'
---
title: ${title}
subtitle: ${subtitle}
author: ${author:-/about}
collection:
    name: ${collection_name:-Articles}
    showCount: true
    showMenu: true
content:
    items: '@self.children'
child_type: article
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
                addressRegion: ${person_state:-OR}
                postalCode: ${person_zip}
                addressCountry: ${person_country}
---

${summary}

===


