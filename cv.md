# Lev Kalinin

![Profile picture](https://avatars.githubusercontent.com/u/68015557?v=4 'Profile picture')

## Contacts

- Location: Batumi, Georgia
- Phone: (+995)593-623-268
- Email: lkalinindev@gmail.com
- Telegram: @almost0ne
- LinkedIn: [Lev Kalinin](https://www.linkedin.com/in/lkalinin/ 'LinkedIn url')
- Github: [almalmalm](https://github.com/almalmalm 'Github url')
- Discord: almalmalm
- Codewars: [almalmalm](https://www.codewars.com/users/almalmalm 'Codewars url')

## About

My goal in life is to enjoy my own work. My priorities in life are a healthy lifestyle, peace of mind, family and travel.

I have tried many different areas of work and fell in love with the IT field. I studied QA and frontend development at the same time. But it turned out that I got a job as a QA. Right away I started using javascript and typescript and writing autotests and even helped with small tasks at the frontend.

After 2 years of working as QA, I got tired of working from manual tasks, because even as QA Automation I do manual tasks. I spend almost all my free time creating web applications and use react most of the time.

## Skills

- HTML, CSS, SQL, Bash, Javascript, Typescript, Java, Python
- Cypress, Playwright, Pytest, Selenium, TestNG, Mocha, React, Angular, TailwindCSS, SCSS, Redux, Next, Three.js
- Git, GitHub, GitLab
- Docker, Nodejs, Jira, Confluence, DevTools, Postman, Swagger, Figma, Allure, Gitlab CI/CD, GitHub Actions
- VSCode, WebStorm, IntelliJIDEA, PyCharm
- Windows, Linux, MacOS
- MySQL, MongoDB

## Code

**Typescript + React**

```
type Props = {
  characters: Character[];
};

type Character = {
  id: number;
  name: string;
  gender: string;
  episodes: string[];
  image: string;
  species: string;
  status: string;
  url: string;
  location: { name: string; url: string };
};

const Characters: React.FC<Props> = ({ characters }) => {
  return (
    <>
      <Header position="relative" />
      <div className="text-[#fbfcff] tablet:my-0 tablet:mx-auto w-full">
        <ul className="flex flex-wrap justify-center">
          {characters.map((character: Character) => (
            <li key={character.id}>
              <Character img={character.image} name={character.name} />
            </li>
          ))}
        </ul>
      </div>
      <Pagination />
    </>
  );
};
```

---

**Typescript + Nodejs**

```
interface BookDocument extends Document {
  title: string;
  author: string;
  description: string;
  link: string;
}

const BookSchema = new Schema<BookDocument>({
  title: { type: String, required: true },
  author: { type: String, required: true },
  description: { type: String, required: true },
  link: { type: String, required: true },
});

const Book = mongoose.model<BookDocument>('Book', BookSchema);
```

---

**Java + Selenium**

```
public class GoogleTest {
    @Test
    public void search() throws InterruptedException {
        WebDriverManager.chromedriver().setup();
        WebDriver driver = new ChromeDriver();

        driver.get("https://www.google.com/");

        WebElement textBox = driver.findElement(By.name("q"));

        textBox.sendKeys("selenium");
        textBox.sendKeys(Keys.RETURN);

        WebElement text = driver.findElement(By.xpath("//h3[text() = \"Selenium\"]"));

        Assert.assertEquals(text.getText(),"Selenium");

        driver.quit();
    }
}
```

---

**Python + Selenium**

```
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install()))

def test_open_stack():
    driver.get("https://stackoverflow.com/")
    driver.maximize_window()
    search = driver.find_element(By.CSS_SELECTOR, 'input[name="q"]')
    search.send_keys("Python")
    time.sleep(5)
    assert driver.current_url.__contains__("stackoverflow")
```

---

**Typescript + Cypress**

```
class MainPage {
  private readonly title = '[data-test="title"]';
  private readonly information = '[data-test="information"]';
  private readonly description = '[data-test="description"]';
  private readonly buttonSignIn = '[data-test="sign-in"]';
  private readonly buttonSignUp = '[data-test="sign-up"]';

  // Navigates to the main page
  visit() {
    cy.visit('https://my-expenses-three.vercel.app/');
  }
  // Verify text in the title
  verifyTitleIsEqualTo(title: string) {
    cy.get(this.title)
      .should('have.text', title)
      .should('have.css', 'text-transform', 'uppercase');
  }
  // Verify text in the description
  verifyDescriptionIsEqualTo(description: string) {
    cy.get(this.description).should('have.text', description);
  }
  // Verify description located under the title
  verifyDescriptionIsUnderTheTitle() {
    cy.get(this.information)
      .contains('My expenses')
      .parent()
      .next()
      .contains(
        'You can track your money expenses, view monthly statistics and more.'
      )
      .should('be.visible');
  }
  // Verify sign in button is visible
  verifySignInButtonIsVisible() {
    cy.get(this.buttonSignIn).should('be.visible');
  }
  // Verify sign up button is visible
  verifySignUpButtonIsVisible() {
    cy.get(this.buttonSignUp).should('be.visible');
  }
  // Verify sign in button color
  verifySignInButtonColor(color: string) {
    cy.get(this.buttonSignIn)
      .should('have.css', 'background-color')
      .and('eq', color);
  }
  // Verify sign in button color
  verifySignUpButtonColor(color: string) {
    cy.get(this.buttonSignIn)
      .should('have.css', 'background-color')
      .and('eq', color);
  }
}
```

---

**Codewars Rank 6 Java**

```
public class PangramChecker {
  public boolean check(String sentence){
    //code
    sentence = sentence.toLowerCase();
    if(sentence.contains("a")&&sentence.contains("b")&&sentence.contains("c")&&sentence.contains("d")&&sentence.contains("e")&&sentence.contains("f")&&sentence.contains("g")&&sentence.contains("h")&&sentence.contains("i")&&sentence.contains("j")&&sentence.contains("k")&&sentence.contains("l")&&sentence.contains("m")&&sentence.contains("n")&&sentence.contains("o")&&sentence.contains("p")&&sentence.contains("q")&&sentence.contains("r")&&sentence.contains("s")&&sentence.contains("t")&&sentence.contains("u")&&sentence.contains("w")&&sentence.contains("y")&&sentence.contains("x")&&sentence.contains("y")&&sentence.contains("z")){
      return true;
    }else{
     return false;
    }
  }
}
```

---

**Codewars Rank 6 Typescript**

```
export function createPhoneNumber(numbers: number[]): string {
  return `(${numbers[0]}${numbers[1]}${numbers[2]}) ${numbers[3]}${numbers[4]}${numbers[5]}-${numbers[6]}${numbers[7]}${numbers[8]}${numbers[9]}`
}
```

## Work Experience

- **Rusklimat** _QA Automation Engineer(Playwright + Typescript) + QA Manual_ Moscow, Russia 09,2022 - Now
- **Anflat** _QA Manual + QA Automation Engineer(Cypress + Javascript)_ Kazan, Russia 12,2021 - 09,2022

---

**Projects**

- [My Expenses app](https://my-expenses-three.vercel.app/ 'App about money spending') [GitHub](https://github.com/almalmalm/my-expenses 'GitHub url')
- [Rick and Morty](https://rick-and-morty-almalmalm.vercel.app/ 'App about Rick and Morty series') [GitHub](https://github.com/almalmalm/rick-and-morty 'GitHub url')

## Education

- Bachelor of Computer Science 2021 - now(paused at 09,2022)
- Food Service Technologist 2016-2019
- Andersen QA course

## Languages

**English** [Intermediate/ Upper-Intermediate](https://www.efset.org/cert/2BwmeD 'EFSET certificate')
**Russian** Native
