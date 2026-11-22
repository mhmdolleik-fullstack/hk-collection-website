# HK Collection | Arabic Retail Catalog

I built this Arabic-language storefront for HK Collection so customers can browse the shop’s products on their phones and ask about a specific item through WhatsApp. The shop can manage its catalog from a separate admin page.

## Shopping experience

Customers browse seven categories, including perfumes, watches, wallets, and makeup. Each product has a detail page with its photo and price. The order button opens WhatsApp with a message about the selected item, so the customer and shop can continue the order there.

## Catalog management

The admin dashboard supports adding, editing, and removing products, uploading images, filtering the catalog, and exporting product data. The storefront reads from an Express API backed by MongoDB and includes a bundled catalog in `data.js` as a fallback.

## Preview locally

From the project root, run:

```sh
python -m http.server 8000
```

Open [the storefront](http://localhost:8000/) to browse. The frontend uses the configured hosted API by default.

## Run the API locally

From the `server` directory, run `npm ci`. Create a local `.env` file there with your MongoDB connection string:

```dotenv
MONGODB_URI=mongodb://127.0.0.1:27017/hk_collection
```

With MongoDB running, start the API with `npm start` and check [the health endpoint](http://localhost:5000/api/health). For local development, point the API URLs in `script.js` and `admin.js` to `http://localhost:5000/api` before editing catalog data.

**Stack** — HTML, CSS, JavaScript, Node.js, Express, Mongoose, and MongoDB.
