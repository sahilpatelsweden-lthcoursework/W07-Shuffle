error id: file://<HOME>/Programming/w07%20Shuffle/Deck.scala:scala/Array#
file://<HOME>/Programming/w07%20Shuffle/Deck.scala
empty definition using pc, found symbol in pc: scala/Array#
empty definition using semanticdb
empty definition using fallback
non-local guesses:
	 -Array#
	 -scala/Predef.Array#
offset: 135
uri: file://<HOME>/Programming/w07%20Shuffle/Deck.scala
text:
```scala
package poker

import scala.collection.immutable.ArraySeq

class Deck private (val initCards: ArraySeq[Card]):
  private var cards: Arr@@ay[Card] = initCards.toArray

  def reset(): Unit = cards = initCards.toArray

  def apply(i: Int): Card = cards(i)

  def toSeq: ArraySeq[Card] = cards.to(ArraySeq)

  def show: String = cards.map(_.show).mkString(" ")

  def peek(n: Int): ArraySeq[Card] = 
    cards.take(n).to(ArraySeq)

  def remove(n: Int): ArraySeq[Card] =
    val init = peek(n)
    cards = cards.drop(n)
    init
  end remove

  def prepend(moreCards: Card*): Unit = 
    cards = (moreCards ++ cards).toArray

  /** Swaps cards at position a and b. */
  def swap(a: Int, b: Int): Unit = ???

  /** Randomly reorders the cards in this deck. */
  def shuffle(): Unit = ???

object Deck:
  def apply(cards: Seq[Card]): Deck = new Deck(cards.to(ArraySeq))

  /** Creates a new full Deck with 52 cards in rank and suit order. */
  def full(): Deck = ???

```


#### Short summary: 

empty definition using pc, found symbol in pc: scala/Array#