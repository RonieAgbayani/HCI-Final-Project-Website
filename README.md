# HCI-Final-Project-Website

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ordering System Group 3</title>
    <link rel="stylesheet" href="HCI_FinalProject_Website.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <div class="container">
        <div class="products">
            <div class="product" onclick="selectProduct('Yellow Pad Paper')">
                <img src="images/YellowPaper.jpg" alt="Yellow Pad Paper">
                <p>Yellow Pad Paper</p>
            </div>
            <div class="product" onclick="selectProduct('Ballpen')">
                <img src="images/ballpen.jpg" alt="Ballpen">
                <p>Ballpen</p>
            </div>
            <div class="product" onclick="selectProduct('Notebook')">
                <img src="images/Notebook.jpg" alt="Notebook">
                <p>Notebook</p>
            </div>
            <div class="product" onclick="selectProduct('Pencil')">
                <img src="images/pencil.jpg" alt="Pencil">
                <p>Pencil</p>
            </div>
            <div class="product" onclick="selectProduct('Eraser')">
                <img src="images/eraser.jpg" alt="Eraser">
                <p>Eraser</p>
            </div>
            <div class="product" onclick="selectProduct('Marker')">
                <img src="images/marker.jpg" alt="Marker">
                <p>Marker</p>
            </div>
            <div class="product" onclick="selectProduct('Scissors')">
                <img src="images/gunting2.jpg" alt="Scissors">
                <p>Scissors</p>
            </div>
            <div class="product" onclick="selectProduct('Glue')">
                <img src="images/glue.jpg" alt="Gluer">
                <p>Glue</p>
            </div>
            <div class="product" onclick="selectProduct('Ruler')">
                <img src="images/Ruler2.jpg" alt="Ruler">
                <p>Ruler</p>
            </div>
            <div class="product" onclick="selectProduct('Crayons')">
                <img src="images/crayons.jpg" alt="Crayons">
                <p>Crayons</p>
            </div>
            <div class="product" onclick="selectProduct('Coupon')">
                <img src="images/bandpaper.jpg" alt="Coupon">
                <p>Coupon</p>
            </div>
            <div class="product" onclick="selectProduct('Highlighter')">
                <img src="images/highlighter.jpg" alt="Highlighter">
                <p>Highlighter</p>
            </div>
            <div class="product" onclick="selectProduct('Tape')">
                <img src="images/tape.jpg" alt="Tape">
                <p>Tape</p>
            </div>
            <div class="product" onclick="selectProduct('Sharpener')">
                <img src="images/sharpener.jpg" alt="Sharpener">
                <p>Sharpener</p>
            </div>
            <div class="product" onclick="selectProduct('Calculator')">
                <img src="images/calculator2.jpg" alt="Calculator">
                <p>Calculator</p>
            </div>
            <div class="product" onclick="selectProduct('Bag Pack')">
                <img src="images/bag.jpg" alt="Bag Pack">
                <p>Bag Pack</p>
            </div>
        </div>

        <div class="order-form">
    <h2>School Supply Ordering System Group 3</h2>
    <form id="orderForm">
        <input type="text" id="buyerName" placeholder="Enter your name" required class="form-control my-2">
        <input type="email" id="email" placeholder="Enter your email" required class="form-control my-2">
        <input type="text" id="selectedItem" placeholder="Selected Item" readonly required class="form-control my-2">
        <input type="number" id="quantity" placeholder="Quantity" min="1" required class="form-control my-2">
        <input type="text" id="address" placeholder="Enter your address" required class="form-control my-2">
        <button type="submit" class="btn btn-primary">Place Order</button>

        <div id="orderSummary" class="order-summary mt-4" style="display: none;">
            <h4>Order Summary</h4>
            <p><strong>Name:</strong> <span id="summaryName"></span></p>
            <p><strong>Email:</strong> <span id="summaryEmail"></span></p>
            <p><strong>Item:</strong> <span id="summaryItem"></span></p>
            <p><strong>Quantity:</strong> <span id="summaryQty"></span></p>
            <p><strong>Address:</strong> <span id="summaryAddress"></span></p>
        </div>
    </form>
</div>

    <script>
        function selectProduct(item) {
            document.getElementById('selectedItem').value = item;
        }

        document.getElementById("orderForm").addEventListener("submit", function(e) {
            e.preventDefault();

            const name = document.getElementById("buyerName").value;
            const email = document.getElementById("email").value;
            const item = document.getElementById("selectedItem").value;
            const qty = document.getElementById("quantity").value;
            const address = document.getElementById("address").value;

            document.getElementById("summaryName").textContent = name;
            document.getElementById("summaryEmail").textContent = email;
            document.getElementById("summaryItem").textContent = item;
            document.getElementById("summaryQty").textContent = qty;
            document.getElementById("summaryAddress").textContent = address;

            document.getElementById("orderSummary").style.display = "block";
        });
    </script>
