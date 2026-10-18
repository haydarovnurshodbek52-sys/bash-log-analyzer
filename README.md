# bash-log-analyzer

Log fayldagi eng ko'p uchragan IP manzillarni topuvchi Bash skripti.

## Nima qiladi
Log fayldan IP manzillarni regex bilan ajratadi, sanaydi va eng faollarini ko'rsatadi.
Brute-force yoki shubhali trafikni birinchi ko'rishda aniqlash uchun foydali.

## Ishlatish
```bash
chmod +x log-analyzer.sh
./log-analyzer.sh access.log        # top 10
./log-analyzer.sh access.log 5      # top 5
```

## Misol natija
```
      3 192.168.1.10
      2 10.0.0.5
      1 172.16.0.3
```

## Nimalar o'rgandim
- `grep -oE` bilan regex orqali ma'lumot ajratish
- `sort | uniq -c | sort -rn` pipe zanjiri
- Argumentlar (`$1`, `$2`) va xatolarni tekshirish

## Keyingi rejalar
- [ ] Python versiyasini yozish
- [ ] Faqat ma'lum vaqt oralig'ini tahlil qilish
