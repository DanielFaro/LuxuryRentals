# Luxury Rentals

## Summary - 
My goal was to create a straightforward luxury vehicle rental site for Los Angeles.
For UI design I went with simple boxes in a grid format. I used colors and buttons more easily identifyable by the color blind.
Being 'red-green' colorblind myself, I belive every section and button are appropriate. In addition I added drop shadow and
increased scale on hover for better clarity and interactivity. I decided to have a fixed navbar at the page top, which contains
section links. This way a user knows what the page contains on first entry, and I also added autoscrolling so a user can navigate
anywhere on the page through the navbar. I put a footer at the page bottom, only visible when fully scrolled down. This was to
prevent clutter as we already have a fixed navbar. I added social network icons and common section links which would need to be 
added in the future. I am happy with the simple filtering I provided in the rental section. Data is first retrieved from port:5000
which is running an express server, and fetching data from mongodb. This data is then set to component state and filtered in the 
VehicleList component. 

There are a few additions I would make 
if given the chance. For one I would add typescript to ensure proper data structures. Instead of styled components, I could have used
tailwind, but did not as I am only slightly familiar with TailwindCSS and would not have guaranteed finishing application functionality.
I would have liked to add resizing/breakpoints for different screen sizes. In addition, upon adding more pages, Next.js could be used
for navigation using Link components. For a fully loaded render more quickly, a static page could be served from the backend. 
Thank you.


## Instructions - 
To run the codebase, clone the repo and type 'npm run start' or try it on the linked github pages.
[Try Me](https://danielfaro.github.io/LuxuryRentals/)

   
## Library choices

### State Management - 

**Zustand** - Redux seemed like overkill for a small application and I wantedt to challenge myself by trying a new library. I chose zustand due to the small boilerplate and straightforward usage. Some local state was used e.g. the search bar uses a searchValue for the input, which is then sent to the store and set in global state as 'searchTerm'. 

### Visualization - 

**ChartJS with recharts** - I had used ChartJS in the past and with some minor research was able to implement a scatter plot. It also seemed more straight forward than d3, which I don't have much experience with.

### Styling - 

**Styled-Components** - I decided to use styled-components for all accept the table component,
which had a more complicated structure. I decided to create a separate css file for the table to 
not end up with an enormous main Table component which would decrease readability. Styled-components
provided me with enough functionality without having to rely on prebuilt component libraries and global themes as with e.g. MaterialUI.

## Things I'm Proud of - 
I used memoization where I could, but due to having to fit everything within a timeframe, there are definite ways to improve performance. (see possible enhancements)
I am a fan of the dog image showing on hover in the tooltip. I found this a good way to decrease the table row height and show more data per page.
I think I chose a good set of data to visualize, especially interesting to see the chart after searching.

## Possible Enhancements - 
 
1. Lazy loading images
2. More memoization
3. I would ideally get rid of the search button and add debouncing to prevent constant resetting of the filter term.



## Available Scripts

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.


The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!
