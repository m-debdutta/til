{::options parse_block_html="true" /}

# 4th June, 2023

[Go to index](index.md)

## Today's activities

- Book reading
  - Foundation by Isaac Asimov (44 pages)
- Started making "Today I Learned notes"

## Today's Learning

- <details><summary markdown="span"> words I learned </summary>

    - shrivelled
    - trifling
    - courtiers
    - beetled 
    - chamberlains
    - morosely
    - canted
    - athwart
    - plummet
    - unregal
    - poppycock
    - peevishness
    - sardonic
    - conciliatory
    - wrangling
    - sardonically
    - blasphemous
    - queer
    - mummery 
    - peremptory
    - presentiments
    - dissident
    - vociferous
    - deputation
    - obscure 
    - crannies 
    - flummery
    - garbled
    - muffed
    - visicasters
    - impeached
    - frigid
    - reminiscently
    - sombrely
    - staggering
    - ebbing
    - pagenantry
    - herald
    - apoplexy
    - dowager
    - precarious
    - commode
    - contemptuously
    - interdict
    - blisterd
    - blazing 
    - coronet
    - buffeted
    - stricken
    - huskily
    - exultantly
    - sacrilege
    - acolyte
    - veneration
    - blasphemer
    - haggered
    - stolidly
    - spasmodically
    - prerogative
    - hitherto
    - prerogative
    - hysterically

  </details>

---

# 5th June, 2023

[Go to index](index.md)

## Today's activities

- Topics learned 
    - publishing an event
    - subscribing to an event
    - event emitter
    - createReadStream in fileSystem

## Today's learnings

- ### My event reader : 
    created a demo class which behaves like eventEmitter class.

  <details><summary markdown="span"> code snippet </summary>

  ```js
  class StdInp {
    constructor() {
      this.events = { data: [], end: [] };
    }

    on(eventName, callback) {
      this.events[eventName].push(callback);
    }

    start() {
      process.stdin.setEncoding("utf-8");
      const intervalId = setInterval(() => {
        const data = process.stdin.read();

        if (process.stdin._readableState.ended) {
          clearInterval(intervalId);
        }

        if (data) {
          this.events.data.forEach((callback) => 
          callback(data)
          );
        }
      }, 100);
    }
  }
  const stdInp = new StdInp();
  stdInp.on("data", callback);

  setTimeout(() => {
    stdInp.on("data", callback1);
  }, 2000);

  stdInp.start();
  ```
    </details>

---

# 6th June, 2023

[Go to index](index.md)

## Today's events
### Topics done : 
- npm - node process manager.

## Today I learned
- command - npm
  - options
      <details><summary markdown="span">init</summary>

      ```sh
      npm init
      ```
      </details> 
      
      <details><summary markdown="span">test</summary>

      ```sh
      npm test
      ```
      </details>

      <details><summary markdown="span">install</summary>

      ```sh
      npm install --save filePath or dependency name
      ```
      </details> 
  
---
# 7th June, 2023

[Go to index](index.md)

## Today's events

### - Book reading
  - Foundation by Isaac Asimov ( pages)

## Today's learnings 

- <details><summary markdown="span">Words learned</summary>

    - trespassed
    - unwittingly
    - deplorable
    - wince
    - scornful
    - veneration
    - interdict
    - intoned
  </details>
---
# 8th June, 2023

[Go to index](index.md)
---
# 9th June, 2023

[Go to index](index.md)

## Today's events
### Book reading
  - Foundation by Isaac Asimov (pages)
### Session
  - inheritance

## Today's learnings
  - bookReading
      - <details><summary markdown="span">Words learned</summary>

        </details>

  - inheritance
      - <details><summary markdown="span">define</summary>

        It is a concept of a class inheriting the methods and properties of another class. When a class inherit another class, the class that inherits a class is called a derived class and the class that is being inherited is called a base class.
        </details>

    - a [derived_class_name] is a [base_class_name]
    
      example - A Dog is an Animal (here Dog and Animal are class)
    - a base/parent class is inherited by using the keyword `extends`
    - when we write a derived class `super()` should be defined first inside a constructor. If constructor is not defined js manages it.
      <details><summary markdown="span">snipet</summary>

      ```js
      class Dog extends Animal {
        constructor(){
          super();
          this.sound = 'bark';
        }
      }
      ```
      <details>
---

{::options parse_block_html="false" /}