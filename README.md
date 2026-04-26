#!/bin/bash

# Tạo 50 commit dummy
for i in {1..50}
do
    # Tạo file dummy hoặc chỉnh sửa file hiện có (nếu không có file nào thì tạo file mới)
    echo "Commit số $i - $(date)" >> dummy_commits.txt
    
    # Stage và commit
    git add dummy_commits.txt
    git commit -m "chore: commit dummy số $i - $(date '+%Y-%m-%d %H:%M:%S')"
    
    echo "Đã tạo commit $i/50"
done

echo "Hoàn thành! Đã tạo 50 commit."
