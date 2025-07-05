# Shampoo-Inventory-System-Mini-ERP-
Shampoo Inventory System (Mini ERP)
# Shampoo Inventory Tracking System

class Shampoo:
    def __init__(self, name, quantity, reorder_level):
        self.name = name
        self.quantity = quantity
        self.reorder_level = reorder_level

    def status(self):
        return "⚠️ Reorder Needed" if self.quantity <= self.reorder_level else "✅ Stock OK"

# Add 3 shampoo products
shampoos = [
    Shampoo("Dove Shampoo", 15, 10),
    Shampoo("Head & Shoulders", 8, 12),
    Shampoo("Clinic Plus", 25, 15)
]

# Print Inventory Status
print("🧴 Shampoo Inventory Report\n")
for s in shampoos:
    print(f"{s.name} - Qty: {s.quantity} | Reorder Level: {s.reorder_level} → {s.status()}")
