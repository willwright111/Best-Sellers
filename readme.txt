Call the created block, to do that go to Backend > CMS > Pages > Edit Page ‘Home page’ and add the following lines of code:

{{block type="catalog/product_bestseller" template="catalog/product/bestseller.phtml" header="Bestsellers" limit=4}}


Also you can add a new block via layout update:

<reference name="content">
        <block type="catalog/product_bestseller" name="bestseller" template="catalog/product/bestseller.phtml" before="-">
            <action method="setLimit"><limit>3</limit></action>
            <action method="setHeader"><header>Best Sellers</header></action>
        </block>
</reference>
For instance, try to add this block to the Category View page here:

Backend > Catalog > Manage Categories > Click needed category in the category tree > `Custom Design` horizontal tab > ` Custom Layout Update` field