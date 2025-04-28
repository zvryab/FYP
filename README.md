[NOTE: This is not updated yet, please wait until 30th April before accessing files]

Final Year Project: Enhancing HCI with AI


## Overview

This project investigates how large language models (LLMs) can enhance human-computer interaction by allowing users to query structured databases using natural language, without requiring SQL expertise. A working prototype has been developed using LangChain, PostgreSQL, and Gradio.

The repository is organised into two parts:

- **FYP_research**  
  Contains early research and development work, experimental code, and rough notes exploring different methods of natural language data retrieval. This section documents the iterative learning process during the project's investigation phase.

  DO NOT use this code unless you are able to comprehend all the work and notes. This is purely to observe the research journey and find useful steps you may be taking yourself.

  

- **FYP_final**  
  Contains the final, functional system code. This version demonstrates a working natural language to SQL query agent, connected to a PostgreSQL database through a secure tunnel (Ngrok), and presented via a Gradio interface.

## System Requirements

- Python 3.9+
- PostgreSQL installed locally
- Ngrok account (free tier sufficient)
- Google Colab or local Jupyter environment (Preferrably Colab Pro to use Terminal)
- Required Python packages:  
  (`LangChain`, `Gradio`, `SQLAlchemy`, `psycopg2`) + more specificed in code


## How to Run the Final System

1. **Setup PostgreSQL database**:
   - Deploy a PostgreSQL database locally.
   - Populate it using the sample database provided ( refer to dissertation report section 8.3 on how to setup a sample database, this one is known as 'Northwind'.)

2. **Connect Database to Google Colab**:
   - Open the notebook in `FYP_final` in Google Colab.
   - Follow steps on connecting database which will require details, instructions are shown below.
   - Start a local Ngrok tunnel to your PostgreSQL port (default: 5432).
     ```
     ngrok tcp 5432
     ```
   - Copy the Ngrok forwarding address and update the database connection settings in the notebook.

3. **Run the Gradio Interface**:
   - Launch the Gradio app from the Colab notebook.
   - Use the provided Gradio URL to interact with the system through a simple natural language input field.

## Notes

- Ngrok links remain active for a limited time (currently 1 week as of April 2025) unless upgraded to a paid account.
- Larger LLM models may require sufficient compute resources if running outside Colab. (Refer to Ollama's website for more details)
- For full system explanations and testing methodologies, please refer to the accompanying dissertation document.

