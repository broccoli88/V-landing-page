<template>
    <div class="footer">
        <h1>traveler</h1>
        <div class="services">
            <ul>
                <li>Countries</li>
                <li>Regions</li>
                <li>Cities</li>
                <li>Districts</li>
                <li>Airports</li>
                <li>Hotels</li>
                <li>Places of interest</li>
            </ul>
            <ul>
                <li>Homes</li>
                <li>Apartments</li>
                <li>Resorts</li>
                <li>Villas</li>
                <li>Hostels</li>
                <li>B&Bs</li>
                <li>Guest houses</li>
            </ul>

            <ul>
                <li>Unique places to stay</li>
                <li>All destinations</li>
                <li>Discover</li>
                <li>Reviews</li>
                <li>Unpacked: Travel articles</li>
                <li>Travel communities</li>
                <li>Seasonal and holiday deals</li>
            </ul>
            <ul>
                <li>Car rental</li>
                <li>Flight finder</li>
                <li>Restaurant reservations</li>
                <li>Booking.com for Travel Agents</li>
            </ul>
            <ul>
                <li>Coronavirus (COVID-19) FAQs</li>
                <li>About Traveler</li>
                <li>Customer Service Help</li>
                <li>Careers</li>
                <li>Sustainability</li>
                <li>Press center</li>
                <li>Safety Resource Center</li>
                <li>Investor relations</li>
                <li>Terms & conditions</li>
                <li>Partner dispute</li>
                <li>How We Work</li>
                <li>Privacy & cookie statement</li>
                <li>Corporate contact</li>
            </ul>
        </div>
    </div>
</template>



<style scoped>
.footer {
    width: 100%;
    border-top: 5px solid var(--color-secondary);
    padding: 4rem;

    display: flex;
    flex-direction: column;
    gap: 3rem;

    overflow-x: hidden;
}

.services {
    width: 70%;
    margin: 0 auto;

    flex: 1;
    display: flex;
    flex-wrap: wrap;
    /* flex-direction: column; */
    justify-content: space-around;

    gap: 1.5rem;
}

h1 {
    text-transform: capitalize;
    font-family: var(--font-lobster);
    font-size: 3.5rem;
}

ul {
    flex: 1;

    list-style: none;
    font-weight: 400;
    font-size: 1.4rem;
}

ul li {
    cursor: pointer;
}

ul li:hover {
    color: var(--color-secondary);
}
</style>