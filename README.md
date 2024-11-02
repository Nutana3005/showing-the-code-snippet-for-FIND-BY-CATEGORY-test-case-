# showing-the-code-snippet-for-FIND-BY-CATEGORY-test-case-
def test_find_product_by_category(self):
    # Create a product with a specific category
    product = Product(name="SampleProduct", category="Electronics", available=True)
    product.save()
    
    # Retrieve products by category
    found_products = Product.find_by_category("Electronics")
    
    # Assert that the product is in the result
    assert len(found_products) > 0
    assert found_products[0].category == "Electronics"
