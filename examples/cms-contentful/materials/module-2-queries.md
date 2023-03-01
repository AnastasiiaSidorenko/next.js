query {  
  postCollection(limit: 3) {
    items {
      title
      slug
      excerpt
      date 
      coverImage {
        url
      }
      author {
        name
        picture {
          url
        }
      }
    }
  }
}

query {  
  authorCollection {
    items {
      name
      picture {
        url
      }
      linkedFrom {
        postCollection {
          items {
            title
          }
        }
      }
    }
  }
}

query($postId: String!) {  
  post(id: $postId) {
    title
  }
}