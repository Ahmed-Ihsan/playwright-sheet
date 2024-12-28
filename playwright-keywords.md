# Playwright Keywords and Commands Reference

## Browser Control
| Keyword | Description | Example |
|---------|-------------|----------|
| `playwright.chromium` | Launch Chromium browser | `browser = await playwright.chromium.launch()` |
| `playwright.firefox` | Launch Firefox browser | `browser = await playwright.firefox.launch()` |
| `playwright.webkit` | Launch WebKit browser | `browser = await playwright.webkit.launch()` |
| `launch()` | Launch browser with options | `launch({ headless: false })` |
| `close()` | Close browser | `await browser.close()` |

## Context and Pages
| Keyword | Description | Example |
|---------|-------------|----------|
| `newContext()` | Create new browser context | `context = await browser.newContext()` |
| `newPage()` | Create new page | `page = await context.newPage()` |
| `goto()` | Navigate to URL | `await page.goto('https://example.com')` |
| `reload()` | Reload page | `await page.reload()` |
| `goBack()` | Navigate back | `await page.goBack()` |
| `goForward()` | Navigate forward | `await page.goForward()` |

## Selectors and Elements
| Keyword | Description | Example |
|---------|-------------|----------|
| `$` | Select single element | `element = await page.$('.selector')` |
| `$$` | Select multiple elements | `elements = await page.$$('.selector')` |
| `getByRole()` | Select by ARIA role | `await page.getByRole('button')` |
| `getByText()` | Select by text content | `await page.getByText('Click me')` |
| `getByLabel()` | Select by label text | `await page.getByLabel('Username')` |
| `getByPlaceholder()` | Select by placeholder | `await page.getByPlaceholder('Enter email')` |
| `getByTestId()` | Select by test ID | `await page.getByTestId('submit-button')` |

## Actions
| Keyword | Description | Example |
|---------|-------------|----------|
| `click()` | Click element | `await element.click()` |
| `dblclick()` | Double click element | `await element.dblclick()` |
| `fill()` | Fill input field | `await element.fill('text')` |
| `type()` | Type text | `await element.type('text')` |
| `press()` | Press keyboard key | `await page.press('Enter')` |
| `hover()` | Hover over element | `await element.hover()` |
| `check()` | Check checkbox | `await element.check()` |
| `uncheck()` | Uncheck checkbox | `await element.uncheck()` |
| `selectOption()` | Select dropdown option | `await element.selectOption('value')` |

## Waits and Timing
| Keyword | Description | Example |
|---------|-------------|----------|
| `waitForSelector()` | Wait for element | `await page.waitForSelector('.element')` |
| `waitForLoadState()` | Wait for load state | `await page.waitForLoadState('networkidle')` |
| `waitForNavigation()` | Wait for navigation | `await page.waitForNavigation()` |
| `waitForResponse()` | Wait for network response | `await page.waitForResponse(url)` |
| `waitForTimeout()` | Wait for specified time | `await page.waitForTimeout(1000)` |

## State and Properties
| Keyword | Description | Example |
|---------|-------------|----------|
| `isVisible()` | Check if element visible | `await element.isVisible()` |
| `isEnabled()` | Check if element enabled | `await element.isEnabled()` |
| `isChecked()` | Check if checkbox checked | `await element.isChecked()` |
| `getAttribute()` | Get element attribute | `await element.getAttribute('class')` |
| `textContent()` | Get element text content | `await element.textContent()` |
| `innerHTML()` | Get element inner HTML | `await element.innerHTML()` |

## Screenshots and Videos
| Keyword | Description | Example |
|---------|-------------|----------|
| `screenshot()` | Take screenshot | `await page.screenshot({ path: 'screen.png' })` |
| `screencastStarted()` | Start video recording | `await page.video().screencastStarted()` |
| `saveAs()` | Save recorded video | `await page.video().saveAs('video.mp4')` |

## Network and Requests
| Keyword | Description | Example |
|---------|-------------|----------|
| `route()` | Route network requests | `await page.route(pattern, handler)` |
| `unroute()` | Stop routing requests | `await page.unroute(pattern)` |
| `setExtraHTTPHeaders()` | Set HTTP headers | `await context.setExtraHTTPHeaders(headers)` |
| `setRequestInterception()` | Enable request interception | `await page.setRequestInterception(true)` |

## Frames and Windows
| Keyword | Description | Example |
|---------|-------------|----------|
| `frame()` | Get frame by name/URL | `frame = page.frame('frameName')` |
| `frames()` | Get all frames | `frames = page.frames()` |
| `popup()` | Handle new window | `popup = await page.waitForEvent('popup')` |
| `workers()` | Get web workers | `workers = page.workers()` |

## Assertions (Test Runner)
| Keyword | Description | Example |
|---------|-------------|----------|
| `expect()` | Create assertion | `await expect(page).toHaveTitle('Title')` |
| `toBeVisible()` | Assert element visible | `await expect(element).toBeVisible()` |
| `toHaveText()` | Assert element has text | `await expect(element).toHaveText('text')` |
| `toHaveValue()` | Assert input has value | `await expect(element).toHaveValue('value')` |
| `toBeEnabled()` | Assert element enabled | `await expect(element).toBeEnabled()` |

## Events
| Keyword | Description | Example |
|---------|-------------|----------|
| `on()` | Add event listener | `page.on('load', handler)` |
| `once()` | Add one-time listener | `page.once('dialog', handler)` |
| `off()` | Remove event listener | `page.off('console', handler)` |
| `waitForEvent()` | Wait for event | `await page.waitForEvent('load')` |

## Dialog Handling
| Keyword | Description | Example |
|---------|-------------|----------|
| `dialog()` | Handle dialog | `page.on('dialog', dialog => dialog.accept())` |
| `accept()` | Accept dialog | `await dialog.accept()` |
| `dismiss()` | Dismiss dialog | `await dialog.dismiss()` |

## Storage
| Keyword | Description | Example |
|---------|-------------|----------|
| `addInitScript()` | Add initialization script | `await context.addInitScript(script)` |
| `clearCookies()` | Clear cookies | `await context.clearCookies()` |
| `clearStorageState()` | Clear storage state | `await context.clearStorageState()` |
| `storageState()` | Get storage state | `state = await context.storageState()` |

## Accessibility
| Keyword | Description | Example |
|---------|-------------|----------|
| `snapshot()` | Get accessibility snapshot | `snapshot = await page.accessibility.snapshot()` |
| `getByRole()` | Select by ARIA role | `element = await page.getByRole('button')` |
| `getByLabel()` | Select by label | `element = await page.getByLabel('Name')` |
