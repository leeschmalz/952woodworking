---
layout: default
title: 952woodworking Listings
carousels: # should be in same order as listings.yml file
  - images:
      - image: /assets/images/farmhouse-end-tables1.jpg
      - image: /assets/images/farmhouse-end-tables2.jpg
      - image: /assets/images/farmhouse-end-tables3.jpg
  - images:
      - image: /assets/images/farmhouse-coffee-table1.jpg
      - image: /assets/images/farmhouse-coffee-table2.jpg
      - image: /assets/images/farmhouse-coffee-table3.jpg
  - images:
      - image: /assets/images/full-set1.jpg
      - image: /assets/images/full-set2.jpg
      - image: /assets/images/full-set3.jpg
  - images:
      - image: /assets/images/timber-table1.jpg
      - image: /assets/images/timber-table2.jpg
      - image: /assets/images/timber-table3.jpg
      - image: /assets/images/timber-table4.jpg
---

<div class="listings-container">
    <div class="furniture-listings">
    {% for item in site.data.listings %}
        <div class="furniture-item">
            <h2>{{ item.name }}</h2>
            {% include carousel.html height="100" unit="%" duration="7" number=forloop.index0 %}
            <p class="price-tag"><strong>${{ item.price }}</strong></p>
            <p>{{ item.description }}</p>
            <div class="paypal-button-container">
                <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
                <input type="hidden" name="cmd" value="_s-xclick" />
                <input type="hidden" name="hosted_button_id" value="{{ item.payment_button_id }}" />
                <input type="hidden" name="currency_code" value="USD" />
                <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynowCC_LG.gif" border="0" name="submit" title="PayPal - The safer, easier way to pay online!" alt="Buy Now" />
                </form>
            </div>
        </div>
    {% endfor %}
    </div>
</div>