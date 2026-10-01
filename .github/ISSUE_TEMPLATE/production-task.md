name: Production task
about: تتبع مهمة كتابة أو بحث أو أصول أو صوت أو مونتاج
labels: production
body:
  - type: input
    id: episode
    attributes:
      label: الحلقة
      placeholder: EP01
    validations:
      required: true
  - type: dropdown
    id: phase
    attributes:
      label: المرحلة
      options:
        - بحث
        - كتابة
        - أصول بصرية
        - فيديو
        - صوت
        - مونتاج
        - مراجعة
        - إصدار
    validations:
      required: true
  - type: textarea
    id: task
    attributes:
      label: وصف المهمة
    validations:
      required: true
  - type: checkboxes
    id: acceptance
    attributes:
      label: شروط القبول
      options:
        - label: تم تسجيل المصدر/الأداة والحقوق
        - label: تمت مراجعة الاستمرارية
        - label: تم تحديث سجل الأصول
