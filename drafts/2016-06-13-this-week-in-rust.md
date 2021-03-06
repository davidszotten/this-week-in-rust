Title: This Week in Rust 134
Number: 134
Date: 2016-06-13
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta:
safety, concurrency, and speed. This is a weekly summary of its progress and
community. Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us an
email](mailto:corey@octayn.net?subject=This%20Week%20in%20Rust%20Suggestion)!
Want to get involved? [We love
contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/cmr/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/cmr/this-week-in-rust/pulls).

This week's edition was edited by: [Vikrant](https://github.com/nasa42) and [llogiq](https://github.com/llogiq).

# Updates from Rust Community

## News & Blog Posts

## New Crates & Project Updates

* [Rust Project changelog for2016-06-10](https://users.rust-lang.org/t/rust-project-changelog-for-2016-06-10/6181).
  Updates to bitflags, libc, nano-config, regex, rustfmt, rust-mode,
  rustup, rust.vim, sublime-rust, uuid, www.rustbyexample.com,
  www.rust-lang.org.
* [error-chain](https://users.rust-lang.org/t/announcing-error-chain-a-library-for-consistent-and-reliable-rust-error-handling/6133),
  a library for consistent and reliable error handling. Initial release.
* [rust-skeptic 0.5 released](https://users.rust-lang.org/t/rust-skeptic-test-your-rust-markdown-documentation-via-cargo/2163/2?u=brson).
  A tool for testing Rust documentation.

# Crate of the Week

This week's Crate of the Week is [pbr](https://crates.io/crates/pbr), which gives us a simple way to set up a progress bar for our applications. Thanks to Lukas Kalbertodt for the suggestion!

[Submit your suggestions for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

* [easy] [rust: Participate in 2016 State of Rust Survey](http://blog.rust-lang.org/2016/05/09/survey.html).
* [easy] [rust: Add error explanations for all error codes](https://github.com/rust-lang/rust/issues/32777).
* [easy] [Speed up crypto in Rust by contributing to and using crypto-bench](https://users.rust-lang.org/t/speed-up-crypto-in-rust-by-contributing-to-and-using-crypto-bench/6097).

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

84 pull requests were [merged in the last two weeks][merged].

[merged]: https://github.com/issues?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2016-05-30..2016-06-06

* [Avoid double-locking `RWLock`/`Mutex`](https://github.com/rust-lang/rust/pull/33861)
* [Deny unsound projections and speeding up the compiler](https://github.com/rust-lang/rust/pull/33816)
* [Rust aborts processes on Windows with __fastfail](https://github.com/rust-lang/rust/pull/33814) (instead of invalid instruction, this is a potentially breaking change)
* [New AST validation pass](https://github.com/rust-lang/rust/pull/33794) to ensure macro expansions obey language rules
* [MIR Non-zeroing Drop](https://github.com/rust-lang/rust/pull/33622) A journey of three years find a happy conclusion
* [MIR Don't generate 3-armed boolean switches](https://github.com/rust-lang/rust/pull/33583)
* [Support 16-bit pointers](https://github.com/rust-lang/rust/pull/33460) for embedded (or oldschool?) systems
* `def_map` no longer `RefCell`d in [TyCtxt](https://github.com/rust-lang/rust/pull/33977) and [driver::Resolutions](https://github.com/rust-lang/rust/pull/33964)
* [Btree{Set,Map}::split_off](https://github.com/rust-lang/rust/pull/33947) (RFC #509)
* [HIR Split Bindings and Paths](https://github.com/rust-lang/rust/pull/33929)
* [Span of derived attributes fixed](https://github.com/rust-lang/rust/pull/33926)
* [MIR range overflow checks](https://github.com/rust-lang/rust/pull/33905)
* [byte slice compare checks for pointer equality](https://github.com/rust-lang/rust/pull/33892) (performance improvement)

## New Contributors

* cheercroaker
* Ivan Shapovalov
* Jamey Sharp
* M Farkas-Dyck
* Scott A Carr
* Zack M. Davis

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments)
process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

*No RFCs were approved this week.*

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now. [This week's FCPs][fcp] are:

[fcp]: https://github.com/rust-lang/rfcs/labels/final-comment-period

* [Implement new methods for checked and wrapping casts for potentially lossy integer conversions](https://github.com/rust-lang/rfcs/pull/1218).
* [Change thread local variables to only accept async-signal-safe types](https://github.com/rust-lang/rfcs/pull/1379).
* [Add a initial, minimal form of `impl Trait`](https://github.com/rust-lang/rfcs/pull/1522).
* [Normalization for long error codes explanations](https://github.com/rust-lang/rfcs/pull/1567).
* [Standardise stream wrappers like compression, encryption](https://github.com/rust-lang/rfcs/pull/1568).
* [Add a `lifetime` specifier to `macro_rules!`](https://github.com/rust-lang/rfcs/pull/1590).
* [Remove the one-type-only restriction on `format_args!` arguments](https://github.com/rust-lang/rfcs/pull/1618).

## New RFCs

* [Require documentation for all new features](https://github.com/rust-lang/rfcs/pull/1636).
* [Automatically implement some traits for `!`](https://github.com/rust-lang/rfcs/pull/1637).
* [Add two new pointer-sized integer types; `uptr` and `iptr`](https://github.com/rust-lang/rfcs/pull/1635).
* [Add `checked_sub()` already known from various primitive types to the `Duration` struct](https://github.com/rust-lang/rfcs/pull/1640).
* [Add PTX and AMDGPU targets](https://github.com/rust-lang/rfcs/pull/1641).

# Upcoming Events

* 6/8. Rust Community Team Meeting at #rust-community on irc.mozilla.org.
* [6/8. Rust Berlin Meetup](http://www.meetup.com/Rust-Berlin/events/231188250/).
* [6/8. Rust Boulder/Denver Monthly Meeting](http://www.meetup.com/Rust-Boulder-Denver/).
* [6/9. Columbus Rust Society](http://www.meetup.com/columbus-rs/events/230812780/).
* [6/13. Seattle Rust Meetup](https://www.eventbrite.com/e/mozilla-rust-seattle-meetup-tickets-12222326307?aff=erelexporg).
* [6/14. Eat – Drink – Rust! Downtown Rust Meetup (San Diego)](http://www.meetup.com/San-Diego-Rust/events/231356534/)
* 6/15. Rust Community Team Meeting at #rust-community on irc.mozilla.org.
* [6/15. Rust Los Angeles Monthly Meetup - Hack Night](http://www.meetup.com/Rust-Los-Angeles/events/231587506/).
* [6/17. Rhein-Main Rust Regulars' Table](http://www.meetup.com/Rust-Rhein-Main/events/231344035/).

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Email [Erick Tryzelaar][erickt] or [Brian
Anderson][brson] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[erickt]: mailto:erick.tryzelaar@gmail.com
[brson]: mailto:banderson@mozilla.com

# fn work(on: RustProject) -> Money

*No jobs listed for this week.*

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

*No quote was selected for QotW.*

[Submit your quotes for next week][submit]!

[submit]: http://users.rust-lang.org/t/twir-quote-of-the-week/328
