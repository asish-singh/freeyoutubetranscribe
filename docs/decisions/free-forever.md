# Product decision. Why "free forever" is a pricing and positioning choice

*A decision record for [freeyoutubetranscribe.com](https://freeyoutubetranscribe.com). The source is private; this documents the reasoning, which isn't.*

## The market situation

YouTube transcript tools are a crowded space with a predictable business model. YouTube blocks transcript requests from datacenter IPs, so competitors pay for proxy fleets to get around it, and that per request cost forces paywalls, rate limits, and signups. Every competitor's pricing is downstream of the same infrastructure bill.

## The decision

Price at zero, permanently, and treat that not as a promotion but as a positioning claim that competitors structurally cannot copy.

The claim only works if it is true, which imposed a hard engineering constraint. **The marginal cost of one more user must be zero.** That constraint drove the architecture, not the other way around.

- Transcripts are fetched by the user's own browser directly from YouTube, so there is no proxy bill. That bill is the exact cost that forces competitors to charge.
- The machine learning model that restores punctuation runs on the user's device, so heavy compute scales with users at no cost to the service.
- Everything else fits in free tier edge infrastructure.

## Why zero beats cheap

- **Trust.** A "free forever" promise from a service with visibly zero marginal cost is credible; from a service subsidized by investors it is a countdown timer. The README explains the cost structure precisely so users can verify the promise is structural.
- **Distribution as a moat.** Every transcript viewed becomes a cached public page that search engines can index. Users build the library, the library brings search traffic, and traffic brings users. That flywheel only spins if there is no signup wall in the way.
- **Segment fit.** The users who need this most (deaf and hard of hearing readers, language learners, people on expensive connections) are exactly the ones a paywall excludes first.

## What was given up

- No revenue, by design. This is a portfolio and public good project; monetizing it would break the positioning that makes it interesting.
- Fetching from the user's browser fails on some unusual networks, so a fallback on the server exists as a scope concession to reliability.

## The general lesson

Pricing is usually treated as a number chosen after the product is built. Here it worked better in reverse. Choosing the price first (zero, forever) dictated the architecture, the marketing story, and the growth loop, and made all three consistent.
