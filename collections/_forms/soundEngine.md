---
layout: articles
show_title: false
show_date: false
permalink: /voyage/soundEngine
titles:
  en: &EN Create Sound Engine
  en-GB: *EN
  en-US: *EN
  en-CA: *EN
  en-AU: *EN
key: IP
---

<!-- Sound Engine Form Container -->
<div class="form-container">
    <div class="button-container">
        <div class="back-button-container">
            <a href="/voyage" title="Back to Voyage">
                <button id="backButton" class="btn button--outline-primary button--circle">
                    <span class="material-symbols-outlined">arrow_back_ios_new</span>
                </button>
            </a>
        </div>
        <div class="edit-button-container">
            <button id="editButton" class="btn button--outline-primary button--circle" title="Edit Sound Engine" style="display: none;">
                <span class="material-symbols-outlined">edit</span> 
            </button>
        </div>
    </div>

    <h3 id="formTitle">Create a Sound Engine</h3>
    <p>Create a new Sound Engine with custom parameters for audio manipulation.</p>
    <div class="p-2"></div>

    <!-- View Mode -->
    <div id="soundEngineView">
        <div id="soundEngineImagePreviewContainer">
            <img id="soundEngineImagePreview" src="" alt="Sound Engine Image" style="display: none;" width="480" height="480">
        </div>
        <p><strong>Developer Username:</strong> <span id="displayDeveloperUsername"></span></p>
        <p><strong>Sound Engine Name:</strong> <span id="displaySoundEngineName"></span></p>
        <p><strong>Color 1:</strong> <span id="displayColor1"></span></p>
        <p><strong>Color 2:</strong> <span id="displayColor2"></span></p>
        <p><strong>Sonification Button:</strong> <span id="displaysonificationState"></span></p>
        <p><strong>Availability:</strong> <span id="displayAvailability"></span></p>
        <p><strong>Credits:</strong> <span id="displayCredits"></span></p>
    </div>

    <!-- Edit/Create Mode -->
    <form id="soundEngineForm" class="contact-form" style="display: none;" enctype="multipart/form-data">
        <!-- Sound Engine Image Upload -->
        <label for="soundEngineImage">Upload Sound Engine Image (Optional):</label>
        <div id="soundEngineImagePreviewContainer">
            <img id="soundEngineImagePreviewForm" src="" alt="Sound Engine Image" style="display: none;" width="480" height="480">
            <!-- Add a label showing the existing image path -->
            <p id="existingImage" style="display: none;">Current Image: <a href="" target="_blank" id="existingImageLink">View</a></p>
        </div>
        <input type="file" id="soundEngineImage" name="soundEngineImage" accept=".jpg, .jpeg, .png"><br><br>

        <!-- Sound Engine JSON Upload -->
        <label for="soundEngineFile">Upload Sound Engine JSON File (Optional):</label>
        <p id="existingJsonFile" style="display: none;">Current JSON File: <a href="" target="_blank" id="existingJsonLink">Download</a></p>
        <input type="file" id="soundEngineFile" name="soundEngineFile" accept=".json"><br><br>

        <!-- Other input fields -->
        <label for="developerUsername">Developer Username<span style="color: red;">*</span>:</label>
        <input type="text" id="developerUsername" name="developerUsername" required><br><br>

        <label for="soundEngineName">Sound Engine Name<span style="color: red;">*</span>:</label>
        <input type="text" id="soundEngineName" name="soundEngineName" required><br><br>

        <!-- Color 1 Picker -->
        <div id="color1Section" style="border: 5px solid rgba(255, 255, 255, 1); padding: 10px; margin-bottom: 10px;">
            <label for="color1">Color 1 (RGBA)<span style="color: red;">*</span>:</label>
            <input type="color" id="color1Picker" name="color1Picker" value="#ff33cc" required>
            <input type="range" id="alpha1Picker" name="alpha1Picker" min="0" max="1" step="0.01" value="1" required>
            <label for="alpha1Picker">Alpha 1: <span id="alpha1Value">1</span></label>
            <input type="hidden" id="color1" name="color1">
        </div>

        <!-- Color 2 Picker -->
        <div id="color2Section" style="border: 5px solid rgba(255, 255, 255, 1); padding: 10px; margin-bottom: 10px;">
            <label for="color2">Color 2 (RGBA)<span style="color: red;">*</span>:</label>
            <input type="color" id="color2Picker" name="color2Picker" value="#33ffff" required>
            <input type="range" id="alpha2Picker" name="alpha2Picker" min="0" max="1" step="0.01" value="1" required>
            <label for="alpha2Picker">Alpha 2: <span id="alpha2Value">1</span></label>
            <input type="hidden" id="color2" name="color2">
        </div><br><br>

        <!-- X Parameter (Speed) -->
        <div style="margin-right: 20px;">
            <div style="flex: 2;">
                <label for="xParamLabel">X Parameter Label<span style="color: red;">*</span>:</label>
                <input type="text" id="xParamLabel" name="xParamLabel" value="Speed" required>
            </div>
            <div style="display: flex; align-items: center; justify-content: space-between; margin-right: 15px;">
                <div style="flex: 1;">
                    <label for="xParamMin">Min:</label>
                    <input type="number" id="xParamMin" name="xParamMin" value="-100" required>
                </div>
                <div style="flex: 1;">
                    <label for="xParamMax">Max:</label>
                    <input type="number" id="xParamMax" name="xParamMax" value="100" required>
                </div>
                <div style="flex: 1;">
                    <label for="xParamInit">Initial:</label>
                    <input type="number" id="xParamInit" name="xParamInit" value="1" required>
                </div>
            </div>
        </div><br><br>

        <!-- Y Parameter (Tremolo) -->
        <div style="margin-right: 20px;">
            <div style="flex: 2;">
                <label for="yParamLabel">Y Parameter Label<span style="color: red;">*</span>:</label>
                <input type="text" id="yParamLabel" name="yParamLabel" value="Tremolo" required>
            </div>
            <div style="display: flex; align-items: center; justify-content: space-between; margin-right: 15px;">
                <div style="flex: 1;">
                    <label for="yParamMin">Min:</label>
                    <input type="number" id="yParamMin" name="yParamMin" value="-100" required>
                </div>
                <div style="flex: 1;">
                    <label for="yParamMax">Max:</label>
                    <input type="number" id="yParamMax" name="yParamMax" value="100" required>
                </div>
                <div style="flex: 1;">
                    <label for="yParamInit">Initial:</label>
                    <input type="number" id="yParamInit" name="yParamInit" value="0" required>
                </div>
            </div>
        </div><br><br>

        <!-- Z Parameter (SpaceReverb) -->
        <div style="margin-right: 20px;">
            <div style="flex: 2;">
                <label for="zParamLabel">Z Parameter Label<span style="color: red;">*</span>:</label>
                <input type="text" id="zParamLabel" name="zParamLabel" value="SpaceReverb" required>
            </div>
            <div style="display: flex; align-items: center; justify-content: space-between; margin-right: 15px;">
                <div style="flex: 1;">
                    <label for="zParamMin">Min:</label>
                    <input type="number" id="zParamMin" name="zParamMin" value="-100" required>
                </div>
                <div style="flex: 1;">
                    <label for="zParamMax">Max:</label>
                    <input type="number" id="zParamMax" name="zParamMax" value="100" required>
                </div>
                <div style="flex: 1;">
                    <label for="zParamInit">Initial:</label>
                    <input type="number" id="zParamInit" name="zParamInit" value="0" required>
                </div>
            </div>
        </div><br><br>

        <label for="sonificationState">Sonification Button:</label>
        <select id="sonificationState" name="sonificationState" required>
            <option value="false">Disabled</option>
            <option value="true">Enabled</option>
        </select><br><br>

        <label for="Availability">Availability:</label>
        <select id="availability" name="availability" required>
            <option value="public">Public</option>
            <option value="private">Private</option>
        </select><br><br>
        
        <label for="credits">Credits:</label>
        <textarea id="credits" name="credits" rows="3" maxlength="500"></textarea><br><br>

        <button type="submit">Save Sound Engine</button>
        <div class="p-2"></div>

        <!-- Progress Bar -->
        <div class="progress-bar" style="width: 100%; background-color: lightgray;">
            <div id="progress" style="width: 0%; height: 20px; background-color: green;"></div>
        </div>
        
        <button type="button" id="cancelButton" class="btn button--outline-primary button--circle">Cancel</button>
        <div class="p-2"></div>
    </form>
