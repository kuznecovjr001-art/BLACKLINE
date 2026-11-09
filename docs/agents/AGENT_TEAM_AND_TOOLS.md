# Команда ИИ-агентов и полезные репозитории

**Назначать ролям ограниченную зону ответственности; не позволять нескольким агентам править один модуль без объединяющего архитектора.**

Роли: (1) Product/ADR auditor — сверка решений GrillMe и нетривиальных запретов; (2) GIS urban planner — граф дорог, входы, инфраструктура; (3) architect/technical artist — фасады/Blender/LOD/лицензии; (4) Godot systems engineer — сцены, API, save schema; (5) physics/vehicle engineer; (6) character animation/IK; (7) AI/zombie perception and crowd LOD; (8) networking/persistence; (9) QA/performance and security reviewer. Все агенты под утверждённым task card, не «производят весь город автономно».

Кандидаты к подключению, только после проверки версии:
- Godot engine: https://github.com/godotengine/godot
- Blender (адаптация): https://www.blender.org/
- Terrain3D: https://github.com/TokisanGames/Terrain3D (terrain/foliage/heightmap; совместимость проверять)
- GdUnit4: https://github.com/godot-gdunit-labs/gdUnit4 (unit/integration tests); альтернатива GUT: https://github.com/bitwes/Gut — выбрать ОДИН по тестам.
- GDScript Toolkit: https://github.com/Scony/godot-gdscript-toolkit (gdformat, gdlint; версия для Godot 4)
- Voxel terrain optional: https://github.com/Zylann/godot_voxel (нужен только при реально разрушимом 3D-грунте, не автоматически)
- Godot MCP editor bridge candidate: https://github.com/Mobuis/godot-mcp2 — сторонний проект. До подключения audit безопасности/прав доступа, только локальный доступ, не открывать в интернет.
- Godot Jolt: движок встроен в Godot 4.6+, поэтому старый https://github.com/godot-jolt/godot-jolt НЕ ставить по умолчанию.

Порядок: локальный Godot CLI + Blender и Python → lint/test framework → GIS/asset pipeline → Terrain3D по измерениям → MCP после permission-audit. Каждый сторонний проект закреплять по версии, лицензии и тесту на текущей версии движка. Не обещать, что аддон решает стриминг всего Екатеринбурга автоматически.
