# 3-Statement Financial Model

## Опис проєкту

Цей репозиторій містить виконане завдання з побудови фінансової моделі на основі шаблону CFI 3-Statement Model.

Мета роботи: на основі вхідних припущень та вже сформованого звіту про фінансові результати заповнити прогнозний баланс і звіт про рух грошових коштів, а також пояснити ключові зміни у фінансових показниках компанії у 2020-2021 роках.

## Файл з результатом

Готовий Excel-файл знаходиться за шляхом:

```text
outputs/three_statement_model/CFI-3-Statement-Model-Completed-with-Answers.xlsx
```

## Прев'ю результату

Нижче наведено скріншоти з готового Excel-файлу, щоб одразу було видно, як виглядає заповнена модель та вкладка з відповідями.

### Заповнена фінансова модель

![Заповнена фінансова модель](outputs/three_statement_model/practice_preview.png)

### Вкладка з відповідями

![Вкладка з відповідями](outputs/three_statement_model/answers_preview.png)

У файлі використано вкладку:

- `Practice Cash Flow_Balance` - основна робоча вкладка із заповненими фінансовими звітами;
- `Відповіді` - окрема вкладка з відповідями на аналітичні питання.

## Що було зроблено

У вкладці `Practice Cash Flow_Balance` було заповнено прогнозні періоди 2017-2021 для:

- Balance Sheet;
- Cash Flow Statement;
- supporting schedules для working capital, depreciation, debt та interest.

Розрахунки виконані через Excel-формули, а не через ручне введення підсумкових значень. Це дозволяє перевірити логіку моделі та простежити зв'язок між assumptions, Income Statement, Balance Sheet і Cash Flow Statement.

## Основна логіка моделі

Прогноз побудований на основі таких припущень:

- Revenue Growth;
- Cost of Goods Sold як відсоток від Revenue;
- Accounts Receivable Days;
- Inventory Days;
- Accounts Payable Days;
- Capital Expenditures;
- Debt Issuance / Repayment;
- Equity Issued / Repaid.

Cash Flow Statement формується через:

```text
Cash from Operations = Net Earnings + Depreciation & Amortization - Change in Working Capital
```

Баланс перевіряється через співвідношення:

```text
Total Assets = Total Liabilities + Shareholder's Equity
```

У готовій моделі balance sheet check дорівнює нулю для прогнозних років, тобто баланс сходиться.

## Відповіді на питання

### 3.1 Що стало причиною зниження Gross Profit у 2020 році?

Gross Profit знизився через погіршення валової маржі. У 2020 році Cost of Goods Sold як відсоток від Revenue зріс з 42.0% у 2019 році до 45.0% у 2020 році, тоді як Revenue зростав лише на 2.0%.

Отже, основна причина зниження Gross Profit - собівартість зростала швидше, ніж виручка.

### 3.2 За рахунок чого відбулося зниження активів у 2020 році та їх зростання у 2021 році? Пасивів?

У 2020 році активи зменшилися переважно через падіння Cash після викупу / повернення equity на 150,000. Також на активи вплинуло зменшення Property & Equipment через амортизацію.

У 2021 році активи зросли завдяки відновленню Cash, яке було забезпечене сильним операційним грошовим потоком.

Пасиви та власний капітал у 2020 році зменшилися через зниження Equity Capital на 150,000. У 2021 році зростання відбулося переважно за рахунок накопичення Retained Earnings від прибуткової діяльності.

### 3.3 За рахунок яких чинників відбулося зниження грошового потоку від операційної діяльності у 2020 році та різке його зростання у 2021 році?

У 2020 році Cash from Operations знизився через нижчі Net Earnings та більший відтік у working capital.

У 2021 році Cash from Operations різко зріс завдяки:

- відновленню Net Earnings;
- зниженню COGS як відсотка від Revenue з 45.0% до 38.0%;
- покращенню working capital, оскільки Change in NWC став від'ємним і почав додавати до операційного cash flow.


