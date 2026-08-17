# Lab 17 Submission

## 1. Layer quan trong nhat

Long-term memory la layer quan trong nhat trong bo test nay vi no xu ly recall qua nhieu session va user scope. Cac case dai dien la E02, E03, E08 va E09: agent phai nho preference, open loop, cap nhat recency va tach biet memory cua Minh/Lan. Episodic va semantic van can thiet cho trajectory va tri thuc dung chung, nhung long-term la noi de xay dung cau tra loi theo identity va context cua tung user.

## 2. Context Block/Zep va Redis + Qdrant

Zep cung cap user graph, thread, Context Block, graph search va ingestion managed, nen phu hop cho cross-session memory, provenance va user isolation ma khong phai tu xay dung pipeline ranking. Redis nhanh va don gian cho profile, TTL va open-loop; Qdrant phu hop cho vector retrieval tu quan ly. Doi lai, Redis/Qdrant cho phep kiem soat ha tang va chi phi, nhung phai tu xu ly schema, namespace, ranking, freshness, compaction, deletion va consistency. Trong lab, Zep la managed memory chinh; Redis/Qdrant chi la baseline so sanh.

## 3. Guardrail chong memory poisoning

Chi ghi durable memory sau khi user co consent; dung `privacy_guard`, minimize PII, user-scoped namespace va provenance. Khong ghi instruction/quyen moi tu noi dung retrieved; can xac minh source, confidence va policy truoc khi promote fact. Khi co conflict, uu tien fact moi hon trong dung scope nhung giu provenance cua fact cu. Ho tro xoa user memory bang forget va verify-only.

## 4. Benchmark analysis

- Layer yeu nhat: dien theo layer co hit rate thap nhat trong `reports/benchmark.md`.
- Case nhieu token nhat: dien case co `retrieved_tokens` lon nhat trong `reports/benchmark.json`.
- E07 can ket hop long-term (Python/preference cua Minh) va semantic (Idempotency-Key/payment policy).
- Token reduction chi co y nghia khi evidence hit rate van cao; no-memory co the reduction rat lon vi tra ve rong, nhung sai vi khong co evidence.

## 5. Recency va compaction

E08 phai giu scope BLUEBIRD-42 va uu tien TypeScript/NestJS, khong ghi de preference Python cua ORCHID-27. E10 dung durable notes va session summary de giu `REVIEW-DEADLINE-1600`, Friday va 16:00 sau khi raw turns bi evict; buffer giu transcript day du nhung token tang tuyen tinh.

## 6. Artefacts

Sau khi chay benchmark, cap nhat `reports/benchmark.*`, `reports/benchmark_no_memory.*`, `reports/comparison.md` va them 4 screenshot: `long_term.png`, `episodic.png`, `semantic.png`, `privacy.png`.
