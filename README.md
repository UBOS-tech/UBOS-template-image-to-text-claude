<p align="center">
  <img width="50%" align="center" alt="Ubos - End-to-End Software Development Platform" src="https://ubos.tech/wp-content/uploads/2023/03/cropped-Group-21015-1.png">
</p>

<h3 align="center">
  <b><a href="https://documentation.ubos.tech/docs/intro">Get Started</a></b>
  •
  <a href="https://community.ubos.tech/">Community</a>
  •
  <a href="https://www.youtube.com/@ubos_tech">Youtube</a>
  •
  <a href="https://discord.com/invite/dt59QaptH2">Discord</a>
  •
  <a href="https://github.com/UBOS-tech">GitHub</a>
  </h3>

<div align="center">
  
  [![Use template](https://ubos.tech/wp-content/uploads/2023/06/download-logo.png)](https://platform.ubos.tech/?templateId=65f48f82e25b49001179f4ee)
  
</div>
    <h1>Image to Text with Claude 3</h1>

  <p>The Image to Text with Claude 3 template is a powerful tool that leverages the capabilities of the advanced Claude 3 AI model to generate accurate and insightful textual descriptions from uploaded images. This template provides a seamless experience for users, enabling them to effortlessly extract meaningful information from visual content.</p>

  <h2>Node-RED Flow for Image Description using Claude AI</h2>

  <p>
    <img src="https://github.com/UBOS-tech/UBOS-template-image-to-text-claude/assets/87094132/3a21c713-1089-4792-a855-99969ea4a586" alt="Image">
  </p>

  <p>This is a Node-RED flow that allows users to send an image and receive a textual description of the image's contents using the Claude AI model from Anthropic. Here's a breakdown of the flow's components:</p>

  <ul>
    <li><strong>HTTP Input Node:</strong> This node listens for incoming HTTP POST requests at the /describeImage endpoint. It expects the request to include an image file and an API key for Anthropic.</li>
    <li><strong>Function Node (make request to Claude):</strong> This function node prepares the request payload to be sent to the Anthropic API. It constructs a JSON object with the necessary fields, including the AI model to use (msg.payload.model), the maximum number of tokens to generate (max_tokens: 2500), and the user's input, which is an array containing the base64-encoded image data and the prompt "What is in this image?".</li>
    <li><strong>HTTP Request Node (to Anthropic):</strong> This node sends a POST request to the Anthropic API (https://api.anthropic.com/v1/messages) with the prepared payload. The request includes the necessary headers, such as the API key and the Anthropic version.</li>
    <li><strong>Function Node (prepare response to UI):</strong> This function node processes the response from the Anthropic API. If the response status code is 200 (successful), it extracts the generated text from the response payload and assigns it to msg.payload. If there's an error, it constructs an error message and assigns it to msg.payload.</li>
    <li><strong>HTTP Response Node:</strong> This node sends the final response back to the client, containing either the generated text description of the image or an error message.</li>
  </ul>

  <h2>Key Features</h2>

  <h3>Image Upload</h3>
  <p>The template features a user-friendly interface that allows users to upload images in popular formats such as JPEG, PNG, GIF, WEBP. The uploading process is straightforward and intuitive, ensuring a smooth user experience.</p>

  <h3>Text Extraction with Claude 3</h3>
  <p>At the heart of this template lies the powerful Claude 3 AI model, specifically designed for image analysis and text generation tasks. Claude 3 employs advanced computer vision and natural language processing techniques to accurately interpret the visual content and generate detailed textual descriptions.</p>

  <h3>Multiple Model Variants</h3>
  <p>To cater to diverse use cases and preferences, the template offers multiple variants of the Claude 3 model:</p>
  <ul>
    <li><strong>claude-3-opus-20240229:</strong> This model provides comprehensive and detailed descriptions, making it well-suited for longer-form content or narratives.</li>
    <li><strong>claude-3-sonnet-20240229:</strong> Optimized for generating concise and poetic descriptions, this model excels in creative or artistic contexts, offering a more artistic interpretation of the visual content.</li>
    <li><strong>claude-3-haiku-20240307:</strong> Designed to craft succinct and evocative descriptions in the traditional Japanese haiku structure, this model offers a unique and minimalistic approach to describing images.</li>
  </ul>

  <h3>API Integration</h3>
  <p>To ensure secure and seamless integration with the Claude 3 AI model, users need to obtain an API key. The template provides clear instructions and guidance on how to acquire and utilize the API key effectively.</p>

  <h3>Fast Processing</h3>
  <p>Thanks to Claude 3's efficient processing capabilities, users can expect quick turnaround times for generating image descriptions. This feature ensures a smooth and responsive user experience, minimizing wait times and enabling users to access insights from visual data promptly.</p>

  <h3>Accuracy and Reliability</h3>
  <p>Claude 3 is trained on vast datasets and continuously updated to maintain high accuracy and reliability in generating descriptions. Users can trust the quality of the outputted text, ensuring that the information extracted from images is precise and dependable.</p>

  <h3>Customization Options</h3>
  <p>The template offers various customization options, allowing users to fine-tune the output according to their specific requirements. This includes adjusting parameters such as output length, level of detail, and specific areas of focus, ensuring that the generated descriptions align with the user's needs.</p>

  <h2>Benefits</h2>
  <p>The Image to Text with Claude 3 template empowers users with a robust and efficient solution for extracting valuable information from images. Whether for accessibility purposes, content indexing, data analysis, or simply gaining insights from visual data, this template offers a comprehensive and user-friendly experience. By leveraging the advanced capabilities of Claude 3, users can unlock the hidden potential of their visual content and transform it into actionable and meaningful textual information.</p>

    <p>
    <img src="https://ubos.tech/wp-content/uploads/2024/03/Group-15.png" alt="Image">
  </p>
