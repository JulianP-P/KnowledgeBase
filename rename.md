Общая логика
```
 ->for node : nodeList {
|    if node = транзакция {
|   -->анализ названия транзакции
|  |  if имя транзакции удовлеворяет маске {
|  |    while node != hashTree {
|  |       node = соседний элемент
|  |    }
|  |     nodeListHashTree = node.getchildren();
|  | -->for nodeHashTree: nodeListHashTree{
|  ||    if nodeHashTree = семплер {
|  ||       переименовываем семплер
|  ||     }
|  ||     if nodeHashTree = hashTree {
|  ||--------рекурсия
|  |       }
|  |      if nodeHashTree = транзакция {
|  |----------рекурсия
|          }
|        }
|     }
|  } else if(node.hasChildren()){
----------рекурсия
    }
  }
```