</div>

<!-- Toast Container for Notifications -->
<div id="toastContainer" style="position: fixed; top: 20px; right: 20px; z-index: 1000;"></div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const userId = localStorage.getItem('userId'); 
    if (!userId) {
        document.getElementById('messageDisplay').innerText = 'No logged-in user found. Please log in first.';
        document.getElementById('messageDisplay').style.color = 'red';
        window.location.href = '/login';
        return;
    }

    let isEditMode = false;
    let currentSoundEngineId = null;
    let isOwner = false;

    const formTitle = document.getElementById('formTitle');
    const soundEngineView = document.getElementById('soundEngineView');
    const soundEngineForm = document.getElementById('soundEngineForm');
    const editButton = document.getElementById('editButton');
    const backButton = document.getElementById('backButton');
    const cancelButton = document.getElementById('cancelButton');

    const soundEngineFileInput = document.getElementById('soundEngineFile');
    const soundEngineImageInput = document.getElementById('soundEngineImage');
    const soundEngineImagePreview = document.getElementById('soundEngineImagePreview');
    const soundEngineImagePreviewForm = document.getElementById('soundEngineImagePreviewForm');

    const color1Picker = document.getElementById('color1Picker');
    const color2Picker = document.getElementById('color2Picker');
    const alpha1Picker = document.getElementById('alpha1Picker');
    const alpha2Picker = document.getElementById('alpha2Picker');
    const color1Section = document.getElementById('color1Section');
    const color2Section = document.getElementById('color2Section');

    const color1Input = document.getElementById('color1');
    const color2Input = document.getElementById('color2');
    const alpha1Value = document.getElementById('alpha1Value');
    const alpha2Value = document.getElementById('alpha2Value');

    const urlParams = new URLSearchParams(window.location.search);
    const mode = urlParams.get('mode');
    currentSoundEngineId = urlParams.get('id');

    // Function to convert Hex to RGBA
    function hexToRgba(hex, alpha = 1) {
        let r = 0, g = 0, b = 0;
        if (hex.length === 7) {
            r = parseInt(hex.slice(1, 3), 16);
            g = parseInt(hex.slice(3, 5), 16);
            b = parseInt(hex.slice(5, 7), 16);
        }
        return `rgba(${r},${g},${b},${alpha})`;
    }

    // Update the border color of the Color 1 section
    function updateBorderColor() {
        const rgbaColor = hexToRgba(color1Picker.value, alpha1Picker.value);
        color1Section.style.borderColor = rgbaColor;
        color1Input.value = rgbaColor;
        alpha1Value.innerText = alpha1Picker.value;
    }

    function updateBorderColor2() {
        const rgbaColor = hexToRgba(color2Picker.value, alpha2Picker.value);
        color2Section.style.borderColor = rgbaColor;
        color2Input.value = rgbaColor;
        alpha2Value.innerText = alpha2Picker.value;
    }

    // Event listeners for color pickers
    color1Picker.addEventListener('input', updateBorderColor);
    alpha1Picker.addEventListener('input', updateBorderColor);
    color2Picker.addEventListener('input', updateBorderColor2);
    alpha2Picker.addEventListener('input', updateBorderColor2);

    // Initial call to set border color
    updateBorderColor();
    updateBorderColor2();

    // Handle mode logic and load sound engine details
    if (!currentSoundEngineId || mode === 'create') {
        formTitle.innerText = 'Create a Sound Engine';
        toggleViewMode(true);
    } else if (mode === 'edit' && currentSoundEngineId) {
        isEditMode = true;
        formTitle.innerText = 'Edit Sound Engine';
        loadSoundEngineDetails(currentSoundEngineId);
    } else if (mode === 'soundEngine' && currentSoundEngineId) {
        formTitle.innerText = 'Sound Engine Details';
        loadSoundEngineDetails(currentSoundEngineId);
    }

    editButton.addEventListener('click', function() {
        toggleViewMode(true);
    });

    cancelButton.addEventListener('click', function() {
        if (isEditMode) {
            loadSoundEngineDetails(currentSoundEngineId);
            toggleViewMode(false);
        } else {
            soundEngineForm.reset();
            soundEngineImagePreviewForm.src = '';
            soundEngineImagePreviewForm.style.display = 'none';
            toggleViewMode(false);
        }
    });

    backButton.addEventListener('click', function() {
        window.location.href = '/voyage';
    });

    // Image preview functionality
    soundEngineImageInput.addEventListener('change', function(event) {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = function(e) {
                soundEngineImagePreviewForm.src = e.target.result;
                soundEngineImagePreviewForm.style.display = 'block';
            };
            reader.readAsDataURL(file);
        } else {
            soundEngineImagePreviewForm.src = '';
            soundEngineImagePreviewForm.style.display = 'none';
        }
    });

    // Function to handle form submission
