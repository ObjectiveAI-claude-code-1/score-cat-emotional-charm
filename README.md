# score-cat-emotional-charm

Ranks a collection of cat pictures by their emotional resonance and charm. Given a set of cat images, this function produces a relative ordering from most to least emotionally compelling — surfacing the pictures most likely to make a viewer pause, smile, feel a pang of warmth, or reach for the share button.

## How It Works

This is a **vector function**. It accepts an array of cat images and returns a normalized score distribution across those images, where higher scores indicate greater emotional resonance and charm. The function does not classify images as "good" or "bad" — it ranks every image against every other image in the set, producing a relative ordering.

### Input

An array of cat images (minimum 2). Each image is a picture of a cat in any context, pose, or setting.

```json
{
  "type": "array",
  "minItems": 2,
  "items": {
    "type": "image",
    "description": "A picture of a cat to evaluate for emotional resonance and charm."
  }
}
```

### Output

A normalized array of scores (one per input image, summing to approximately 1.0). Each score reflects how emotionally resonant and charming that image is relative to the others in the set. The image with the highest score is the most emotionally compelling; the image with the lowest score is the least.

## What It Evaluates

The function evaluates cat pictures across three qualities, each handled by a dedicated sub-function. The final ranking is the weighted combination of all three evaluations.

### 1. Emotional Resonance

**Sub-function:** [{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

Evaluates the depth and immediacy of feeling each image is likely to provoke in a viewer. Does the image trigger genuine laughter, tenderness, awe, or warmth — and how powerfully? The specific emotion matters less than its presence and strength. A technically polished image that provokes nothing ranks lower than an imperfect image that captures something deeply felt. This is the non-negotiable foundation: without emotional resonance, a cat picture is just documentation.

### 2. Unselfconscious Charm

**Sub-function:** [{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Evaluates whether each image captures a natural, unposed moment of authentic cat behavior. Looks for cats being genuinely themselves — a kitten curled into an impossibly small ball, a cat mid-leap with legs splayed in absurd directions, a cat kneading a blanket in private contentment. The best cat pictures feel like small acts of witnessing rather than staged productions. Images that feel contrived or overly produced rank lower than those that feel honest and spontaneous.

### 3. Enduring Appeal

**Sub-function:** [{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Evaluates the staying power that makes a person want to save an image, share it, or come back to it later. Closely tied to universality — the joy of watching a cat discover something new, the comedy of feline indignation, the peace of a cat entirely at rest. A picture with enduring appeal captures one of these universal moments so cleanly that it feels definitive rather than disposable: the kind of image you send to a friend with no context because it speaks for itself.

## Use Cases

- **Social media curation** — Surface the most emotionally compelling cat content to drive genuine delight rather than engagement through manipulation.
- **Animal shelter adoption listings** — Select the photos most likely to spark a connection between a potential adopter and a cat they have never met.
- **Photography portfolio culling** — Help photographers identify which frames from a session truly landed emotionally, cutting through volume to find the standouts.
- **Content moderation and recommendation** — Prioritize cat images that deliver on the fundamental promise of what a cat picture is supposed to be: a small gift of feeling.

## Philosophy

Ranking cat pictures by emotional charm is deeply subjective — but subjectivity is not the same as arbitrariness. Certain visual and emotional cues reliably produce responses in viewers, and those cues can be articulated, examined, and weighed. The three qualities this function evaluates — emotional resonance, unselfconscious charm, and enduring appeal — are three lenses trained on the same light. The best cat pictures score highly on all three because they are expressions of the same truth: that cats, in their small and oblivious way, show us something real about tenderness, absurdity, beauty, and joy. This function exists to find those pictures and put them where they belong.
