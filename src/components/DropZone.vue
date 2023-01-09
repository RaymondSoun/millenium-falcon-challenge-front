<template>
    <div>
        <header>
        <p>
            <font-awesome-icon :icon="['fa-solid', 'fa-jedi']" /> Intercepted data
        </p>
        </header>
        <div
        @dragenter.prevent="toggleActive"
        @dragleave.prevent="toggleActive"
        @dragover.prevent
        @drop.prevent="toggleActive"
        :class="{ 'active-dropzone': active }"
        class="dropzone"
        >
            <font-awesome-icon id="textIcon" :icon="['fa', 'fa-file-text']" />
            <span><b>Drag and drop</b> intercepted data here</span>
            <!-- <span> OR </span> -->
            <label for="dropzoneFile">or <span style="color:#41b883; text-decoration: underline;">browse</span> to upload</label>
            <input type="file" id="dropzoneFile" class="dropzoneFile"/>
        </div>
    </div>
    
</template>

<script>
import { ref } from 'vue';
import { library } from '@fortawesome/fontawesome-svg-core';
import { faCloudUpload, faFileText, faJedi } from '@fortawesome/free-solid-svg-icons';
library.add(faCloudUpload)
library.add(faFileText)
library.add(faJedi)
export default {
    name:"DropZone",
    setup(){
        const active = ref(false)

        const toggleActive = () => {
            active.value = !active.value
        }

        return {active, toggleActive }
    }
}
</script>

<style>

span{
    color : darkgray
}

header {
  background: #4db6ac;
  text-align: center;
  font-size: 30px;
  padding: 20px 0;
  color: #fff;
  border-top-left-radius: 5px 5px;
  border-top-right-radius: 5px 5px;
}

.dropzone{
    width: 400px;
    height: 200px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* row-gap: 16px; */
    
    background-color: #fff;
    /* transition: 0.3s ease all; */
    border-bottom-left-radius: 5px 5px;
    border-bottom-right-radius: 5px 5px;

    
}

label{
    /* padding: 8px 12px; */
    color: darkgray;
    /* background-color: #41b883; */
    /* transition: 0.3s ease all;         */
}

input{
    display: none;
}

label span{
    cursor : pointer;
}

.active-dropzone{
    color: white;
    border-color: white;
    border: 2px dashed #41b883;
    /* background-color: #41b883; */

    
}



span b{
    color:#41b883;
}

.active-dropzone label{
    background-color:#fff;
    /* color: #41b883; */
}

#textIcon{
    position:relative;
    font-size: 65px;
    color: lightgray;
    padding-bottom: 20px;

}

</style>