<h1 align="center">HTML Template & Style Guide</h1>

## 🧐 Style Guide <a name = "about"></a>

Dokumen ini berisi panduan dalam menulis Styling.

## Typograph System

#### Font Size (px)

- 10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98

#### Font Weight

- Default : 400
- Medium : 500
- Semi Bold : 600
- Bold : 700

#### Line Height

- Default : 1
- Small : 1.05
- Medium : 1.2
- Paragraph Default : 1.6
- Large : 1.8

#### Letter Spacing

- 0.5px
- 0.75px

## Colors

- Primary : N/A
- Secondary : N/A
- Tertiary : N/A

---

### CSS Template

```
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  html {
    /* font-size: 10px; */

    /* 10px / 16px = 0.625 = 62.5% */
    /* Percentage of user's browser font-size setting */
    font-size: 62.5%;
    overflow-x: hidden;

    /* Does NOT work on Safari */
    /* scroll-behavior: smooth; */
  }

  body {
    font-family: "Quicksand", sans-serif;
    line-height: 1;
    font-weight: 400;
    color: #555;

    /* Only works if there is nothing absolutely positioned in relation to body */
    overflow-x: hidden;
  }
```

---

## General Reusable Style

```
.container {
    /* 1140px */
    max-width: 120rem;
    padding: 0 3.2rem;
    margin: 0 auto;
  }

  .grid {
    display: grid;
    column-gap: 6.4rem;
    row-gap: 9.6rem;

    /* margin-bottom: 9.6rem; */
  }

  /* .grid:last-child {
    margin-bottom: 0;
  } */

  .grid:not(:last-child) {
    margin-bottom: 9.6rem;
  }

  .grid--2-cols {
    grid-template-columns: repeat(2, 1fr);
  }

  .grid--3-cols {
    grid-template-columns: repeat(3, 1fr);
  }

  .grid--4-cols {
    grid-template-columns: repeat(4, 1fr);
  }

  /* .grid--5-cols {
    grid-template-columns: repeat(5, 1fr);
  } */

  .grid--center-v {
    align-items: center;
  }

  .heading-primary,
  .heading-secondary,
  .heading-tertiary {
    font-weight: 700;
    color: #333;
    /* color: #45260a; */
    /* color: #343a40; */
    letter-spacing: -0.5px;
  }

  .heading-primary {
    font-size: 5.2rem;
    line-height: 1.05;
    margin-bottom: 3.2rem;
  }

  .heading-secondary {
    font-size: 4.4rem;
    line-height: 1.2;
    margin-bottom: 9.6rem;
  }

  .heading-tertiary {
    font-size: 3rem;
    line-height: 1.2;
    margin-bottom: 3.2rem;
  }

  .subheading {
    display: block;
    font-size: 1.6rem;
    font-weight: 500;
    color: #cf711f;
    text-transform: uppercase;
    margin-bottom: 1.6rem;
    letter-spacing: 0.75px;
  }

  .btn,
  .btn:link,
  .btn:visited {
    display: inline-block;

    text-decoration: none;
    font-size: 2rem;
    font-weight: 600;
    padding: 1.6rem 3.2rem;
    border-radius: 9px;

    /* Only necessary for .btn */
    border: none;
    cursor: pointer;
    font-family: inherit;

    /* Put transition on original "state" */
    /* transition: background-color 0.3s; */
    transition: all 0.3s;
  }

  .btn--full:link,
  .btn--full:visited {
    background-color: #e67e22;
    color: #fff;
  }

  .btn--full:hover,
  .btn--full:active {
    background-color: #cf711f;
  }

  .btn--outline:link,
  .btn--outline:visited {
    background-color: #fff;
    color: #555;
  }

  .btn--outline:hover,
  .btn--outline:active {
    background-color: #fdf2e9;

    /* border: 3px solid #fff; */

    /* Trick to add border inside */
    box-shadow: inset 0 0 0 3px #fff;
  }

  .btn--form {
    background-color: #45260a;
    color: #fdf2e9;
    align-self: end;
    padding: 1.2rem;
  }

  .btn--form:hover {
    background-color: #fff;
    color: #555;
  }

  .link:link,
  .link:visited {
    display: inline-block;
    color: #e67e22;
    text-decoration: none;
    border-bottom: 1px solid currentColor;
    padding-bottom: 2px;
    transition: all 0.3s;
  }

  .link:hover,
  .link:active {
    color: #cf711f;
    border-bottom: 1px solid transparent;
  }

  .list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 1.6rem;
  }

  .list-item {
    font-size: 1.8rem;
    display: flex;
    align-items: center;
    gap: 1.6rem;
    line-height: 1.2;
  }

  .list-icon {
    width: 3rem;
    height: 3rem;
    color: #e67e22;
  }

  *:focus {
    outline: none;
    /* outline: 4px dotted #e67e22; */
    /* outline-offset: 8px; */
    box-shadow: 0 0 0 0.8rem rgba(230, 125, 34, 0.5);
  }

  /* HELPER/SETTINGS CLASSES */
  .margin-right-sm {
    margin-right: 1.6rem !important;
  }

  .margin-bottom-md {
    margin-bottom: 4.8rem !important;
  }

  .center-text {
    text-align: center;
  }

  strong {
    font-weight: 500;
  }

```