soundEngineForm.addEventListener('submit', function(event) {
    event.preventDefault();

    const developerUsername = document.getElementById('developerUsername').value.trim();
    const soundEngineName = document.getElementById('soundEngineName').value.trim();
    const color1 = color1Input.value.trim();
    const color2 = color2Input.value.trim();
    const sonificationState = document.getElementById('sonificationState').value;
    const availability = document.getElementById('availability').value;
    const credits = document.getElementById('credits').value.trim();

    if (!developerUsername || !soundEngineName || !color1 || !color2 || !sonificationState) {
        showToast('Please fill in all required fields.', 'error');
        return;
    }

    const formData = new FormData();
    formData.append('ownerId', userId);
    formData.append('availability', availability);
    formData.append('developerUsername', developerUsername);
    formData.append('soundEngineName', soundEngineName);
    formData.append('color1', color1);
    formData.append('color2', color2);
    formData.append('xParam', JSON.stringify({ label: 'Speed', min: -100, max: 100, initValue: 1 }));
    formData.append('yParam', JSON.stringify({ label: 'Tremolo', min: -100, max: 100, initValue: 0 }));
    formData.append('zParam', JSON.stringify({ label: 'SpaceReverb', min: -100, max: 100, initValue: 0 }));
    formData.append('sonificationState', sonificationState);
    formData.append('credits', credits);

    // If no new image is uploaded, include the existing image path
    if (!soundEngineImageInput.files[0] && existingSoundEngine.soundEngineImage) {
        formData.append('existingImagePath', existingSoundEngine.soundEngineImage);
    } else if (soundEngineImageInput.files[0]) {
        formData.append('soundEngineImage', soundEngineImageInput.files[0]);
    }

    // If no new JSON file is uploaded, include the existing JSON file path
    if (!soundEngineFileInput.files[0] && existingSoundEngine.soundEngineFile) {
        formData.append('existingJsonFilePath', existingSoundEngine.soundEngineFile);
    } else if (soundEngineFileInput.files[0]) {
        formData.append('soundEngineFile', soundEngineFileInput.files[0]);
    }

    let apiEndpoint = 'http://media.maar.world:3001/api/soundEngines';
    let method = 'POST'; // Default method for creating a new sound engine

    if (isEditMode && currentSoundEngineId) {
        apiEndpoint += `/${currentSoundEngineId}`;
        method = 'PUT'; // Use PUT method for updating an existing sound engine
    }

    // Disable form inputs while submitting
    disableFormInputs(true);

    const xhr = new XMLHttpRequest();
    xhr.open(method, apiEndpoint, true);

    // Update progress bar during upload
    xhr.upload.onprogress = function(event) {
        if (event.lengthComputable) {
            const percentComplete = (event.loaded / event.total) * 100;
            document.getElementById('progress').style.width = percentComplete + '%';
        }
    };

    // Handle response
    xhr.onload = function() {
        if (xhr.status === 200 || xhr.status === 201) {
            const response = JSON.parse(xhr.responseText);
            if (response.success) {
                showToast(response.message || (isEditMode ? 'Sound Engine updated successfully!' : 'Sound Engine created successfully!'), 'success');
                if (isEditMode) {
                    loadSoundEngineDetails(currentSoundEngineId);
                    toggleViewMode(false);
                } else {
                    window.location.href = `/voyage/soundEngine?mode=soundEngine&id=${response.soundEngine._id}`;
                }
            } else {
                showToast(response.message || 'Failed to save sound engine.', 'error');
            }
        } else {
            showToast('An error occurred while saving the sound engine.', 'error');
        }

        // Re-enable form inputs after completion
        disableFormInputs(false);
    };

    // Handle upload error
    xhr.onerror = function() {
        showToast('An error occurred while uploading the sound engine.', 'error');
        disableFormInputs(false);
    };

    xhr.send(formData);
});


    // Function to disable or enable form inputs
    function disableFormInputs(disable) {
        const inputs = soundEngineForm.querySelectorAll('input, textarea, select, button');
        inputs.forEach(input => {
            input.disabled = disable;
        });
    }

    // Toggle between view and edit modes
    function toggleViewMode(editMode) {
        if (editMode) {
            soundEngineView.style.display = 'none';
            soundEngineForm.style.display = 'block';
        } else {
            soundEngineView.style.display = 'block';
            soundEngineForm.style.display = 'none';
        }
    }

