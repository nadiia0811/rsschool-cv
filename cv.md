# Nadiia Krzesinska
### Junior Web Developer

#### **Contacts:** 
- Phone: +48 733 508 511
- E-mail: nb1985@ukr.net
- Discord: @Nadiia
#### **About me:**
I am a junior web developer with a solid foundation in JavaScript, HTML, CSS, and React. My proactive approach to learning and my experience in building responsive and visually appealing web applications have equipped me with the skills to tackle complex challenges effectively. I thrive in collaborative environments, where I can contribute to team success and continuously enhance my skills. My passion for web development drives me to stay updated with the latest trends, making me a valuable addition to your team.
#### **Tech Skills:**
##### Frontend:
- JavaScript (ES6+) 
- React + TypeScript 
- CSS
- HTML
- Tailwind 
- Framer Motion, Shadcn, Lucide and other libraries
##### **Backend:** 
- NodeJS, Express
##### **Data bases:**
- MongoDB, MySQL
#### **Soft Skills:**
- I can work effectively both independently and collaboratively in a team environment
- Time management
- Continuous learning
#### **Code example:**
```sh
export const useGetMyUser = () => {
  const { getAccessTokenSilently } = useAuth0();
  const getMyUserRequest = async (): Promise<User> => {
  const accessToken = await getAccessTokenSilently();

  const response = await fetch(`${API_BASE_URL}/api/my/user`, {
    method: "GET",
    headers: {
        Authorization: `Bearer ${accessToken}`,
        "Content-Type": "application/json"
    },   
  });

  if(!response.ok) {
    throw new Error("Failed get user info");
  }

  return response.json();
  };

  const { data: currentUser, isPending, error} = useQuery({
        queryKey: ["fetchCurrentUser"], 
        queryFn: getMyUserRequest});
  if(error) {
    toast.error(error.toString());
  }

  return { currentUser, isPending };
}
```
##### **Code explanation:**
This is a custom React hook designed to retrieve the current user's information. It uses the fetch API to perform a 'GET' request to the backend, which in turn queries MongoDB for the relevant user data. The hook returns an object containing two properties: currentUser, which holds the current user's data, and isLoading, a boolean value that indicates whether the data is still loading. This hook helps streamline data fetching in my application, making it more organized and reusable across different components.
You can see how the application works by visiting: [https://mern-food-ordering-app-frontend-c7fh.onrender.com](https://mern-food-ordering-app-frontend-c7fh.onrender.com)
#### **Education and Experience:**
- Course: Programming for Beginners (Brain Academy, Zaporizhzhia)
- High School of Information Technologies and Management (Rzeszów, Poland)
- W3School
- Free Code Camp courses
- Practical JavaScript - Advanced Level (Udemy)
- JavaScript + React: Full Course from Zero to Advanced (Ivan Petrichenko, Udemy)

In my portfolio I have projects: 
- E-commerce: An application that allows users to register, log in, add and delete products from their cart, retrieve products from the database upon logging in, and sort products by price.
- Food Ordering App: A full-stack application featuring user authentication with Auth0, user profile management, restaurant and menu creation, order management, and payment processing via Stripe.
#### **English Level:** B1