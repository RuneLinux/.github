# Rune
Description of Rune package manager ideas

## English

I wanted to have my own package manager that would bring together features scattered across other managers but never combined in one place. On top of that, I didn’t want to build an entirely new system from scratch — rather, rethink the existing one and take a slightly different path within its current framework.

Specific decisions:
- Execution queue and PATH  
An execution queue is implemented using PATH simply because it’s convenient. It also provides a natural read order, which effectively solves duplication issues without any additional mechanisms. As for the queue itself, it was chosen for the sake of maximum flexibility.

- Path registration and clean removal  
Clean removal was just a personal preference of mine, since after installing most programs the system ends up with a lot of files that are hard to track, and after removing them it’s even harder to understand whether something is still needed or just leftover junk. I consider explicit path registration the most balanced way to implement this — one that doesn’t interfere with unnecessary files. Some people might find it annoying, but here’s my view: if a developer doesn’t know exactly which files their program creates and where—without direct user involvement—then that program is generally unsafe to run, let alone distribute. Besides, this approach gives a lot of control to the end user.

## Русский

Мне хотелось иметь свой пакетный менеджер с функциями, что разбросаны по другим, но не собраны вместе. На это всё наложилось ещё и то, что я не хотел делать совершенно новую систему, а скорей переосмыслить и пройти немного другой путь в рамках текущей.

Конкретные решения:
- Очередь запуска и PATH  
Для очереди запуска используется PATH просто потому что это удобно. К тому же у него есть последовательность чтения, что по факту решает проблему с дублированием без дополнительных решений. Сама же очередь выбрана с точки зрения максимальной гибкости.
- Прописывание путей и чистое удаление  
Чистое удаление просто было моим небольшим пунктиком, ведь после установки большинства программ по системе появляется много файлов, что сложно отследить, а после удаления и понять нужно оно или это обычный мусор. Прописывание путей я считаю самым сбалансированным вариантом для его реализации, что не будет задевать лишние файлы. Кого-то может это и будет бесить, но у меня мнение такое: если разработчик не знает какие файлы и где без прямого участия пользователя создаст его программа - такую программу в целом небезопасно запускать, не говоря уж о распространении. Да и это даёт много возможностей конечному пользователю.