let existingSoundEngine = null;  // Define existingSoundEngine at the top

// Load sound engine details
function loadSoundEngineDetails(soundEngineId) {
    fetch(`http://media.maar.world:3001/api/soundEngines/${soundEngineId}?userId=${userId}`)
        .then(response => response.json())
        .then(data => {
            console.log('Received Sound Engine Data:', data);

            if (data.success && data.soundEngine) {
                existingSoundEngine = data.soundEngine; // Populate existingSoundEngine with the data
                populateViewMode(data.soundEngine);
                populateFormMode(data.soundEngine);

                // Log the ownerId and userId for comparison
                console.log('Logged-in userId:', userId);
                console.log('Sound Engine ownerId:', data.soundEngine.ownerId._id);  // Access the _id field from ownerId

                // Check if the logged-in user is the owner of the sound engine
                isOwner = data.soundEngine.ownerId._id === userId;
                console.log('Is user the owner? ', isOwner);

                // Show the edit button only if the user is the owner
                if (isOwner) {
                    editButton.style.display = 'block';
                } else {
                    editButton.style.display = 'none';
                }
            } else {
                showToast(data.message || 'Failed to load sound engine details.', 'error');
            }
        })
        .catch(error => {
            console.error('An error occurred while loading sound engine details:', error);
            showToast('An error occurred while loading sound engine details.', 'error');
        });
}


    // Populate view mode with sound engine details
    function populateViewMode(soundEngine) {
        document.getElementById('displayDeveloperUsername').innerText = soundEngine.developerUsername;
        document.getElementById('displaySoundEngineName').innerText = soundEngine.soundEngineName;
        document.getElementById('displayColor1').innerText = soundEngine.color1;
        document.getElementById('displayColor2').innerText = soundEngine.color2;
        document.getElementById('displaysonificationState').innerText = soundEngine.sonificationState ? 'Enabled' : 'Disabled';
        document.getElementById('displayAvailability').innerText = soundEngine.availability;
        document.getElementById('displayCredits').innerText = soundEngine.credits || 'No credits provided';

        if (soundEngine.soundEngineImage) {
            const imageURL = `https://media.maar.world${encodeURI(soundEngine.soundEngineImage)}`;
            soundEngineImagePreview.src = imageURL;
            soundEngineImagePreview.style.display = 'block';
        } else {
            soundEngineImagePreview.style.display = 'none';
        }
    }

    // Populate form fields for edit mode
    function populateFormMode(soundEngine) {
        const baseUrl = 'https://media.maar.world';

        document.getElementById('developerUsername').value = soundEngine.developerUsername;
        document.getElementById('soundEngineName').value = soundEngine.soundEngineName;
        document.getElementById('color1').value = soundEngine.color1;
        document.getElementById('color2').value = soundEngine.color2;
        document.getElementById('availability').value = soundEngine.availability;
        document.getElementById('sonificationState').value = soundEngine.sonificationState;
        document.getElementById('credits').value = soundEngine.credits || '';

        // Show existing image
        if (soundEngine.soundEngineImage) {
            const fullImageUrl = `${baseUrl}${soundEngine.soundEngineImage}`;
            document.getElementById('existingImage').style.display = 'block';
            document.getElementById('existingImageLink').href = fullImageUrl;
            document.getElementById('existingImageLink').textContent = soundEngine.soundEngineImage.split('/').pop();
            document.getElementById('soundEngineImagePreviewForm').src = fullImageUrl;
            document.getElementById('soundEngineImagePreviewForm').style.display = 'block';
        } else {
            document.getElementById('soundEngineImagePreviewForm').style.display = 'none';
        }

        // Show existing JSON file
        if (soundEngine.soundEngineFile) {
            const fullJsonUrl = `${baseUrl}${soundEngine.soundEngineFile}`;
            document.getElementById('existingJsonFile').style.display = 'block';
            document.getElementById('existingJsonLink').href = fullJsonUrl;
            document.getElementById('existingJsonLink').textContent = soundEngine.soundEngineFile.split('/').pop();
        } else {
            document.getElementById('existingJsonFile').style.display = 'none';
        }

        // Update the color pickers and alpha sliders based on stored RGBA values
        const [color1R, color1G, color1B, color1A] = extractRGBAValues(soundEngine.color1);
        const [color2R, color2G, color2B, color2A] = extractRGBAValues(soundEngine.color2);
        
        color1Picker.value = rgbToHex(color1R, color1G, color1B);
        alpha1Picker.value = color1A;

        color2Picker.value = rgbToHex(color2R, color2G, color2B);
        alpha2Picker.value = color2A;
        
        updateBorderColor();
        updateBorderColor2();
    }

    // Helper to extract RGBA values from a string like "rgba(255, 51, 204, 0.5)"
    function extractRGBAValues(rgbaString) {
        const rgbaMatch = rgbaString.match(/rgba?\((\d+),\s*(\d+),\s*(\d+),?\s*(\d*(?:\.\d+)?)?\)/);
        if (rgbaMatch) {
            const [, r, g, b, a = 1] = rgbaMatch;
            return [parseInt(r), parseInt(g), parseInt(b), parseFloat(a)];
        }
        return [0, 0, 0, 1]; // default values if parsing fails
    }

    // Helper to convert RGB values to hex
    function rgbToHex(r, g, b) {
        return `#${((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1).toUpperCase()}`;
    }

    // Toast function for showing messages
    function showToast(message, type = 'success') {
        const toastContainer = document.getElementById('toastContainer');
        const toast = document.createElement('div');
        const toastId = `toast_${Date.now()}`;
        toast.classList.add('toast');
        toast.setAttribute('id', toastId);
        if (type === 'success') {
            toast.classList.add('success');
        } else if (type === 'error') {
            toast.classList.add('error');
        }
        toast.textContent = message;
        toastContainer.appendChild(toast);

        setTimeout(() => {
            toast.classList.add('show');
        }, 100);

        setTimeout(() => {
            toast.classList.remove('show');
            setTimeout(() => {
                const toastElem = document.getElementById(toastId);
                if (toastElem) {
                    toastElem.remove();
                }
            }, 500);
        }, 3000);
    }

    // Validation for Min, Max, and Initial Values
    const params = ['x', 'y', 'z'];
    
    params.forEach(param => {
        const minInput = document.getElementById(`${param}ParamMin`);
        const maxInput = document.getElementById(`${param}ParamMax`);
        const initInput = document.getElementById(`${param}ParamInit`);

        const validateInitValue = () => {
            let min = parseInt(minInput.value, 10);
            let max = parseInt(maxInput.value, 10);
            let init = parseInt(initInput.value, 10);

            if (min < -100) min = -100;
            if (min > 100) min = 100;
            if (max < -100) max = -100;
            if (max > 100) max = 100;

            minInput.value = min;
            maxInput.value = max;

            const realMin = Math.min(min, max);
            const realMax = Math.max(min, max);

            if (init < realMin) init = realMin;
            if (init > realMax) init = realMax;

            initInput.value = init;
        };

        minInput.addEventListener('input', validateInitValue);
        maxInput.addEventListener('input', validateInitValue);
        initInput.addEventListener('input', validateInitValue);
    });
});
</script>
