# amazonPriceDrops
Filter an amazon wish list by items with price drops

1. Navigate to your wishlist URL i.e. https://www.amazon.com/gp/registry/wishlist/153OV2P85MJD6
2. Run the JavaScript in amazonPriceDrops.js
3. Depending on your connection speed and size of your wishlist it could take up to a minute to load in all your items and filter the list

<a class="bookmarklet" href="javascript:(function()%7Bfunction%20removeItemsWithoutPriceDrops()%7Bvar%20anyRemoved%20%3D%20false%3Bvar%20listItems%20%3D%20document.getElementsByClassName('a-section%20g-item-sortable')%3Bfor%20(var%20i%20%3D%200%3B%20i%20%3C%20listItems.length%3B%20i%2B%2B)%20%7Bvar%20priceDrop%20%3D%20listItems%5Bi%5D.querySelectorAll('.itemPriceDrop')%3Bif%20(priceDrop.length%20%3D%3D%200)%20%7BlistItems%5Bi%5D.parentElement.removeChild(listItems%5Bi%5D)%3BanyRemoved%20%3D%20true%3B%7D%7Dif%20(anyRemoved)%20%7BremoveItemsWithoutPriceDrops()%3B%7D%7Dfunction%20loadAllAndRemoveItemsWithoutPriceDrops()%7Bwindow.scroll(0%2C%20document.body.scrollHeight)%3Bif%20((document.body.textContent%20%7C%7C%20document.body.innerText).indexOf('End%20of%20List')%20%3E%20-1)%20%7Bwindow.clearInterval(interval)%3BremoveItemsWithoutPriceDrops()%3Bdocument.getElementById('profile-list-name').innerHTML%20%3D%20'Books%20-%20'%20%2B%20document.getElementsByClassName('a-section%20g-item-sortable').length%3Bwindow.scroll(0%2C%200)%3B%7D%7Dvar%20interval%20%3D%20window.setInterval(loadAllAndRemoveItemsWithoutPriceDrops%2C%20250)%7D)()">Drag this to your bookmark bar</a>