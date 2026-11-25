# 基层转诊与专家下沉资料基线

CSV 使用 UTF-8 编码，首行为字段名。资料仅提供项目所需的合成事实，空值代表来源尚未提供。

- `visits.csv`：基线资料，首行为 `visit,token,township,condition,visit_date,outcome`。
- `referrals.csv`：基线资料，首行为 `referral,token,condition,requested_on,urgency,status`。
- `sessions.csv`：基线资料，首行为 `session,expert,condition,clinic,date,slots,used`。
- `followups.csv`：基线资料，首行为 `referral,returned_on,result,source_version`。

## 基线检查

运行 `python3 -m unittest discover -s tests -v` 可检查资料可读性、主键唯一性和版本锚点。该检查不实现业务分析能力。
