With *Bounded Overtaking*, there is a limit to how many times one thread can overtake another. If a thread is delayed from entering the critical section, the delay will eventually end, allowing it to proceed after a bounded number of times the other thread enters the critical section. This is important to prevent starvation, ensuring that every thread gets a fair chance over time.

With *Unbounded Overtaking*, there is no limit on how many times a thread can overtake another. This means a thread might continually enter the critical section while another thread is delayed indefinitely, which could lead to starvation. In this case, the delayed thread might never get a chance to proceed if it continually loses the race for entry.

