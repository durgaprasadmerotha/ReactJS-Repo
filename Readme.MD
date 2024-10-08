# ReactJs

ReactJS ek JavaScript library hai jo mainly UI (User Interface) banane ke liye use hoti hai. Yeh Facebook ke ne banayi thi aur aaj yeh kaafi popular ho chuki hai single-page applications (SPA) banane ke liye.

ReactJS ko Facebook ke ek engineer Jordan Walke ne 2011 mein banaya tha. Us waqt Facebook apni website ke front-end issues face kar raha tha, jisme unko fast aur responsive UI banane mein dikkat aa rahi thi. Jordan Walke ne React ko is problem ko solve karne ke liye develop kiya tha. Pehle React ko Facebook ke newsfeed me use kiya gaya tha, aur baad mein Instagram me bhi implement kiya gaya.

2013 mein, Facebook ne React ko open-source kar diya, taaki baaki developers bhi isse use kar sakein. Aaj React ek widely used library ban chuki hai.

## 1. ReactJS kya hai?

React ek front-end library hai jo UI components ko efficiently banane aur manage karne ke liye use hoti hai. Yeh JavaScript aur JSX (JavaScript XML) ko use karke components create karti hai.

## 2. ReactJS ki zarurat kyun padti hai?

JavaScript frameworks aur libraries, jaise jQuery, use karte waqt code complexity badh jaati thi, especially jab ek large application banana hota tha. Is complexity ko reduce karne aur code ko modular aur maintainable banane ke liye React banayi gayi. Kuch reasons ye hain:

Component-based architecture: React me tumhara UI chhote components me divided hota hai. Har component independent hota hai aur apne aap ko handle kar sakta hai. Jaise buttons, forms, list items sab apne-apne components ban jaate hain.

Virtual DOM: React ek Virtual DOM ko use karta hai, jo ki real DOM ka ek light-weight copy hoti hai. Isse app fast rehti hai, kyunki React sirf wahi parts update karta hai jo change hue hain, poori page ko reload nahi karta.

Declarative syntax: React me tum apne UI ko describe karte ho, aur React us state ke basis pe UI ko update kar deta hai. Tumhe manually DOM manipulation karne ki zarurat nahi padti.

One-way data binding: React ek direction me data flow ko follow karta hai, jo ki bugs aur unexpected behavior ko reduce karta hai.

## 3. ReactJS ke advantages

Fast performance: Virtual DOM ki wajah se React fast rehta hai.
Reusability: Components ko baar baar reuse kar sakte ho, jo development ko faster aur efficient banata hai.
Community support: React ka bahut bada community support hai, to tumhe help easily mil jaati hai.

## 4. React me kaam kaise hota hai?

Tum ek component likhte ho.
Wo component, JSX return karta hai.
React wo JSX ko HTML me convert karta hai aur browser ko dikhata hai.
Agar state ya props change hoti hain, React sirf wahi part update karta hai jo change hua hai, isliye app fast rehti hai.

## 5. ReactJS ke basic concepts

Components: React ka sabse important concept hai "components." Yeh basically reusable building blocks hain jo tumhare UI ka part bante hain. Do tarah ke components hote hain:

Functional Components: Yeh ek simple JavaScript function hota hai jo HTML (JSX) return karta hai.
Class Components: Yeh JavaScript class hoti hai jo React.Component ko extend karti hai aur render method return karti hai. (Modern React me functional components zyada use hote hain with hooks.)
JSX (JavaScript XML): React me tum JavaScript ke andar HTML-like syntax use karte ho, jise JSX kehte hain. Yeh syntax ko more readable aur maintainable banata hai.


// jsx
function MyComponent() {
return <h1>Hello, World!</h1>;
}


Props (Properties): Props wo data hote hain jo ek component ko doosre component se pass hote hain. Yeh read-only hote hain aur immutable (change nahi hote).

State: State ek component ka internal data hota hai jo change ho sakta hai. Jab state update hoti hai, to component re-render hota hai. State ko handle karne ke liye hooks ka use hota hai jaise useState().


// jsx
const [count, setCount] = useState(0);


Hooks: Yeh React ke functions hain jo functional components me features jaise state aur lifecycle methods ko allow karte hain. Common hooks hain:
useState(): State manage karne ke liye.
useEffect(): Side effects jaise data fetch karne ya DOM updates ko handle karne ke liye.

