<script>
  let text = "Type your message here...";

  // Download as PNG image using html2canvas
  import html2canvas from 'html2canvas';
  let previewEl;

  async function downloadImage() {
    const canvas = await html2canvas(previewEl, { backgroundColor: '#fff' });
    const url = canvas.toDataURL('image/png');
    const a = document.createElement('a');
    a.href = url;
    a.download = 'message.png';
    a.click();
  }
</script>

<style>
  textarea {
    font-family: 'Mr Fruit', sans-serif;
    font-size: 26px;
    width: 100%;
    height: 150px;
    padding: 10px;
    border: 5px solid red;
    background-color: #fdf677;
  }


  .editable {
    font-family: 'Mr Fruit', sans-serif;
    font-size: 26px;
    width: 100%;
    min-height: 220px;
    padding: 10px;
    border: 5px solid red;
    background-color: #fdf677;
    white-space: pre-wrap;
    word-wrap: break-word;
    outline: none;
  }


  button {
    margin-top: 15px;
    margin-left:auto;
    padding: 10px 20px;
    font-size: 16px;
    display: block;
    font-weight: 600;
    background-color: white;
    font-family:"Tiempos Text", Iowan Old Style, Times New Roman, Times, serif;
  }

    textarea{
        max-width: 100%;
        margin: auto;
    }
</style>

<div
  class="editable"
  contenteditable="true"
  bind:this={previewEl}
  on:input={(e) => text = e.target.innerText}
>{text}</div>


<!-- <div class="preview">
  {text}
</div> -->

<button on:click={downloadImage}>Download as image</button>
