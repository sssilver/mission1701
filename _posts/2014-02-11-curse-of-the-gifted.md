---
title: Curse of the Gifted
date: 2014-02-12 01:20:36 +0400
layout: post
---
<pre>Date:	Tue, 22 Aug 2000 16:00:52 -0400
From:	"Eric S. Raymond" <esr@thyrsus.com>
To:	Linus Torvalds <torvalds@transmeta.com>
Subject: Re: [PATCH] Re: Move of input drivers, some word needed from you

Linus Torvalds <torvalds@transmeta.com>:
> 
> 
> On Tue, 22 Aug 2000, Eric S. Raymond wrote:
> >
> > Linus Torvalds <torvalds@transmeta.com>:
> > > But the "common code helps" thing is WRONG. Face it. It can hurt. A lot.
> > > And people shouldn't think it is the God of CS.
> > 
> > I think you're mistaken about this. 
> 
> I'll give you a rule of thumb, and I can back it up with historical fact.
> You can back up yours with nada.

Yes, if twenty-seven years of engineering experience with complex
software in over fourteen languages and across a dozen operating
systems at every level from kernel out to applications is nada :-).
Now you listen to grandpa for a few minutes.  He may be an old fart,
but he was programming when you were in diapers and he's learned a few
tricks...

> Face it. Every once in a while, you have to start afresh. Tell people that
> "Ok, we can't share this code any more, it's getting to be a major
> disaster".

I'm not arguing that splitting a driver is always wrong -- I can
easily imagine making that call myself in your shoes, and for the
exact reasons you give.  I'm arguing that the perspective from which
you approach this issue causes you to underweight the benefits of
sharing code, and to not look for ways to do it as carefully and
systematically as you ought.

When you were in college, did you ever meet bright kids who graduated
top of their class in high-school and then floundered freshman year 
in college because they had never learned how to study?  It's a common
trap.  A friend of mine calls it "the curse of the gifted" -- a tendency
to lean on your native ability too much, because you've always been
rewarded for doing that and self-discipline would take actual work.

You are a brilliant implementor, more able than me and possibly (I say
this after consideration, and in all seriousness) the best one in the
Unix tradition since Ken Thompson himself.  As a consequence, you
suffer the curse of the gifted programmer -- you lean on your ability
so much that you've never learned to value certain kinds of coding
self-discipline and design craftsmanship that lesser mortals *must*
develop in order to handle the kind of problem complexity you eat for
breakfast.

Your tendency to undervalue modularization and code-sharing is one
symptom.  Another is your refusal to use systematic version-control or
release-engineering practices.  To you, these things seem mostly like
overhead and a way of needlessly complicating your life.  And so far,
your strategy has worked; your natural if relatively undisciplined
ability has proved more than equal to the problems you have set it.
That success predisposes you to relatively sloppy tactics like
splitting drivers before you ought to and using your inbox as a patch
queue.

But you make some of your more senior colleagues nervous.  See, we've
seen the curse of the gifted before.  Some of us were those kids in
college.  We learned the hard way that the bill always comes due --
the scale of the problems always increases to a point where your
native talent alone doesn't cut it any more.  The smarter you are, the
longer it takes to hit that crunch point -- and the harder the
adjustment when you finally do.  And we can see that *you*, poor damn
genius that you are, are cruising for a serious bruising.

As Linux grows, there will come a time when your raw talent is not
enough.  What happens then will depend on how much discipline about
coding and release practices and fastidiousness about clean design you
developed *before* you needed it, back when your talent was sufficient
to let you get away without.  The code-sharing issue -- more
specifically, your tendency to abandon modularization and re-use
before you probably ought to -- is part of this.  Andy Tanenbaum's
charge against you was not entirely without justice.

The larger problem is a chronic topic of face-to-face conversation
whenever two or more senior lkml people get together and you aren't
around.  You're our chosen benevolent dictator and maybe the second
coming of Ken, and we respect you and like you, but that doesn't mean
we're willing to close our eyes.  And when you react to cogent and
well-founded arguments like Rogier Wolff's as you have -- well, it
makes us more nervous.

I used to worry about what would happen if Linus got hit by a truck.
With all respect, I still worry about what will happen if the
complexity of the kernel exceeds the scope of your astonishing native
talent before you grow up.
-- 
		<a href="http://www.tuxedo.org/~esr/">Eric S. Raymond</a>
</pre>