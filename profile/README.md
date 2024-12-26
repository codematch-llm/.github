# CodeMatch - We detect stolen* code using LLM

In this project we aim to solve the modern challenge of code cloning, which has become increasingly common with the rise of AI-generated solutions. Using the power of Large Language Models (LLMs), CodeMatch helps developers ensure their code is original, compliant with licensing requirements, and free from intellectual property issues. The project is designed to identify and flag potential code clones, making it a valuable tool for fostering confidence and integrity in software development.

<img src="https://github.com/user-attachments/assets/a0c32170-3f28-4ee5-8db1-a0d88e9210d4" alt="inputted-code" width="500">
<img src="https://github.com/user-attachments/assets/c13339f8-3aa5-4aa7-bc8f-b2cd7532bbf3" alt="search-result" width="500">



Below is the general workflow of CodeMatch, which outlines how the system works end-to-end. Following the workflow, we provide detailed explanations of each component to give you a clear understanding of the process behind it.

<img src="https://github.com/user-attachments/assets/e0282343-a483-4b2a-8a8b-099c67778d82" alt="Workflow" width="500">

Each step is numbered from 1 to 10, representing the different stages of the process. Steps 7 and 10 occur after the optimal LLM has been selected and the system is fully operational.

### Components of the Workflow

1. **Finding/Creating Datasets**: At this initial stage, we gather or create datasets to evaluate various language models according to the project’s objectives. These datasets include original code snippets and their clones, covering a variety of programming languages and scenarios.

2. **Developing a Benchmark Mechanism for LLMs**: A robust benchmark is designed to evaluate and compare the performance of multiple LLMs. This involves assessing their ability to detect various types of code clones, such as exact, renamed, or semantic clones.

3. **Training/Fine-tuning the Chosen LLM Model**: Based on the benchmark results, the best-performing model is selected and fine-tuned for optimal performance. This ensures the model can generate accurate embeddings that capture the semantic meaning of code snippets.

4. **Retrieving Open Source Snippets from the Internet**: Once the optimal LLM is selected, we collect open-source code snippets from various repositories to populate the system's database. These snippets provide a foundation for detecting clones in real-world scenarios.

5. **Creating Embeddings with the Selected Model**: The chosen LLM is used to generate embeddings for the collected code snippets. These embeddings represent the semantic structure and functionality of the code, enabling efficient similarity searches.

6. **Using a Vector Database for Storage and Search**: The generated embeddings are stored in a vector database optimized for similarity searches. This database allows for fast and accurate retrieval of code snippets based on their embeddings.

7. **User Input Through Frontend**: Developers input new code snippets into the system using an intuitive frontend interface. This interface is designed to simplify the submission process and ensure a seamless user experience.

8. **Creating an Embedding with the Selected LLM**: In this step, a new code snippet submitted by the user is processed by the system. The selected LLM generates an embedding for the snippet, which is then used to search the database.

9. **Retrieving All Similar Code Snippets**: The system retrieves the top similar code snippets from the database and presents them to the user. Links to the original sources are provided for further review, ensuring compliance and originality.

10. **System Output Through Frontend**: The results, including similar code snippets and their sources, are displayed in an easy-to-understand format on the frontend. This allows users to assess the originality and compliance of their code efficiently.


### Outlining the Core Components

From the workflow outlined above, three key components of the CodeMatch system can be identified:

#### 1. Benchmark
This component focuses on evaluating and selecting the best LLM for the system. It includes:
- **Step 1**: Finding or creating datasets to evaluate language models.
- **Step 2**: Developing a robust benchmarking mechanism to compare LLMs.
- **Step 3**: Training or fine-tuning the chosen LLM for optimal performance.

The benchmark component has its own dedicated [repository](https://github.com/codematch-llm/benchmark).

#### 2. Backend
The backend is responsible for handling the core functionalities of the system, including:
- **Step 4**: Retrieving open-source snippets from the internet.
- **Step 5**: Generating embeddings for these snippets using the selected LLM.
- **Step 6**: Storing and managing embeddings in a vector database to enable efficient similarity searches.

The backend is part of the system repository - [system-backend](https://github.com/codematch-llm/system/tree/main/backend).

#### 3. Frontend
The frontend provides a user-friendly interface that interacts with the backend. It includes:
- **Step 7**: Allowing users to input new code snippets.
- **Step 8**: Generating embeddings for the submitted code.
- **Step 9**: Retrieving similar code snippets from the database.
- **Step 10**: Displaying the results and their sources to the user.

The frontend is part of the system repository - [system-frontend](https://github.com/codematch-llm/system).

--

In each repository there is a more in-depth explanation of how its respective components work and are implemented in detail.

--



