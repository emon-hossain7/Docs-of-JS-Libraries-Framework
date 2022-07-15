# JavaScript Using Method And Example

### what is javaScript?
- JavaScript is a dynamic programming language that's used for web development, web applications, game development, and lots more. JavaScript language is used both on the client-side and server-side allowing you to make web pages interactive.
### Why use JavaScript?
- Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.


List of :

- [TemplateString](#TemplateString)
- [ArrowFunction](#ArrowFunction)
- [useSignInWithEmailAndPassword](#usesigninwithemailandpassword)
- [useSignInWithApple](#usesigninwithapple)
- [useSignInWithFacebook](#usesigninwithfacebook)
- [useSignInWithGithub](#usesigninwithgithub)
- [useSignInWithGoogle](#usesigninwithgoogle)
- [useSignInWithMicrosoft](#usesigninwithmicrosoft)
- [useSignInWithTwitter](#usesigninwithtwitter)
- [useSignInWithYahoo](#usesigninwithyahoo)
- [useUpdateEmail](#useupdateemail)
- [useUpdatePassword](#useupdatepassword)
- [useUpdateProfile](#useupdateprofile)
- [useSendPasswordResetEmail](#usesendpasswordresetemail)
- [useSendEmailVerification](#usesendemailverification)

### TemplateString
<details>
<summary>
  <h3>What is Template String?</h3>
</summary>
<br >
  
- Template String is

</details>



```js
const numbers = [87, 342, 54, 23, 56, 234];
const student = {
    name: 'sakib Khan',
    age: 32,
    movies: ['king khan', 'dhakar masta,', 'aynabaji']
};

const about = `My name is ${student.name} age of ${student.age} has number ${numbers[2]} also liked mvies ${student.movies[2]}`;
console.log(about)
```

### ArrowFunction
<details>
<summary>
  <h3>What is Arrow Function?</h3>
</summary>
<br >
  
- Arrow Function is

</details>



```js
const numbers = [87, 342, 54, 23, 56, 234];
const student = {
    name: 'sakib Khan',
    age: 32,
    movies: ['king khan', 'dhakar masta,', 'aynabaji']
};

const about = `My name is ${student.name} age of ${student.age} has number ${numbers[2]} also liked mvies ${student.movies[2]}`;
console.log(about)
```

Create a user with email and password. Wraps the underlying `firebase.auth().createUserWithEmailAndPassword` method and provides additional `loading` and `error` information.

The `useCreateUserWithEmailAndPassword` hook takes the following parameters:

- `auth`: `auth.Auth` instance for the app you would like to monitor
- `options`: (optional) `Object` with the following parameters:
  - `emailVerificationOptions`: (optional) `auth.ActionCodeSettings` to customise the email verification
  - `sendEmailVerification`: (optional) `boolean` to trigger sending of an email verification after the user has been created

Returns:

- `createUserWithEmailAndPassword(email: string, password: string)`: a function you can call to start the registration
- `user`: The `User` if the user was created or `undefined` if not
- `loading`: A `boolean` to indicate whether the the user creation is processing
- `error`: Any `Error` returned by Firebase when trying to create the user, or `undefined` if there is no error

#### Full Example

```jsx
import { useCreateUserWithEmailAndPassword } from 'react-firebase-hooks/auth';

const SignIn = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [
    createUserWithEmailAndPassword,
    user,
    loading,
    error,
  ] = useCreateUserWithEmailAndPassword(auth);

  if (error) {
    return (
      <div>
        <p>Error: {error.message}</p>
      </div>
    );
  }
  if (loading) {
    return <p>Loading...</p>;
  }
  if (user) {
    return (
      <div>
        <p>Registered User: {user.email}</p>
      </div>
    );
  }
  return (
    <div className="App">
      <input
        type="email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      <input
        type="password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
      />
      <button onClick={() => createUserWithEmailAndPassword(email, password)}>
        Register
      </button>
    </div>
  );
};
```

### useSignInWithEmailAndPassword

```js
const [
  signInWithEmailAndPassword,
  user,
  loading,
  error,
] = useSignInWithEmailAndPassword(auth);
```

Login a user with email and password. Wraps the underlying `auth.signInWithEmailAndPassword` method and provides additional `loading` and `error` information.

The `useSignInWithEmailAndPassword` hook takes the following parameters:

- `auth`: `Auth` instance for the app you would like to monitor

Returns:

- `signInWithEmailAndPassword(email: string, password: string)`: a function you can call to start the login
- `user`: The `auth.User` if the user was logged in or `undefined` if not
- `loading`: A `boolean` to indicate whether the the user login is processing
- `error`: Any `Error` returned by Firebase when trying to login the user, or `undefined` if there is no error

#### Full Example

```jsx
import { useSignInWithEmailAndPassword } from 'react-firebase-hooks/auth';

const SignIn = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [
    signInWithEmailAndPassword,
    user,
    loading,
    error,
  ] = useSignInWithEmailAndPassword(auth);

  if (error) {
    return (
      <div>
        <p>Error: {error.message}</p>
      </div>
    );
  }
  if (loading) {
    return <p>Loading...</p>;
  }
  if (user) {
    return (
      <div>
        <p>Signed In User: {user.email}</p>
      </div>
    );
  }
  return (
    <div className="App">
      <input
        type="email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      <input
        type="password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
      />
      <button onClick={() => signInWithEmailAndPassword(email, password)}>
        Sign In
      </button>
    </div>
  );
};
```

### useSignInWithApple

```js
const [signInWithApple, user, loading, error] = useSignInWithApple(auth);
```

Login a user with Apple Authenticatiton. Wraps the underlying `auth.signInWithPopup` method with the `auth.OAuthProvider` and provides additional `loading` and `error` information.

The `useSignInWithApple` hook takes the following parameters:

- `auth`: `Auth` instance for the app you would like to monitor

Returns:

- `signInWithApple(scopes: string[], customOAuthParameters: auth.CustomParameters)`: a function you can call to start the login
- `user`: The `auth.User` if the user was logged in or `undefined` if not
- `loading`: A `boolean` to indicate whether the the user login is processing
- `error`: Any `Error` returned by Firebase when trying to login the user, or `undefined` if there is no error

#### Full example

See [social login example](#social-login-example)

### useSignInWithFacebook

```js
const [signInWithFacebook, user, loading, error] = useSignInWithFacebook(auth);
```

Login a user with Facebook Authenticatiton. Wraps the underlying `auth.signInWithPopup` method with the `auth.OAuthProvider` and provides additional `loading` and `error` information.

The `useSignInWithApple` hook takes the following parameters:

- `auth`: `Auth` instance for the app you would like to monitor

Returns:

- `signInWithFacebook(scopes: string[], customOAuthParameters: auth.CustomParameters)`: a function you can call to start the login
- `user`: The `auth.User` if the user was logged in or `undefined` if not
- `loading`: A `boolean` to indicate whether the the user login is processing
- `error`: Any `Error` returned by Firebase when trying to login the user, or `undefined` if there is no error

#### Full example

See [social login example](#social-login-example)

<div class="overflow-x-auto">
  <table class="table w-full">
    <!-- head -->
    <thead>
      <tr>
        <th></th>
        <th>Name</th>
        <th>Job</th>
        <th>Favorite Color</th>
      </tr>
    </thead>
    <tbody>
      <!-- row 1 -->
      <tr>
        <th>1</th>
        <td>Cy Ganderton</td>
        <td>Quality Control Specialist</td>
        <td>Blue</td>
      </tr>
      <!-- row 2 -->
      <tr>
        <th>2</th>
        <td>Hart Hagerty</td>
        <td>Desktop Support Technician</td>
        <td>Purple</td>
      </tr>
      <!-- row 3 -->
      <tr>
        <th>3</th>
        <td>Brice Swyre</td>
        <td>Tax Accountant</td>
        <td>Red</td>
      </tr>
    </tbody>
  </table>
</div>
