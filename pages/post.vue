<template>
    <Navbar />
    <div class="tw-relative tw-pt-10 tw-px-20">
        <div class="tw-flex tw-justify-center tw-text-5xl tw-font-bold tw-text-emerald-800 ">
            POST
         </div>   

          <!-- input search  -->
    <div class="tw-flex tw-items-center tw-gap-2 tw-pt-5">
      <input v-model="search" type="text" placeholder="Search"
        class="tw-border tw-border-light-gray-2 tw-rounded-md tw-h-[42px] tw-w-full tw-px-5">
      <Button label="Search" @click="searchPost" />
      <Button label="Clear" @click="getPostList" />
        </div>
    </div>
</template> 



<script>
const searchPost = () => {
  if (search.value.trim() === '') {
    getPostList()
    return
  }
  const searchTerm = search.value.toLowerCase()
  posts.value = posts.value.filter(post =>
    post.title.toLowerCase().includes(searchTerm) ||
    post.body.toLowerCase().includes(searchTerm)
  )
}
</script>
