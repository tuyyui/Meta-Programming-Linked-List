#include <iostream>
template <class T>
class Node{
 // bunch of types
public:
  typedef T value_type;
  typedef T& reference_type;
  typedef T const& const_reference_type;
  typedef T* pointer_type;
  typedef T const* const_pointer_type;

  value_type m_value;
  Node* m_next;
};
template <class T>
class List{
  typedef Node<T> node_type;
  typedef node_type* node_pointer;
  public:
  typedef typename node_type::value_type value_type;
  typedef typename node_type::reference_type reference_type;
  typedef typename node_type::const_reference_type const_reference_type;
  void AddToNode(value_type);
  void LoopThroughNodes();

    node_pointer m_head = NULL;
    node_pointer m_curr;
};
 template <class T>
 void List<T>::AddToNode(value_type _data){
   node_pointer m_newnode = new node_type;
   m_newnode->m_value = _data;

   if(m_head == NULL){
    m_head = m_newnode;
    m_curr = m_head;
   }
   else
   {
       m_curr->m_next = m_newnode;
       m_curr = m_newnode;
   }

}
template <class T>
void List<T>::LoopThroughNodes(){

  node_pointer m_newnode = new node_type;
  m_newnode = m_head;
  for(int i = 0; i < 3; i++){
    std::cout << m_newnode->m_value << " " << std::endl;;
    m_newnode = m_newnode->m_next;
  }

}
int main()
{
    List<int> LinkedList;
    LinkedList.AddToNode(23);
    LinkedList.AddToNode(43);
    LinkedList.AddToNode(90);
    LinkedList.LoopThroughNodes();
    return 0;
}
