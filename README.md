# Deneb_Vega-Stacked-Bar-Chart
Deneb Vega stacked bar, sorted, and custom colors
{
  "data": {"name": "dataset"},
  "transform": [
    {
      "calculate": "indexof(['FA', 'SP', 'SU'], datum.Semester)",
      "as": "order"
    }
  ],
  "mark": {
    "type": "bar"
  },
  "encoding": {
    "x": {
      "field": "Academic Year",
      "type": "nominal"
    },
    "y": {
      "field": "Traditional CH",
      "type": "quantitative"
    },
    "color": {
      "field": "Semester",
      "scale":
      {"domain": ["FA","SP","SU"], "range": ["#3C8A2E", "#BEC0C2","#000000"]
      }
    },
    "order": {"field": "order", "type": "ordinal"}
  }
}
