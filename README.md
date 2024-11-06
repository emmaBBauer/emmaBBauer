- 👋 Hi, I’m @emmaBBauer (primary Key)
- 👀 I’m interested in everything except coding. 
- 🌱 I’m currently learning jwt with Prof.VK
- 💞️ I’m looking to collaborate on nice projects. 
- 📫 How to reach me:  LinkedIn.  
- 😄 Pronouns: frontend/backend
- ⚡ Fun fact: You know that you are in a perfect relationship, when @JsonBackReference has two meanings ;)



export const findUser = (email:string, password:string):IUser | undefined =>
{
    const user:IUser | undefined= users_mock.find( (u:IUser) => {
        console.log("*****");
        console.log("mail ==",email);
        console.log("password ==",password);
        let ok =true;
        console.log("u ==",u);
        console.log("u.email !== email ==",u.email !== email);
        if (u.email !== email)
        {
            ok=false;
        }
        console.log("u.password !== password ==",u.password !== password);
        if (u.password !== password) {
            ok=false;
        }
        console.log("ok:",ok);
        return ok? u : null;
    });

    return user;
}