## 6. Difference between RDOM and VDOM

1. Real DOM (RDOM):
Real DOM browser ka asli Document Object Model hai, jo web page ka structure ko represent karta hai.

JavaScript se jab bhi tum DOM ko manipulate karte ho (jaise kisi element ka content change karte ho), to puri DOM re-render hoti hai. Ye process slow hota hai, especially jab bade web pages hote hain.

Problems with RDOM:

Slow updates: RDOM pe har chhoti update ke liye poori DOM re-render hoti hai, jo performance ko degrade karta hai.
Expensive: DOM manipulation karna CPU-intensive hota hai, isliye zyada frequent changes se application slow ho sakta hai.

2. Virtual DOM (VDOM):
Virtual DOM ek light-weight copy hai jo React maintain karta hai. Ye DOM ka ek virtual representation hai, jo JavaScript object form mein hota hai.

Jab tum React me koi state ya data change karte ho, React pehle VDOM ko update karta hai, aur uske baad VDOM aur RDOM ke beech difference ko compare karta hai.

Is comparison process ko "diffing algorithm" kehte hain. Iske baad React sirf wahi specific parts update karta hai jo change hue hain, bina poori page ko reload kiye.

Advantages of VDOM:

Fast updates: VDOM efficiently update karta hai, kyunki sirf changed part ko RDOM me reflect karta hai, isliye performance better hoti hai.
Minimized re-renders: React sirf necessary updates karta hai, isse browser me minimum re-renders hote hain.

### Key Differences Between Real DOM and Virtual DOM

| *Feature*      | *Real DOM (RDOM)*                                              | *Virtual DOM (VDOM)*                                            |
| ---------------- | ---------------------------------------------------------------- | ----------------------------------------------------------------- |
| *Nature*       | Browser ki asli DOM                                              | React ka virtual representation of the DOM                        |
| *Speed*        | Slow updates and re-renders                                      | Fast updates, as sirf changed parts update hote hain              |
| *Re-rendering* | Pura DOM re-render hota hai                                      | Sirf jo parts change hue hain, unhi ko update karta hai           |
| *Performance*  | Heavy and slow, especially for large applications                | Efficient aur fast, especially for large applications             |
| *Memory Usage* | Less memory efficient, as every update involves DOM manipulation | More memory efficient, as comparison happens in virtual DOM first |
| *How it works* | Directly interacts with the browser DOM                          | First updates virtual DOM, then compares with real DOM            |

### Reconciliation

Reconciliation ReactJS ka ek process hai jisme Virtual DOM (VDOM) aur Real DOM (RDOM) ke beech differences ko compare karke sirf necessary updates ko apply kiya jata hai, bina poori DOM ko re-render kiye. React ke reconciliation process ki wajah se application fast aur efficient banti hai.

## 7. ReactJs and NextJs

nextJs ek framework hai. reactJs ko framework ke roop me use krne ke liye hi nextJs ka use reactJs ke sath kiya jata hai.

## 8. ReactJs installation and Vite

Vite ek modern build tool hai jo aapke React applications ko aur tez aur efficient banata hai. Jab aap create-react-app use karte ho, toh woh Webpack ka use karta hai, jo thoda slow ho sakta hai bade projects ke liye. Vite usi problem ko solve karne ke liye banaya gaya hai. Yah React ke liye bhi use hota hai aur iska kaafi faayda hai:

Vite Install Karne ke Reasons:
Faster Development: Vite development server ko instantaneously start karta hai, kyunki ye modules ko lazily load karta hai (sirf wahi files load hoti hain jo aapke code mein zarurat hoti hain). Jab ki Webpack-based tools poori application bundle karte hain, jo time leta hai.

Hot Module Replacement (HMR): Vite ka HMR kaafi fast hota hai, matlab jab aap code mein koi changes karte ho, toh woh turant browser mein reflect hota hai bina poori page ko reload kiye. Isse development experience kaafi smooth ho jata hai.

Faster Build Time: Vite build process mein bhi efficient hai. Ye modern ES module browser support ka faayda uthata hai aur optimized output generate karta hai, jo aapki production build ko kaafi fast banata hai.

Minimal Configuration: Vite ka configuration simple hota hai. Aapko Webpack jaisi heavy configuration files manage karne ki zarurat nahi padti.

