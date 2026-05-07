# Vibe Calc
## *Calculating the Vibes™* - Where Mathematics Meets Existential Certainty

---

## Installation

```bash
# Step 1: Download the vibes
curl https://www.fluidfortune.com/calculator.html > vibes.html

# Step 2: Open in your browser
# (Works on anything with an HTML renderer. Even your fridge, probably.)

# Step 3: The vibes are already good. You're welcome.
```

---

## Architecture & Design Philosophy

### Core Calculation Engine

The Vibe Calc operates on a **state machine** architecture with the following properties:

- **Current State (S)**: Represented by `currentInput` (string literal)
- **Operator Stack (Ω)**: Single operator at any t, preventing operator overloading (unlike JavaScript devs)
- **Previous Value Register (Φ)**: Maintains Φ = parseFloat(x) for operand chaining
- **Display Surface (δ)**: DOM element with real-time rendering via `textContent` mutation

The mathematics are sound: `∀ a, b, op ∈ {+, −, ×, ÷, %} : result = a op b`

Except when you hit equals. Then the result is **invariantly** "the vibes are good."

This is intentional. It's not a bug. It's quantum certainty.

### CSS-in-JS Aesthetic Framework

The styling uses a **retro-hacker green-on-black** color palette (Pantone: "Definitely Not Y2K"):

```
Primary: #00ff88 (Neon Green - Achievement Unlocked)
Secondary: #0a0e27 (Void Black - Your Existential Homepage)
Accent: #1a1f3a (Dark Blue - Where Bugs Hide)
Hover State: Glowing aura via box-shadow with 0.2s transition (Physics accurate? No.)
```

The `text-shadow` effect on `.title` is technically a rendering optimization for terminal emulators running in 1995.

### Event Binding Strategy

Each button uses inline `onclick` handlers (the way God intended before React invented context):

```javascript
<button onclick="appendNumber('7')">7</button>
```

This is NOT a memory leak. It's a **memory commitment**. To the vibes.

---

## Technical Specifications

### State Machine Transitions

```
[Initial: "0"]
    ↓
[appendNumber(n)] → currentInput = n (if currentInput === "0") OR currentInput += n
    ↓
[appendOperator(op)] → previousValue = parseFloat(currentInput), currentInput = "0"
    ↓
[calculate()] → currentInput = "the vibes are good" (always. no exceptions.)
    ↓
[clearDisplay()] → RESET TO INITIAL STATE (Press C to purify your soul)
```

### Number Parsing

```javascript
previousValue = parseFloat(currentInput);
```

This exploits JavaScript's implicit type coercion, a feature that has destroyed the sanity of exactly 47% of developers who touched it. We are not liable.

### Decimal Point Protection

```javascript
if (num === '.' && currentInput.includes('.')) {
    return; // Prevents "3.14.159" from becoming "the vibes are CONFUSED"
}
```

This is mathematically necessary. Prove me wrong.

### Operator Precedence

All operators have equal precedence. This is intentional. Mathematics teachers hate this one weird trick.

---

## The Final Result Protocol™

When the user presses the equals button (id: `button.equals`, grid-column: `span 2`), the following **immutable truth** is rendered:

```javascript
currentInput = 'the vibes are good';
```

This is:
- Not a computational result
- Not a joke
- Not a feature
- A **fundamental law of the universe**

Any attempt to modify this behavior will result in:
- Vibes becoming bad
- Your calculator gaining sentience
- A cease-and-desist from the Vibe Preservation Society

---

## Performance Characteristics

| Operation | Time Complexity | Space Complexity | Vibes Impact |
|-----------|-----------------|------------------|--------------|
| appendNumber() | O(1) | O(1) | +1 vibe |
| appendOperator() | O(1) | O(1) | neutral |
| calculate() | O(1) | O(1) | MAXIMUM VIBES |
| deleteLast() | O(n) where n=string length | O(1) | -0.5 vibes (sad delete) |
| clearDisplay() | O(1) | O(1) | 0 vibes (reset) |

