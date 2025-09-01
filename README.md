# SmolVLM Real-time Camera Demo

A simple demo on using the `llama.cpp` server with SmolVLM 500M for real-time object detection.

## How to Setup

1.  Install [llama.cpp](https://github.com/ggml-org/llama.cpp).
2.  Run the `llama.cpp` server. The server will automatically download the model from Hugging Face.

   *   **Basic command (CPU):**
      ```llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF```

   *   **Command with GPU acceleration:**
      ```llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF:Q8_0 -ngl 99 -t 8 --port 8080```

   **Common Flags:**
   *   `-ngl 99`: Enables GPU acceleration by offloading layers to the GPU.
   *   `-t 8`: Sets the number of CPU threads.
   *   `--port 8080`: Specifies the server port.
   *   `:Q8_0`: Selects the model quantization type.

   > **Note:** Other multimodal models are also supported. See the [llama.cpp documentation](https://github.com/ggml-org/llama.cpp/blob/master/docs/multimodal.md) for more options.

3.  Open `index.html` in your browser.
4.  (Optional) Modify the instruction prompt in the UI (e.g., to return JSON).
5.  Click "Start" to begin.

