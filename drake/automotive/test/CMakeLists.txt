drake_add_cc_test(curve2_test)
target_link_libraries(curve2_test drakeAutomotive)

drake_add_cc_test(simple_car_test)
target_link_libraries(simple_car_test drakeAutomotive)

drake_add_cc_test(simple_car_to_euler_floating_joint_test)
target_link_libraries(simple_car_to_euler_floating_joint_test drakeAutomotive)

drake_add_cc_test(trajectory_car_test)
target_link_libraries(trajectory_car_test drakeAutomotive)

drake_add_cc_test(linear_car_test)
target_link_libraries(linear_car_test drakeAutomotive)

drake_add_cc_test(idm_planner_test)
target_link_libraries(idm_planner_test drakeAutomotive)

drake_add_cc_test(single_lane_ego_and_agent_test)
target_link_libraries(single_lane_ego_and_agent_test drakeAutomotive)

if(lcm_FOUND)
  drake_add_cc_test(simple_car_state_translator_test)
  target_link_libraries(simple_car_state_translator_test drakeAutomotiveLcm)

  drake_add_cc_test(automotive_simulator_test automotive_simulator_test.cc)
  target_link_libraries(automotive_simulator_test drakeAutomotiveLcm)
endif()
