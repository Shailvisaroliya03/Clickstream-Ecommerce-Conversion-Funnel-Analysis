Objective

Build core visuals, KPIs, and the first complete version of the conversion funnel.

1. KPIs Created
  Sessions
    Sessions = DISTINCTCOUNT(fWebEvents[session_id])
  Orders
    Orders = DISTINCTCOUNT(fOrders[order_id])
  Conversion Rate
    Conversion Rate = DIVIDE([Orders], [Sessions])
  Average Order Value (AOV)
    AOV = DIVIDE(SUM(fOrders[order_value]), [Orders])
  Cart Abandonment Rate
  Cart Abandonment = 
    DIVIDE(
        [AddToCart Sessions] - [Checkout Sessions],
        [AddToCart Sessions]
    )
  Cost Per Acquisition (CPA)
    CPA = DIVIDE(SUM(fCampaignCost[cost]), [Orders])

These measures form the core logic behind all Week 2 visuals.

2. Funnel Visualization (Main Page)
  Built full customer journey funnel:
    Homepage → Product Page → Add to Cart → Checkout → Purchase

  Included:
    Funnel chart showing drop-off % between each stage
    KPIs on top (Sessions, Orders, Conversion Rate, CPA, AOV)
    Device filter
    Date range filter
    Campaign filter

3. Supporting Charts Added
  Sessions by Event Type
  Checkout Conversion Rate by Device
  Orders by Device
  Campaign Performance (basic version)

4. Page-Level Design
  Used consistent theme
  Used clean KPI cards
  Proper spacing + alignment
  No unnecessary visuals (kept it analytical, not decorative)

5. Week 2 Output Summary

  First full dashboard page completed
  PDF export of Week 2 dashboard included
  All core KPIs + core DAX created
  Working filters added
  Funnel chart functional
