# Node-API Overview

## Generic JavaScript API

<table>
<tbody><tr><td valign="top">

## Key types
- [`napi_env`](https://nodejs.org/api/n-api.html#napi_env) – the environment (per module, per context)<br>
- [`napi_value`](https://nodejs.org/api/n-api.html#napi_value) – stack-based value<br>
- [`napi_ref`](https://nodejs.org/api/n-api.html#napi_ref) – persistent value (wraps napi_value)<br>
- [`napi_status`](https://nodejs.org/api/n-api.html#napi_status) – returned by each function.<br>
  - `napi_ok` – no issues
  - `napi_pending_exception` – JS exception
  - other error statuses

</td><td valign="top">

## Environment
[`napi_get_global`](https://nodejs.org/api/n-api.html#napi_get_global)
[`napi_get_version`](https://nodejs.org/api/n-api.html#napi_get_version)
[`napi_run_script`](https://nodejs.org/api/n-api.html#napi_run_script)
[`napi_set_instance_data`](https://nodejs.org/api/n-api.html#napi_set_instance_data)
[`napi_get_instance_data`](https://nodejs.org/api/n-api.html#napi_get_instance_data)
[`napi_adjust_external_memory`](https://nodejs.org/api/n-api.html#napi_adjust_external_memory)

## Error handling
[`napi_get_last_error_info`](https://nodejs.org/api/n-api.html#napi_get_last_error_info)
[`napi_is_exception_pending`](https://nodejs.org/api/n-api.html#napi_is_exception_pending)
[`napi_get_and_clear_last_exception`](https://nodejs.org/api/n-api.html#napi_get_and_clear_last_exception)

</td></tr></tbody>
</table>

<table>
<tbody><tr><td valign="top">

## Value types
[`napi_undefined`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_null`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_boolean`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_number`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_string`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_symbol`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_object`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_function`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_external`](https://nodejs.org/api/n-api.html#napi_valuetype)
[`napi_bigint`](https://nodejs.org/api/n-api.html#napi_valuetype)

</td><td valign="top">

## Get value type
[`napi_typeof`](https://nodejs.org/api/n-api.html#napi_typeof)

## Value equality
[`napi_strict_equals`](https://nodejs.org/api/n-api.html#napi_strict_equals)

## Value coercion
[`napi_coerce_to_bool`](https://nodejs.org/api/n-api.html#napi_coerce_to_bool)
[`napi_coerce_to_number`](https://nodejs.org/api/n-api.html#napi_coerce_to_number)
[`napi_coerce_to_object`](https://nodejs.org/api/n-api.html#napi_coerce_to_object)
[`napi_coerce_to_string`](https://nodejs.org/api/n-api.html#napi_coerce_to_string)

</td><td valign="top">

## Value scoping
[`napi_open_handle_scope`](https://nodejs.org/api/n-api.html#napi_open_handle_scope)
[`napi_close_handle_scope`](https://nodejs.org/api/n-api.html#napi_close_handle_scope)
[`napi_open_escapable_handle_scope`](https://nodejs.org/api/n-api.html#napi_open_escapable_handle_scope)
[`napi_close_escapable_handle_scope`](https://nodejs.org/api/n-api.html#napi_close_escapable_handle_scope)
[`napi_escape_handle`](https://nodejs.org/api/n-api.html#napi_escape_handle)

## Persistent values
[`napi_create_reference`](https://nodejs.org/api/n-api.html#napi_create_reference)
[`napi_delete_reference`](https://nodejs.org/api/n-api.html#napi_delete_reference)
[`napi_reference_ref`](https://nodejs.org/api/n-api.html#napi_reference_ref)
[`napi_reference_unref`](https://nodejs.org/api/n-api.html#napi_reference_unref)
[`napi_get_reference_value`](https://nodejs.org/api/n-api.html#napi_get_reference_value)

</td></tr></tbody>
</table>

<table>
<tbody><tr><td valign="top">

## Undefined
[`napi_get_undefined`](https://nodejs.org/api/n-api.html#napi_get_undefined)

## Null
[`napi_get_null`](https://nodejs.org/api/n-api.html#napi_get_null)

## Boolean
[`napi_get_boolean`](https://nodejs.org/api/n-api.html#napi_get_boolean)
[`napi_get_value_bool`](https://nodejs.org/api/n-api.html#napi_get_value_bool)

## Number
[`napi_create_double`](https://nodejs.org/api/n-api.html#napi_create_double)
[`napi_create_int32`](https://nodejs.org/api/n-api.html#napi_create_int32)
[`napi_create_uint32`](https://nodejs.org/api/n-api.html#napi_create_uint32)
[`napi_create_int64`](https://nodejs.org/api/n-api.html#napi_create_int64)
[`napi_get_value_double`](https://nodejs.org/api/n-api.html#napi_get_value_double)
[`napi_get_value_int32`](https://nodejs.org/api/n-api.html#napi_get_value_int32)
[`napi_get_value_uint32`](https://nodejs.org/api/n-api.html#napi_get_value_uint32)
[`napi_get_value_int64`](https://nodejs.org/api/n-api.html#napi_get_value_int64)

## Symbol
[`napi_create_symbol`](https://nodejs.org/api/n-api.html#napi_create_symbol)
[`node_api_symbol_for`](https://nodejs.org/api/n-api.html#node_api_symbol_for)

</td><td valign="top">

## String
[`napi_create_string_latin1`](https://nodejs.org/api/n-api.html#napi_create_string_latin1)
[`napi_create_string_utf8`](https://nodejs.org/api/n-api.html#napi_create_string_utf8)
[`napi_create_string_utf16`](https://nodejs.org/api/n-api.html#napi_create_string_utf16)
[`napi_get_value_string_latin1`](https://nodejs.org/api/n-api.html#napi_get_value_string_latin1)
[`napi_get_value_string_utf8`](https://nodejs.org/api/n-api.html#napi_get_value_string_utf8)
[`napi_get_value_string_utf16`](https://nodejs.org/api/n-api.html#napi_get_value_string_utf16)

## Object
[`napi_create_object`](https://nodejs.org/api/n-api.html#napi_create_object)
[`napi_get_prototype`](https://nodejs.org/api/n-api.html#napi_get_prototype)
[`napi_object_freeze`](https://nodejs.org/api/n-api.html#napi_object_freeze)
[`napi_object_seal`](https://nodejs.org/api/n-api.html#napi_object_seal)
[`napi_define_properties`](https://nodejs.org/api/n-api.html#napi_define_properties)
[`napi_get_property_names`](https://nodejs.org/api/n-api.html#napi_get_property_names)
[`napi_get_all_property_names`](https://nodejs.org/api/n-api.html#napi_get_all_property_names)
[`napi_set_property`](https://nodejs.org/api/n-api.html#napi_set_property)
[`napi_has_property`](https://nodejs.org/api/n-api.html#napi_has_property)
[`napi_get_property`](https://nodejs.org/api/n-api.html#napi_get_property)
[`napi_delete_property`](https://nodejs.org/api/n-api.html#napi_delete_property)
[`napi_has_own_property`](https://nodejs.org/api/n-api.html#napi_has_own_property)
[`napi_set_named_property`](https://nodejs.org/api/n-api.html#napi_set_named_property)
[`napi_has_named_property`](https://nodejs.org/api/n-api.html#napi_has_named_property)
[`napi_get_named_property`](https://nodejs.org/api/n-api.html#napi_get_named_property)
[`napi_set_element`](https://nodejs.org/api/n-api.html#napi_set_element)
[`napi_has_element`](https://nodejs.org/api/n-api.html#napi_has_element)
[`napi_get_element`](https://nodejs.org/api/n-api.html#napi_get_element)
[`napi_delete_element`](https://nodejs.org/api/n-api.html#napi_delete_element)

</td><td valign="top">

## Function
[`napi_create_function`](https://nodejs.org/api/n-api.html#napi_create_function)
[`napi_define_class`](https://nodejs.org/api/n-api.html#napi_define_class)
[`napi_call_function`](https://nodejs.org/api/n-api.html#napi_call_function)
[`napi_new_instance`](https://nodejs.org/api/n-api.html#napi_new_instance)
[`napi_instanceof`](https://nodejs.org/api/n-api.html#napi_instanceof)
[`napi_get_cb_info`](https://nodejs.org/api/n-api.html#napi_get_cb_info)
[`napi_get_new_target`](https://nodejs.org/api/n-api.html#napi_get_new_target)

## External values
[`napi_create_external`](https://nodejs.org/api/n-api.html#napi_create_external)
[`napi_get_value_external`](https://nodejs.org/api/n-api.html#napi_get_value_external)
[`napi_wrap`](https://nodejs.org/api/n-api.html#napi_wrap)
[`napi_unwrap`](https://nodejs.org/api/n-api.html#napi_unwrap)
[`napi_remove_wrap`](https://nodejs.org/api/n-api.html#napi_remove_wrap)
[`napi_add_finalizer`](https://nodejs.org/api/n-api.html#napi_add_finalizer)
[`napi_type_tag_object`](https://nodejs.org/api/n-api.html#napi_type_tag_object)
[`napi_check_object_type_tag`](https://nodejs.org/api/n-api.html#napi_check_object_type_tag)

## BigInt
[`napi_create_bigint_int64`](https://nodejs.org/api/n-api.html#napi_create_bigint_int64)
[`napi_create_bigint_uint64`](https://nodejs.org/api/n-api.html#napi_create_bigint_uint64)
[`napi_create_bigint_words`](https://nodejs.org/api/n-api.html#napi_create_bigint_words)
[`napi_get_value_bigint_int64`](https://nodejs.org/api/n-api.html#napi_get_value_bigint_int64)
[`napi_get_value_bigint_uint64`](https://nodejs.org/api/n-api.html#napi_get_value_bigint_uint64)
[`napi_get_value_bigint_words`](https://nodejs.org/api/n-api.html#napi_get_value_bigint_words)

</td></tr></tbody>
</table>

<table>
<tbody><tr><td valign="top">

## Error
[`napi_is_error`](https://nodejs.org/api/n-api.html#napi_is_error)
[`napi_create_error`](https://nodejs.org/api/n-api.html#napi_create_error)
[`napi_create_type_error`](https://nodejs.org/api/n-api.html#napi_create_type_error)
[`napi_create_range_error`](https://nodejs.org/api/n-api.html#napi_create_range_error)
[`node_api_create_syntax_error`](https://nodejs.org/api/n-api.html#node_api_create_syntax_error)
[`napi_throw`](https://nodejs.org/api/n-api.html#napi_throw)
[`napi_throw_error`](https://nodejs.org/api/n-api.html#napi_throw_error)
[`napi_throw_type_error`](https://nodejs.org/api/n-api.html#napi_throw_type_error)
[`napi_throw_range_error`](https://nodejs.org/api/n-api.html#napi_throw_range_error)
[`node_api_throw_syntax_error`](https://nodejs.org/api/n-api.html#node_api_throw_syntax_error)

## Array
[`napi_is_array`](https://nodejs.org/api/n-api.html#napi_is_array)
[`napi_create_array`](https://nodejs.org/api/n-api.html#napi_create_array)
[`napi_create_array_with_length`](https://nodejs.org/api/n-api.html#napi_create_array_with_length)
[`napi_get_array_length`](https://nodejs.org/api/n-api.html#napi_get_array_length)

</td><td valign="top">

## ArrayBuffer
[`napi_is_arraybuffer`](https://nodejs.org/api/n-api.html#napi_is_arraybuffer)
[`napi_create_arraybuffer`](https://nodejs.org/api/n-api.html#napi_create_arraybuffer)
[`napi_create_external_arraybuffer`](https://nodejs.org/api/n-api.html#napi_create_external_arraybuffer)
[`napi_get_arraybuffer_info`](https://nodejs.org/api/n-api.html#napi_get_arraybuffer_info)
[`napi_detach_arraybuffer`](https://nodejs.org/api/n-api.html#napi_detach_arraybuffer)
[`napi_is_detached_arraybuffer`](https://nodejs.org/api/n-api.html#napi_is_detached_arraybuffer)

## TypedArray
[`napi_is_typedarray`](https://nodejs.org/api/n-api.html#napi_is_typedarray)
[`napi_create_typedarray`](https://nodejs.org/api/n-api.html#napi_create_typedarray)
[`napi_get_typedarray_info`](https://nodejs.org/api/n-api.html#napi_get_typedarray_info)

## DataView
[`napi_is_dataview`](https://nodejs.org/api/n-api.html#napi_is_dataview)
[`napi_create_dataview`](https://nodejs.org/api/n-api.html#napi_create_dataview)
[`napi_get_dataview_info`](https://nodejs.org/api/n-api.html#napi_get_dataview_info)

</td><td valign="top">

## Promise
[`napi_is_promise`](https://nodejs.org/api/n-api.html#napi_is_promise)
[`napi_create_promise`](https://nodejs.org/api/n-api.html#napi_create_promise)
[`napi_resolve_deferred`](https://nodejs.org/api/n-api.html#napi_resolve_deferred)
[`napi_reject_deferred`](https://nodejs.org/api/n-api.html#napi_reject_deferred)

## Date
[`napi_is_date`](https://nodejs.org/api/n-api.html#napi_is_date)
[`napi_create_date`](https://nodejs.org/api/n-api.html#napi_create_date)
[`napi_get_date_value`](https://nodejs.org/api/n-api.html#napi_get_date_value)

</td></tr></tbody>
</table>

## Node.js specific API

<table>
<tbody><tr><td valign="top">

## Environment
[`napi_module_register`](https://nodejs.org/api/n-api.html#napi_module_register)
[`napi_fatal_error`](https://nodejs.org/api/n-api.html#napi_fatal_error)
[`napi_fatal_exception`](https://nodejs.org/api/n-api.html#napi_fatal_exception)
[`napi_get_node_version`](https://nodejs.org/api/n-api.html#napi_get_node_version)
[`node_api_get_module_file_name`](https://nodejs.org/api/n-api.html#node_api_get_module_file_name)
[`napi_add_env_cleanup_hook`](https://nodejs.org/api/n-api.html#napi_add_env_cleanup_hook)
[`napi_remove_env_cleanup_hook`](https://nodejs.org/api/n-api.html#napi_remove_env_cleanup_hook)
[`napi_open_callback_scope`](https://nodejs.org/api/n-api.html#napi_open_callback_scope)
[`napi_close_callback_scope`](https://nodejs.org/api/n-api.html#napi_close_callback_scope)
[`napi_add_async_cleanup_hook`](https://nodejs.org/api/n-api.html#napi_add_async_cleanup_hook)
[`napi_remove_async_cleanup_hook`](https://nodejs.org/api/n-api.html#napi_remove_async_cleanup_hook)
[`napi_get_uv_event_loop`](https://nodejs.org/api/n-api.html#napi_get_uv_event_loop)

## Thread safe function
[`napi_create_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_create_threadsafe_function)
[`napi_get_threadsafe_function_context`](https://nodejs.org/api/n-api.html#napi_get_threadsafe_function_context)
[`napi_call_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_call_threadsafe_function)
[`napi_acquire_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_acquire_threadsafe_function)
[`napi_release_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_release_threadsafe_function)
[`napi_unref_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_unref_threadsafe_function)
[`napi_ref_threadsafe_function`](https://nodejs.org/api/n-api.html#napi_ref_threadsafe_function)

</td><td valign="top">

## Async work
[`napi_async_init`](https://nodejs.org/api/n-api.html#napi_async_init)
[`napi_async_destroy`](https://nodejs.org/api/n-api.html#napi_async_destroy)
[`napi_make_callback`](https://nodejs.org/api/n-api.html#napi_make_callback)
[`napi_create_async_work`](https://nodejs.org/api/n-api.html#napi_create_async_work)
[`napi_delete_async_work`](https://nodejs.org/api/n-api.html#napi_delete_async_work)
[`napi_queue_async_work`](https://nodejs.org/api/n-api.html#napi_queue_async_work)
[`napi_cancel_async_work`](https://nodejs.org/api/n-api.html#napi_cancel_async_work)

## Buffer
[`napi_is_buffer`](https://nodejs.org/api/n-api.html#napi_is_buffer)
[`napi_create_buffer`](https://nodejs.org/api/n-api.html#napi_create_buffer)
[`napi_create_external_buffer`](https://nodejs.org/api/n-api.html#napi_create_external_buffer)
[`napi_create_buffer_copy`](https://nodejs.org/api/n-api.html#napi_create_buffer_copy)
[`napi_get_buffer_info`](https://nodejs.org/api/n-api.html#napi_get_buffer_info)

</td></tr></tbody>
</table>
