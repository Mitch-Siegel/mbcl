
include_directories(include)

# list tests
add_executable(test-list test_list.c)
target_link_libraries(test-list mbcl)

add_test(NAME test_list_sort COMMAND test-list 1)
# rb tree tests
add_executable(test-rb-tree test_rb_tree.c)
target_link_libraries(test-rb-tree mbcl)

add_test(NAME rb_tree_test_ascending_insertion COMMAND test-rb-tree 0)
add_test(NAME rb_tree_test_descending_insertion COMMAND test-rb-tree 1)
add_test(NAME rb_tree_test_worst_case_insertion COMMAND test-rb-tree 2)
add_test(NAME rb_tree_test_find COMMAND test-rb-tree 3)
add_test(NAME rb_test_tree_not_find COMMAND test-rb-tree 4)
add_test(NAME rb_test_tree_remove_single COMMAND test-rb-tree 5)
add_test(NAME rb_test_tree_remove COMMAND test-rb-tree 6)
add_test(NAME rb_test_tree_remove_ascending COMMAND test-rb-tree 7)
add_test(NAME rb_test_tree_remove_descending COMMAND test-rb-tree 8)
add_test(NAME rb_test_tree_insert_million COMMAND test-rb-tree 9)
add_test(NAME rb_test_tree_remove_million COMMAND test-rb-tree 10)


# deque tests
add_executable(test-deque test_deque.c)
target_link_libraries(test-deque mbcl)

add_test(NAME test_deque_forward_queue COMMAND test-deque 0)
add_test(NAME test_deque_backward_queue COMMAND test-deque 1)
add_test(NAME test_deque_interleaved COMMAND test-deque 2)

# hash table tests
add_executable(test-hash-table test_hash_table.c)
target_link_libraries(test-hash-table mbcl)

add_test(NAME test_hash_table_insert_find COMMAND test-hash-table 0)
add_test(NAME test_hash_table_remove COMMAND test-hash-table 1)
add_test(NAME test_hash_table_iterator COMMAND test-hash-table 2)

# set tests
add_executable(test-set test_set.c)
target_link_libraries(test-set mbcl)