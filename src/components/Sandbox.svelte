<script>
  let text = "Type your message here...";

  // Download as PNG image using html2canvas
  import html2canvas from 'html2canvas';
  let previewEl;


function isMobile() {
  return /Mobi|Android/i.test(navigator.userAgent);
}

async function downloadOrShowImage() {
  const canvas = await html2canvas(previewEl, { backgroundColor: '#fff' });
  
  if (isMobile()) {
    // Show image in modal on mobile
    const url = canvas.toDataURL('image/jpeg');
    
    const img = document.createElement('img');
    img.src = url;
    img.style.width = '100%';
    img.style.height = 'auto';

    const modal = document.createElement('div');
    Object.assign(modal.style, {
      position: 'fixed',
      top: 0, left: 0, right: 0, bottom: 0,
      backgroundColor: 'rgba(0,0,0,0.8)',
      display: 'flex',
      justifyContent: 'center',
      alignItems: 'center',
      zIndex: 9999,
    });
    modal.appendChild(img);

    modal.addEventListener('click', () => {
      document.body.removeChild(modal);
    });

    document.body.appendChild(modal);

  } else {
    // On desktop: open in new tab using blob URL
    canvas.toBlob((blob) => {
      if (!blob) return;

      const url = URL.createObjectURL(blob);
      window.open(url, '_blank');
      setTimeout(() => URL.revokeObjectURL(url), 10000);
    }, 'image/jpeg');
  }
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

<button on:click={downloadOrShowImage}>Download as image</button>
