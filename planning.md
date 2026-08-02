# Reviving the Dream: Roadmap to Complete the Abandoned App
Below is a plan organized by larger tasks and their sub-tasks, color-coded by priority:

🔴Dark Red: High priority
🟠Orange: Medium priority
🟢Green: Low priority
🔵Blue: Good practice
<!-- `Almost like a traffic light 😊` -->

<p>The ones with a <span style="background-color: #d4f8d4; padding: 3px;">green</span> cell background are finished, but <span style="background-color:rgb(255, 255, 208); padding: 3px;">yellow</span> - partially done.</p>

<table>
  <thead>
    <tr>
      <th>Task</th>
      <th>Sub-tasks</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Core Functionality</strong></td>
      <td>🔴 Fix image upload</td>
    </tr>
    <tr>
      <td rowspan="4"><strong>Ensuring Clean Data in the Database</strong></td>
      <td style="background-color:rgb(255, 255, 208);">🟠 Add constraints, cascades, triggers, etc.</td>
    </tr>
    <tr>
      <td>🟢 Manually insert testing data</td>
    </tr>
    <tr>
      <td>🔴 Implement data validation at the backend</td>
    </tr>
    <tr>
      <td>🔵 Write unit tests for database integrity</td>
    </tr>
    <tr>
      <td style="background-color: #d4f8d4;" rowspan="2"><strong>Keep My App Up to Date</strong><br>Last update: 28/01/2025</td>
      <td style="background-color: #d4f8d4;">Dockerize Laravel</td>
    </tr>
    <tr>
      <td style="background-color: #d4f8d4;">Update to Laravel 11 (L11)</td>
    </tr>
    <tr>
        <td colspan="2">
            <strong>Figma <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Figma-logo.svg/1200px-Figma-logo.svg.png" alt="Figma logo" style="height: 20px; vertical-align: middle;"> design link</strong>
            <a href="https://www.figma.com/design/F87iJjsQZDMQkVyGkmcQrx/Team-Project?node-id=206-670&t=hYCF5Ed9KaK2Lu4G-0" target="_blank">here</a> (private)
        </td>
    </tr>
    <tr>
      <td rowspan="3"><strong>🔴Localization</strong></td>
      <td>
        Integrate a new route for editing translations in the whole app
      </td>
    </tr>
    <tr>
      <td>Assign translation editing to a role</td>
    </tr>
    <tr>
      <td>Seperate app translations and animals</td>
    </tr>
  </tbody>
</table>

## Important notes

### Moving the whole app to inertia
The current email verification doesnt have to be used so need to rewrite routes that point to the verifications.

### Translations
When moving the app translations, nothing has to be changed, but when i want to translate any of the species names or foods that are stored in the database, i will need a different approach.

`php artisan vendor:publish --provider="Outhebox\TranslationsUI\TranslationsUIServiceProvider" --tag=assets`

<!-- php artisan translations:publish -->

the actual asset publishing happened with this command:
reference from the github repo
https://github.com/MohmmedAshraf/laravel-translations
Before you can access the translations UI, you'll need to publish the package's assets and migrations files by running the following command:

php artisan translations:install

my own apps assets are published seperately with npm run build or run dev.