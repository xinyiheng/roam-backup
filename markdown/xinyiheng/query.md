- 如何使用query
    - QUERIES
    - and
    - Find all blocks matching multiple conditions – i.e. blocks or their parents containing multiple page or block references.
    - {{query: {and: page A page B }}}
      {{query: {and: [[articles]] ((block)) }}}
      {{query: {and: [[Tyler Cowen]] ((block)) [[econ]] }}}
    - or
    - Find all blocks matching any of a number of conditions – i.e. blocks or their parents containing any of the selected page or block references.
    - {{query: {or: page A page B }}}
      {{query: {or: [[Zen]] [[Buddhism]] }}}
      {{query: {or: Utah Idaho Montana }}}
    - not
    - Exclude blocks matching any of the page or block references selected.
    - {{query: {and: page A {not: page B }}}}
      {{query: {and: [[Slate Star Codex]] {not: [[psychiatry]] }}}}
    - between
    - Finds all blocks on daily pages and blocks mentioning a date between two days. You can use the following as a shorthand: [[today]], [[tomorrow]], [[yesterday]], [[last week]], [[next week]], [[last month]], and [[next month]]. Only works on Daily Notes page.
    - {{query: {between: [[January 1st, 2021]] [[today]] }}
      {{query: {and: [[mistakes]] {between: [[January 1st, 2020]] [[December 31st, 2020]] }}}}
      {{query: {and: [[TODO]] {between: [[last week]] [[today]] }}}}
