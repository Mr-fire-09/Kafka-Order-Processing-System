# Kafka Order Processing System

A beginner-friendly Apache Kafka project using **Python**, **Docker**, and **Confluent Kafka Client**. This project demonstrates how a **Kafka Producer** sends order events and a **Kafka Consumer** processes them in real time.

---

## 🚀 Repository Name (Suggested)

**kafka-order-processing-python**

(You can also use: `python-kafka-order-system` or `kafka-producer-consumer-demo`)

---

## 📌 Project Overview

This project simulates a simple **order processing system** similar to real-world applications like Swiggy, Zomato, or Amazon.

### Flow:

```
Producer → Kafka Topic (orders) → Consumer
```

* Producer creates an order and sends it to Kafka
* Kafka stores and streams the message
* Consumer reads and processes the order

---

## 🧱 Tech Stack Used

* **Apache Kafka** (KRaft mode – no Zookeeper)
* **Docker & Docker Compose**
* **Python**
* **confluent-kafka** library

---

## 📂 Project Structure

```
kafka-order-processing-python/
│
├── docker-compose.yml
├── producer.py
├── consumer.py
├── requirements.txt
└── README.md
```

---

## 🐳 Kafka Setup (Docker)

### Step 1: Start Kafka

```bash
docker compose up -d
```

### Step 2: Verify Kafka is running

```bash
docker ps
```

You should see a container named `kafka` running on port **9092**.

---

## 🐍 Python Setup

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶ How to Run the Project

### Step 4: Start the Consumer (First)

```bash
python consumer.py
```

Expected output:

```
🟢 Consumer is running and subscribed to orders topic
```

---

### Step 5: Run the Producer (New Terminal)

```bash
python producer.py
```

Producer output:

```
✅ Delivered {...}
```

Consumer output:

```
📦 Received order: 10 x frozen yogurt from lara
```

---

## 🧾 Sample Order Message

```json
{
  "order_id": "uuid",
  "user": "lara",
  "item": "frozen yogurt",
  "quantity": 10
}
```

---

## 🤔 Why Kafka?

Kafka is used for:

* Real-time event processing
* High-throughput systems
* Decoupled microservices
* Scalable data pipelines

---

## 💡 Use Cases

* Order processing systems
* Log aggregation
* Notification systems
* Event-driven microservices
* Streaming analytics

---

## 📈 Future Improvements

* Multiple consumers (Consumer Groups)
* Kafka partitions
* Database integration
* Retry & error handling
* Schema Registry (Avro / Protobuf)

---

## 🎯 Learning Outcome

By completing this project, you will understand:

* Kafka Producer & Consumer basics
* Kafka topics and consumer groups
* Dockerized Kafka setup
* Real-time message streaming

---

## 🧑‍💻 Author

**Neeraj Singh**
CS Student | Learning DevOps & Cloud

---

⭐ If you found this project helpful, feel free to star the repository!
