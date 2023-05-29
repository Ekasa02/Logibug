<template>
  <div
    class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex sm:items-center sm:justify-center font-['monserrat']"
  >
    <div>
      <div class="bg-white rounded-lg shadow-lg">
        <div class="pt-4">
          <div class="flex">
            <h1
              class="font-['Montserrat'] font-bold text-2xl sm:pr-[300px] pl-5"
            >
              Add result
            </h1>
            <img src="./svg/CloseCircle.svg" class="pr-4" />
          </div>
          <hr class="border-gray-300 my-4 w-full" />
        </div>
        <div class="pl-5 pr-5">
          <div class="relative">
            <label
              class="block font-['Montserrat'] font-bold text-[14px] mb-2"
              for="Actually"
            >
              Actually
            </label>
            <input
              id="Actually"
              class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
              type="text"
              placeholder="Actually"
            />
          </div>
          <div class="pt-[15px] relative">
            <label
              class="block font-['Montserrat'] font-bold text-[14px] mb-2"
              for="note"
            >
              Note
            </label>
            <textarea
              id="note"
              class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
              placeholder="Note"
            >
            </textarea>
          </div>
          <div>
            <div class="pt-[15px] relative">
              <label
                class="block font-['Montserrat'] font-bold text-[14px] mb-2"
                for="project-name"
              >
                State
              </label>
              <div class="relative" >
                
                <select
                  id="project-name"
                  v-model="newItem.type_test"
                  required
                  class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" 
                  
                >
                  <option value="" disabled selected>Select an option</option>
                  <option value="manual">Manual</option>
                  <option value="automatic">Automatic</option>
                </select>
                
                <div
                  class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none"
                >
                  <svg
                    class="w-4 h-4 text-gray-700"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path d="M6 9l6 6 6-6"></path>
                  </svg>
                </div>
              </div>
              <div class="relative py-2" >
                
                <select
                  id="project-name"
                  v-model="newItem.type_test"
                  required
                  class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" 
                  
                >
                  <option value="" disabled selected>Select an option</option>
                  <option value="manual">Manual</option>
                  <option value="automatic">Automatic</option>
                </select>
                
                <div
                  class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none"
                >
                  <svg
                    class="w-4 h-4 text-gray-700"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path d="M6 9l6 6 6-6"></path>
                  </svg>
                </div>
              </div>
              <div class="relative" >
                
                <select
                  id="project-name"
                  v-model="newItem.type_test"
                  required
                  class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" 
                  
                >
                  <option value="" disabled selected>Select an option</option>
                  <option value="manual">Manual</option>
                  <option value="automatic">Automatic</option>
                </select>
                
                <div
                  class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none"
                >
                  <svg
                    class="w-4 h-4 text-gray-700"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path d="M6 9l6 6 6-6"></path>
                  </svg>
                </div>
              </div>
            </div>
            <!-- <div class="relative">
                            <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="result-state">
                                State
                            </label>
                            <div class="flex items-center">
                                <input id="result-state"
                                    class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                    type="text" placeholder="Result state" />
                                <img src="./svg/DropDown.svg" class="absolute right-2" />
                            </div>
                            <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="priority">

                            </label>
                            <div class="flex items-center">
                                <input id="priority"
                                    class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                    type="text" placeholder="Priority" />
                                <img src="./svg/DropDown.svg" class="absolute right-2" />
                            </div>
                            <label class="block font-['Montserrat'] font-bold text-[14px] mb-2" for="severity">

                            </label>
                            <div class=" flex items-center">
                                <input id="severity"
                                    class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                    type="text" placeholder="Severity" />
                                <img src="./svg/DropDown.svg" class="absolute right-2" />
                            </div>
                        </div> -->
          </div>
          <div class="">
            <div class="pt-[15px] font-['Montserrat']">
              <h1 class="block font-bold text-[14px] mb-2">Attacment</h1>
              <p class="pb-2">
                Max file size is 2mb. Supported files are jpg, jpeg, png
              </p>
              <div class="rounded p-4" style="border: dashed 1px #c9c5c5">
                <label for="input-file" class="cursor-pointer">
                  <input
                    id="input-file"
                    type="file"
                    accept="image/*"
                    class="hidden"
                  />
                  <img src="./svg/upload.svg" class="pl-56" />
                  <p class="pl-40 pt-2">Click to browse files</p>
                </label>
              </div>
            </div>
          </div>
          <div class="pt-4 pb-4">
            <div class="pt-9 pb-10">
              <button
                class="font-['Montserrat'] text-white bg-[#554AF0] font-semibold py-2 px-5 rounded"
              >
                Save
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newItem: {
        name: '',
        description: '',
        type_test: 'web',
        platform: 'manual',
      },
    }
  },
}
</script>