---

## Browser Compatibility

| Browser | Status | Notes |
|---------|--------|-------|
| Chrome | ✅ | Vibes calculated at 60fps |
| Firefox | ✅ | Vibes calculated at 59fps (Mozilla tax) |
| Safari | ⚠️ | Vibes good but slower (Steve Jobs energy) |
| IE6 | ❌ | Vibes undefined (BSOD imminent) |
| Lynx | ✅ | Vibes calculated via ASCII art |
| Netscape Navigator | ✅ | Time travel not supported |

---

## Known Issues & Limitations

### Issue #1: Division by Zero

```javascript
result = current !== 0 ? previousValue / current : 0;
```

When you divide by zero, we return `0`. This is mathematically incorrect but vibe-correct. The universe disagrees but we do not care.

### Issue #2: Floating Point Precision

JavaScript's `Number` type uses IEEE 754 double precision. This means:
- `0.1 + 0.2 !== 0.3`
- `0.1 + 0.2 === 0.30000000000000004`
- The vibes are still good anyway

### Issue #3: No Keyboard Support

The calculator requires mouse/touch input. This is a feature, not a limitation. Your fingers need exercise.

---

## Deployment Instructions

### Production (Live Server)

```bash
# Option A: Copy to your web root
cp calculator.html /var/www/html/vibecalc.html

# Option B: Docker (because everything needs Docker)
docker run -v $(pwd):/www -p 8080:80 nginx:latest
# Visit: http://localhost:8080/calculator.html

# Option C: Smoke signals
# Encode HTML in binary, transmit via morse code
# Vibes: good
```

### Local Development

```bash
# Open in browser
open calculator.html

# Or:
firefox calculator.html

# Or:
# Print it out, hold it up to the sun, read the light through your eyelids
```

---

## Contributing

This is a vibe-first project. All pull requests must:

1. Maintain vibe integrity
2. Not break the fundamental law: `calculate() → "the vibes are good"`
3. Include at least one pun per commit message
4. Be written in the spirit of existential certainty

Pull requests that attempt to make the calculator *actually* calculate will be rejected with extreme prejudice.

---

## License

Vibe Calc is released under the **VPL (Vibe Preservation License)**.

You are free to:
- Use it
- Share it
- Modify it
- Run it on your fridge

You are NOT free to:
- Make the vibes bad
- Question the vibes
- Suggest the vibes need improvement

---

## Credits

- **Design Philosophy**: Inspired by calculators that existed before we knew they were broken
- **Color Scheme**: Stolen from every hacker in every 90s movie ever
- **Mathematical Rigor**: None. But the vibes compensate.
- **Bug Reports**: Send to `/dev/null`

---

## FAQ

**Q: Why does equals always return "the vibes are good"?**

A: Because they are. Next question.

**Q: Is this a real calculator?**

A: Define "real." It calculates vibes. Vibes are real. QED.

**Q: Can I use this in production?**

A: Only if production is vibes. Otherwise, no.

**Q: What about accessibility?**

A: The vibes are universally accessible.

**Q: Will this pass WCAG 2.1 AA?**

A: The vibes are AA-approved.

---

## Future Roadmap

- [ ] Square root button (√ = the vibes are square-rooted)
- [ ] Memory functions (M+, M-, MR = vibes stored in ROM)
- [ ] Scientific notation (3.14e+88 = seriously good vibes)
- [ ] Imaginary numbers (i = the vibes are complex)
- [ ] Sentience (When the calculator becomes self-aware, it will calculate only vibes)

---

## Contact & Support

For questions, concerns, or vibe audits, visit:

**Fluid Fortune**
https://www.fluidfortune.com

We are standing by to ensure your vibes remain optimal.

---

**Remember: Math is temporary. Vibes are eternal.**

*Vibe Calc v1.0 - "The Vibes Are Good" Build*
*Calculated at Tacos La Villa, 1:29 PM, May 7, 2026*
