If one of the mapper crash, it rolls back to last_stream_id it saved in checkpoint.
If one of the reducer crash, it rolls back to wc it saved in ckpt.

A mapper changes last_stream_id as soon as it forwards word counts to reducers.