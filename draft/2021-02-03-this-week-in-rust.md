Title: This Week in Rust 376
Number: 376
Date: 2021-02-03
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/rust-lang/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/rust-lang/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/rust-lang/this-week-in-rust/pulls).

# Updates from Rust Community

[gfx-rs ecosystem releases v0.7](https://gfx-rs.github.io/2021/02/02/release-0.7.html)

### Official

### Newsletters

### Project/Tooling Updates

[PL] [CrabbyBird #5 Obsługa kolizji](https://postacnormalna.pl/crabbybird-5-obsluga-kolizji/)

### Observations/Thoughts

### Rust Walkthroughs

### Miscellaneous

# Crate of the Week

This week's crate is [aquamarine](https://github.com/mersinvald/aquamarine) bringing you inline diagrams for your rustdocs.

Thanks to [Willi Kappler](https://users.rust-lang.org/t/crate-of-the-week/2704/874) for the suggestion!

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

299 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2021-01-18..2021-01-25

* [improve unknown external crate error](https://github.com/rust-lang/rust/pull/81046)
* [gracefully handle loop labels missing leading `'` in different positions](https://github.com/rust-lang/rust/pull/81236)
* [improve diagnostics when parsing angle args](https://github.com/rust-lang/rust/pull/80065)
* [permit mutable references in all const contexts](https://github.com/rust-lang/rust/pull/78578)
* [prevent query cycles in the MIR inliner](https://github.com/rust-lang/rust/pull/68828)
* [mir: improve `size_of` handling when arg is unsized](https://github.com/rust-lang/rust/pull/81243)
* [implement `Error` for `&(impl Error)`](https://github.com/rust-lang/rust/pull/75180)
* [change branching in `iter.skip()`](https://github.com/rust-lang/rust/pull/80715)
* [`BufWriter`: Provide `into_raw_parts`](https://github.com/rust-lang/rust/pull/79705)
* [fix soundness issue for `replace_range` and `range`](https://github.com/rust-lang/rust/pull/81169)
* [avoid `hash_slice` in `VecDeque`'s `Hash` implementation](https://github.com/rust-lang/rust/pull/81170)
* [turn alloc's force_expr macro into a regular macro_rules](https://github.com/rust-lang/rust/pull/81241)
* [hashbrown: add `try_insert_no_grow` method on `RawTable`](https://github.com/rust-lang/hashbrown/pull/229)
* [fix a bug in Cargo's cyclic dep graph detection](https://github.com/rust-lang/cargo/pull/9075)
* [cargo: add some extra help to `cargo new` and invalid package names](https://github.com/rust-lang/cargo/pull/9098)
* [rustdoc: fix rendering of stabilization version for trait implementors](https://github.com/rust-lang/rust/pull/81302)
* [clippy: `manual_filter_map` and `manual_find_map`](https://github.com/rust-lang/rust-clippy/pull/6591)
* [clippy: new lint: `exhaustive_enums`, `exhaustive_structs`](https://github.com/rust-lang/rust-clippy/pull/6617)

## Rust Compiler Performance Triage

This week continues a trend of relatively large rollups, which often contain
perf-sensitive PRs. We need to get better at marking PRs as rollup=never or
otherwise not including them, but it is unclear how precisely to go about doing
so. The tooling for testing individual PRs merged in rollups should also be
improved to work better in the next few days, though.

Other than that, this week saw several regressions, most of which were not
easily explained. We are seeking feedback from PR authors and reviewers on
whether the results are expected and if anything can be done.

Triage done by **@rylevick** and **@simulacrum**.
Revision range: [e05409a02c6e73a3dea6da98798468db2910ca59..1483e67addd37d9bd20ba3b4613b678ee9ad4d68](https://perf.rust-lang.org/?start=e05409a02c6e73a3dea6da98798468db2910ca59&end=1483e67addd37d9bd20ba3b4613b678ee9ad4d68&absolute=false&stat=instructions%3Au)

5 Regressions, 2 Improvements, 1 Mixed;
3 of them in rollups

See the [full report](https://github.com/rust-lang/rustc-perf/blob/master/triage/2021-01-26.md) for more.

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments) process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [Allow "artifact dependencies" on bin, cdylib, and staticlib crates](https://github.com/rust-lang/rfcs/pull/3028)

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)

* [Rust 2021 Roadmap](https://github.com/rust-lang/rfcs/pull/3037)

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)

* [disposition: merge] [Remove requirement that forces symmetric and transitive PartialEq impls to exist](https://github.com/rust-lang/rust/pull/81198)
* [disposition: merge] [Stabilize `core::slice::fill_with`](https://github.com/rust-lang/rust/pull/81048)
* [disposition: merge] [Add Box::downcast() for dyn Any + Send + Sync](https://github.com/rust-lang/rust/pull/80945)
* [disposition: merge] [Stabilize by-value `[T; N]` iterator `core::array::IntoIter`](https://github.com/rust-lang/rust/pull/80470)
* [disposition: merge] [Implement missing `AsMut<str>` for `str`](https://github.com/rust-lang/rust/pull/80279)
* [disposition: merge] [stabilise `cargo test -- --include-ignored`](https://github.com/rust-lang/rust/pull/80053)
* [disposition: merge] [Stabilize `peekable_next_if`](https://github.com/rust-lang/rust/pull/80011)
* [disposition: merge] [rustc: Stabilize `-Zrun-dsymutil` as `-Csplit-debuginfo`](https://github.com/rust-lang/rust/pull/79570)
* [disposition: merge] [Stabilize Arc::{increment,decrement}_strong_count](https://github.com/rust-lang/rust/pull/79285)
* [disposition: merge] [expand/resolve: Turn `#[derive]` into a regular macro attribute](https://github.com/rust-lang/rust/pull/79078)
* [disposition: merge] [Implement io::Seek for io::Empty](https://github.com/rust-lang/rust/pull/78044)
* [disposition: merge] [Tracking Issue for `feature(int_bits_const): <integer>::BITS`](https://github.com/rust-lang/rust/issues/76904)
* [disposition: merge] [Tracking Issue for `fmt::Arguments::as_str()`](https://github.com/rust-lang/rust/issues/74442)


## New RFCs

* [Change visibility scoping rules for macro_rules macros](https://github.com/rust-lang/rfcs/pull/3067)

# Upcoming Events

### Online
* [Februar 2, Dublin, IE - Rust Dublin Remote February Meetup - Rust Dublin](https://www.meetup.com/Rust-Dublin/events/275827557/)
* [February 2, Buffalo, NY, US - Buffalo Rust User Group - Buffalo Rust Meetup](https://www.meetup.com/Buffalo-Rust-Meetup/events/275593411/)
* [February 2, Denver, CO, US - ML in Rust, implementing logistic and linear regression from scratch - Rust Denver](https://www.meetup.com/Rust-Boulder-Denver/events/275352662/)
* [February 3, Johannesburg, ZA - Monthly Joburg Rust Chat! - Johannesburg Rust Meetup](https://www.meetup.com/Johannesburg-Rust-Meetup/events/275986420/)
* [February 4, Berlin, DE - Rust Hack and Learn - Berline.rs](https://www.meetup.com/opentechschool-berlin/events/txcprryccdbgb/)
* [February 4, Budapest, HU - Rust meetup S03! - Rust Hungary Meetup](https://www.meetup.com/Rust-Hungary-Meetup/events/275579644/)
* [February 7, Indianapolis, IN, US - Monthly Meetup - Indy.rs](https://www.meetup.com/indyrs/events/246726699/)
* [February 9, Seattle, WA, US - Monthly Meetup - Seattle Rust Meetup](https://www.meetup.com/Seattle-Rust-Meetup/events/gskksryccdbmb/)

### North America
* [February 10, Atlanta, GA, US - Grab a beer with fellow Rustaceans - Rust Atlanta](https://www.meetup.com/Rust-ATL/events/qxqdgryccdbnb/)

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

> Describing Rust as a systems programming language in 2021 is like describing Microsoft as Windows or Google as search. Yes, Rust is equipped for systems programming, but its applicability is much wider.

– [Tim McNamara on twitter](https://twitter.com/timClicks/status/1351247765851017216)

Thanks to [Nixon Enraght-Moony](https://users.rust-lang.org/t/twir-quote-of-the-week/328/993) for the suggestion.

[Please submit quotes and vote for next week!](https://users.rust-lang.org/t/twir-quote-of-the-week/328)

*This Week in Rust is edited by: [nellshamrell](https://github.com/nellshamrell), [llogiq](https://github.com/llogiq), and [cdmistman](https://github.com/cdmistman).*

<small>[Discuss on r/rust](https://www.reddit.com/r/rust/comments/k5nsab/this_week_in_rust_367/)</small>
