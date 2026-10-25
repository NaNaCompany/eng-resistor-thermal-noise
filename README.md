# 저항 열잡음 전압 계산기

저항과 온도, 등가잡음대역폭으로 저항 양단의 열잡음 실효전압 계산.

- ID: E141
- App: https://nanalab.kr/eng-resistor-thermal-noise/
- Repository: https://github.com/NaNaCompany/eng-resistor-thermal-noise
- Formula: Vₙ,rms = √(4k_BTRB)

## Model and data

열평형의 이상 저항과 고전적인 백색 열잡음 모델입니다. B는 필터의 등가잡음대역폭으로, 임의의 −3 dB 대역폭과 같지 않을 수 있습니다. 부하가 없는 저항 양단 전압이며, 부하 분압·초과잡음·양자 고주파 보정은 제외합니다. 사용 주파수에서 hf ≪ k_BT인지 별도로 확인하세요.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