1. [Open this website](https://vitejs.dev/guide/)
2. copy here.
   
   npm create vite@latest
   
3. create a folder
4. select react
5. select javascript
6. cd folder_name
7. npm install
8. code . (for move ito vs code)
9. npm run dev

## Primary Memory vs Secondary Memory

1. Primary Memory (Main Memory):
   Example: RAM (Random Access Memory).
   Speed: Very fast, as it is directly connected to the CPU.
   Storage Type: Volatile, meaning data is lost when the power is turned off.
   Purpose: Stores data that is actively being used or processed by the CPU.
   Capacity: Generally smaller (measured in GBs).
   Cost: More expensive per unit of storage compared to secondary memory.
   Role: Temporarily stores data and instructions that the CPU is currently using.
2. Secondary Memory (Auxiliary Memory):
   Example: Hard Drive, SSD, CD, USB drives.
   Speed: Slower compared to primary memory.
   Storage Type: Non-volatile, meaning data is retained even after the power is off.
   Purpose: Stores data and files long-term, even when not in use.
   Capacity: Larger (measured in TBs).
   Cost: Less expensive per unit of storage.
   Role: Provides long-term storage for data and applications.

Primary memory, ko secondary memory ya secondary ko primary ki tarah use nhi kiya ja skta hai. iski wajah to uper key points se samajh aa jati hai.
primary ko kisi bhi tarah se secondary ki tarah use nhi kr skte lekin secondary ko kuchh had tk primary ki tarah use kr skte hai.

### PC ya laptop lag ya hang karne ke kai reasons ho sakte hain. Yahan kuch common reasons aur unke solutions hain:

- Problem: Jab aap multiple applications ya heavy software use karte hain aur aapke paas sufficient RAM nahi hoti, toh system slow ho sakta hai.
- Solution: RAM upgrade karna ya unnecessary applications ko close karna.

#### Explaination

Jab aap kisi application ko open karte hain, toh wo application secondary memory (jaise hard drive ya SSD) se primary memory (RAM) mein load hoti hai. RAM ko fast access speed ki wajah se applications run karne ke liye use kiya jata hai, aur CPU in applications ko execute karta hai.

Jab aap ek saath kai applications ya high-power applications open karte hain, toh RAM ka space quickly fill ho jata hai kyunki RAM ki capacity limited hoti hai. Jab RAM full ho jati hai, operating system secondary memory ko virtual memory ke roop mein use karna shuru kar deta hai. Virtual memory secondary memory ka ek portion hota hai jo RAM se exceed ho chuki data ko store karta hai.

Lekin, secondary memory ki access speed RAM se bahut kam hoti hai. Iska matlab hai ki jab data RAM se secondary memory (virtual memory) mein swap hota hai, toh data ko access karne mein zyada samay lagta hai. Is slow access ki wajah se system ki performance slow ho jati hai, aur applications ko response time mein delay hota hai.

Agar system ki RAM aur virtual memory dono hi overloaded ho jati hain, toh aapko lag ya hang issues face karne padte hain. System hang kar sakta hai ya performance degrade ho sakti hai kyunki CPU ko data ko access karne mein zyada waqt lagta hai aur applications smoothly nahi chal pati hain.

Toh, jab RAM aur virtual memory overloaded hoti hai, tab system hang ya lag karne lagta hai, kyunki data access aur processing me delays aati hain.

## FPS (Frames Per Second)

Ye ek metric hai jo video ya animation ki smoothness aur quality ko measure karta hai. FPS batata hai ki ek second mein kitne frames (ya images) display kiye ja rahe hain. Zyada FPS ka matlab hai smoother aur more fluid motion, jabki kam FPS se motion choppy ya jerky lag sakta hai.

### Example:

24 FPS: Ye typical frame rate hota hai movies aur films ke liye. Ye cinematic look provide karta hai.
30 FPS: Ye standard frame rate hai jo TV shows aur many online videos mein use hota hai.
60 FPS: Ye common frame rate hai gaming aur high-definition videos ke liye jo smooth aur responsive experience provide karta hai.

#### Metric

Metric ek standardized unit hai jo kisi specific parameter ko measure karne ke liye use hota hai. Metrics ko quantitative data ko measure karne aur compare karne ke liye use kiya jata hai, aur ye specific performance indicators ya characteristics ko define karte hain.

