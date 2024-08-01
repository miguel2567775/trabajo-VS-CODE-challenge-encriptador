document.getElementById('encryptBtn').addEventListener('click', function() {
    let inputText = document.getElementById('inputText').value.trim();
    if (validateInput(inputText)) {
        let encryptedText = encryptText(inputText);
        document.getElementById('outputText').innerText = encryptedText;
    }
});

document.getElementById('decryptBtn').addEventListener('click', function() {
    let inputText = document.getElementById('inputText').value.trim();
    if (validateInput(inputText)) {
        let decryptedText = decryptText(inputText);
        document.getElementById('outputText').innerText = decryptedText;
    }
});

document.getElementById('copyBtn').addEventListener('click', function() {
    let outputText = document.getElementById('outputText').innerText;
    if (outputText !== "Ningún mensaje fue encontrado") {
        navigator.clipboard.writeText(outputText).then(function() {
            alert('Texto copiado al portapapeles');
        }, function(err) {
            console.error('Error al copiar el texto: ', err);
        });
    }
});

function validateInput(text) {
    const lowercaseWithoutAccents = /^[a-z\s]+$/;
    if (text === "") {
        document.getElementById('outputText').innerText = "Ningún mensaje fue encontrado";
        return false;
    } else if (!lowercaseWithoutAccents.test(text)) {
        document.getElementById('outputText').innerText = "Error: Solo letras minúsculas y sin acentos";
        return false;
    }
    return true;
}

function encryptText(text) {
    return text.replace(/e/g, 'enter')
               .replace(/i/g, 'imes')
               .replace(/a/g, 'ai')
               .replace(/o/g, 'ober')
               .replace(/u/g, 'ufat');
}

function decryptText(text) {
    return text.replace(/enter/g, 'e')
               .replace(/imes/g, 'i')
               .replace(/ai/g, 'a')
               .replace(/ober/g, 'o')
               .replace(/ufat/g, 'u');
}
