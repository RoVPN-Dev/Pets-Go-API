// Example data to simulate the response from your API
let responseData = [
    ["Pet", {"id": "Banana"}, 30000000.0], 
    ["Pet", {"id": "Diamond Dragon"}, 8573583.996],
    ["Pet", {"id": "Holographic Cat"}, 3060535.173],
    ["Pet", {"id": "Hippomelon"}, 16721542.364],
    ["Pet", {"id": "Arcane Cat"}, 6395567]
];

// Loop through each item in the response and format it properly
responseData.forEach(item => {
    // Extract the pet name and cost
    let name = item[1].id; // Getting the pet name
    let cost = item[2]; // Getting the pet cost

    // Format the cost to have 'M' for millions
    let formattedCost = cost >= 1000000 ? `${(cost / 1000000).toFixed(0)}M` : cost;

    // Log the formatted output to the console
    console.log(`**Name:** ${name}\n**Cost:** ${formattedCost}`);
});
