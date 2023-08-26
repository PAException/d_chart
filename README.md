# d_chart

D'Chart is the development of an existing package chart, namely **community_charts_flutter**.\
The purpose of this pakage is simple way to use chart from [community_charts_flutter](https://pub.dev/packages/community_charts_flutter).

# Usage

- [Full Documentation](https://flutterdlux.netlify.app/d_chart/)
- Wrap Chart with Widget Size like SizedBox, Container, Aspecration etc to set root size for chart
- Example

```dart
AspectRatio(
    aspectRatio: 16/9,
    child: DChartComboO(),
),

SizedBox(
    width: 240,
    height: 200,
    child: DChartComboN(),
),
```

<br>

| Code | Type    | Domain   |
| ---- | ------- | -------- |
| N    | Numeric | Number   |
| O    | Ordinal | String   |
| T    | Time    | DateTime |

<br>

| <div style="width:30px">No</div> | <div style="width:120px">Type</div>                                       | <div style="width:200px">Widget</div>                                                                | <div style="width:80px">Example</div>                                                                                                                                                                                            |
| :------------------------------: | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                1                 | [Bar](https://flutterdlux.netlify.app/d_chart/widgets/bar/)               | <div style="height:40px">DChartBarO</div>DChartBarT                                                  | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/bar.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}}        |
|                2                 | [Line](https://flutterdlux.netlify.app/d_chart/widgets/line/)             | <div style="height:40px">DChartLineN</div> DChartLineT                                               | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/line.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}}       |
|                3                 | [Scatter](https://flutterdlux.netlify.app/d_chart/widgets/scatter/)       | <div style="height:40px">DChartScatterN</div> DChartScatterT                                         | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/scatter.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}}    |
|                4                 | [Combo](https://flutterdlux.netlify.app/d_chart/widgets/combo/)           | <div style="height:40px">DChartComboN</div> <div style="height:40px">DChartComboO</div> DChartComboT | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/combo.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}}      |
|                5                 | [Pie](https://flutterdlux.netlify.app/d_chart/widgets/pie/)               | <div style="height:40px">DChartPieN</div> <div style="height:40px">DChartPieO</div> DChartPieT       | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/pie.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}}        |
|                6                 | [Bar Custom](https://flutterdlux.netlify.app/d_chart/widgets/bar_custom/) | DChartBarCustom                                                                                      | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/bar_custom.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}} |
|                7                 | [Single Bar](https://flutterdlux.netlify.app/d_chart/widgets/single_bar/) | DChartSingleBar                                                                                      | {{< image src="https://github.com/indratrisnar/d_chart/raw/master/pic/single_bar.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title=""  webp="false" >}} |

<br>

# Table of Content

1. [Bar](#bar)

   - [Image](#bar-image)
   - [Example](#bar-example)

2. [Line](#line)

   - [Image](#line-image)
   - [Example](#line-example)

3. [Pie](#pie)

   - [Image](#pie-image)
   - [Example](#pie-example)

4. [Donut](#donut)

   - [Image](#donut-image)
   - [Example](#donut-example)

5. [Gauge](#gauge)

   - [Image](#gauge-image)
   - [Example](#gauge-example)

6. [Bar Custom](#bar-custom)

   - [Image](#bar-custom-image)
   - [Example](#bar-custom-example)

7. [Time](#time)

   - [Image](#time-image)
   - [Example](#time-example)

8. [Scatter](#scatter)

   - [Image](#scatter-image)
   - [Example](#scatter-example)

9. [Single Bar](#single-bar)

   - [Image](#single-bar-image)
   - [Example](#single-bar-example)

10. Combo: [Move to Web Documentation](https://flutterdlux.netlify.app/d_chart_combo/)

11. [Other](#other)

12. Universal Tutorial

- [All Chart](https://www.youtube.com/watch?v=pw1GEJl7edU&list=PLMeCG4xYek-NxSGp2i2mINmeM7k1Rzj4U&index=2)

<br>

## Bar

### Bar Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_bar1.jpg" alt="dchart_bar1" height="540">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_bar2.jpg" alt="dchart_bar2" height="540">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_bar3.jpg" alt="dchart_bar3" height="540">
</p>

### Bar Example

```dart
DChartBar(
    data: [
        {
            'id': 'Bar',
            'data': [
                {'domain': '2020', 'measure': 3},
                {'domain': '2021', 'measure': 4},
                {'domain': '2022', 'measure': 6},
                {'domain': '2023', 'measure': 0.3},
            ],
        },
    ],
    domainLabelPaddingToAxisLine: 16,
    axisLineTick: 2,
    axisLinePointTick: 2,
    axisLinePointWidth: 10,
    axisLineColor: Colors.green,
    measureLabelPaddingToAxisLine: 16,
    barColor: (barData, index, id) => Colors.green,
    showBarValue: true,
),
```

<br>

## Line

Tutorial:

- [Line Chart From Data Collection](https://www.youtube.com/watch?v=mdMayNHY7so&list=PLMeCG4xYek-OdumjOowVcNmW_nVPPUVfa&index=7)

### Line Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_line1.jpg" alt="dchart_line1" height="540">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_line2.jpg" alt="dchart_line2" height="540">
</p>

### Line Example

```dart
DChartLine(
    data: [
        {
            'id': 'Line',
            'data': [
                {'domain': 0, 'measure': 4.1},
                {'domain': 2, 'measure': 4},
                {'domain': 3, 'measure': 6},
                {'domain': 4, 'measure': 1},
            ],
        },
    ],
    lineColor: (lineData, index, id) => Colors.amber,
),
```

<br>

## Pie

### Pie Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_pie1.jpg" alt="dchart_pie1" height="540">
</p>

### Pie Example

```dart
DChartPie(
    data: [
        {'domain': 'Flutter', 'measure': 28},
        {'domain': 'React Native', 'measure': 27},
        {'domain': 'Ionic', 'measure': 20},
        {'domain': 'Cordova', 'measure': 15},
    ],
    fillColor: (pieData, index) => Colors.purple,
),
```

<br>

## Donut

### Donut Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_pie2.jpg" alt="dchart_pie2" height="540">
</p>

### Donut Example

```dart
DChartPie(
    data: [
        {'domain': 'Flutter', 'measure': 28},
        {'domain': 'React Native', 'measure': 27},
        {'domain': 'Ionic', 'measure': 20},
        {'domain': 'Cordova', 'measure': 15},
    ],
    fillColor: (pieData, index) => Colors.purple,
    donutWidth: 30,
    labelColor: Colors.white,
),
```

<br>

## Gauge

### Gauge Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_gauge.jpg" alt="dchart_gauge" height="540">
</p>

### Gauge Example

```dart
DChartGauge(
    data: [
        {'domain': 'Off', 'measure': 30},
        {'domain': 'Warm', 'measure': 30},
        {'domain': 'Hot', 'measure': 30},
    ],
    fillColor: (pieData, index) {
        switch (pieData['domain']) {
            case 'Off':
            return Colors.green;
            case 'Warm':
            return Colors.orange;
            default:
            return Colors.red;
        }
    },
    showLabelLine: false,
    pieLabel: (pieData, index) {
        return "${pieData['domain']}";
    },
    labelPosition: PieLabelPosition.inside,
    labelPadding: 0,
    labelColor: Colors.white,
),
```

<br>

## Bar Custom

this is not depend on **community_charts_flutter**\

Tutorial:

- [Bar Chart Custom](https://www.youtube.com/watch?v=bm_80bzQ_M4&list=PLMeCG4xYek-OiZKkbBC7ZFvvsbKhr1HJD&index=4)

### Bar Custom Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_bar_custom1.png" alt="dchart_bar_custom1" height="240">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/dchart_bar_custom2.png" alt="dchart_bar_custom2" height="240">
</p>

### Bar Custom Example

```dart
// example 1
AspectRatio(
    aspectRatio: 16 / 9,
    child: DChartBarCustom(
        showDomainLine: true,
        showMeasureLine: true,
        showDomainLabel: true,
        showMeasureLabel: true,
        spaceBetweenItem: 8,
        listData: [
            DChartBarDataCustom(
                value: 13,
                label: 'Jan',
                color: Colors.blue,
            ),
            DChartBarDataCustom(value: 20, label: 'Feb'),
            DChartBarDataCustom(value: 30, label: 'Mar'),
            DChartBarDataCustom(value: 40, label: 'Apr'),
            DChartBarDataCustom(value: 25, label: 'Mei'),
        ],
    ),
),

// example 2
List ranking = [
    {'class': 'A', 'total': 23},
    {'class': 'B', 'total': 14},
    {'class': 'C', 'total': 8},
    {'class': 'D', 'total': 7},
    {'class': 'E', 'total': 21},
];
DChartBarCustom(
    loadingDuration: const Duration(milliseconds: 1500),
    showLoading: true,
    valueAlign: Alignment.topCenter,
    showDomainLine: true,
    showDomainLabel: true,
    showMeasureLine: true,
    showMeasureLabel: true,
    spaceDomainLabeltoChart: 10,
    spaceMeasureLabeltoChart: 5,
    spaceDomainLinetoChart: 15,
    spaceMeasureLinetoChart: 20,
    spaceBetweenItem: 16,
    radiusBar: const BorderRadius.only(
        topLeft: Radius.circular(8),
        topRight: Radius.circular(8),
    ),
    measureLabelStyle: const TextStyle(
        fontWeight: FontWeight.bold,
        fontSize: 16,
        color: Colors.purple,
    ),
    domainLabelStyle: const TextStyle(
        fontWeight: FontWeight.bold,
        fontSize: 16,
        color: Colors.purple,
    ),
    measureLineStyle:
        const BorderSide(color: Colors.amber, width: 2),
    domainLineStyle: const BorderSide(color: Colors.red, width: 2),
    max: 25,
    listData: List.generate(ranking.length, (index) {
        Color currentColor =
            Color((Random().nextDouble() * 0xFFFFFF).toInt());
        return DChartBarDataCustom(
            onTap: () {
                print(
                '${ranking[index]['class']} => ${ranking[index]['total']}',
                );
            },
            elevation: 8,
            value: ranking[index]['total'].toDouble(),
            label: ranking[index]['class'],
            color: currentColor.withOpacity(1),
            splashColor: Colors.blue,
            showValue: ranking[index]['class'] == 'C' ? false : true,
            valueStyle: ranking[index]['class'] == 'A'
                ? const TextStyle(
                    fontWeight: FontWeight.bold,
                    fontSize: 16,
                    color: Colors.black,
                    )
                : const TextStyle(
                    fontWeight: FontWeight.bold,
                    fontSize: 16,
                    color: Colors.white,
                    ),
            labelCustom: ranking[index]['class'] == 'B'
                ? Transform.rotate(
                    angle: 5.5,
                    child: const Text('Bagus'),
                    )
                : null,
            valueCustom: ranking[index]['total'] > 20
                ? Align(
                    alignment: Alignment.center,
                    child: Column(
                        mainAxisSize: MainAxisSize.min,
                        children: [
                        Container(
                            padding: const EdgeInsets.all(4),
                            decoration: BoxDecoration(
                            border: Border.all(width: 2),
                            shape: BoxShape.circle,
                            ),
                            child: Text(
                            '${ranking[index]['total']}',
                            style: const TextStyle(
                                fontSize: 11,
                                color: Colors.red,
                                fontWeight: FontWeight.w900,
                            ),
                            ),
                        ),
                        const Text(
                            '😄',
                            style: TextStyle(fontSize: 20),
                        ),
                        ],
                    ),
                    )
                : null,
            valueTooltip: '${ranking[index]['total']} Student',
        );
    }),
),
```

<br>

## Time

Chart for Time Series, it can be group and custom render chart view\
Render type:

1. DRenderLine
2. DRenderBar
3. DRenderTargetLine
4. DRenderPoint

Tutorial:

- [Intro Time Chart](https://youtu.be/WFkIh3IcCuY)
- [Domain](https://youtu.be/lWO_dx9UIUM)
- [Measure](https://youtu.be/2JTk8WTc0_w)
- [Title & Subtitle](https://youtu.be/lXZke9YcR9s)
- [Legend](https://youtu.be/lqcB19ciNBk)
- [DRenderLine](https://youtu.be/AmMQnxg8kqI)
- [DRenderTargetLine](https://youtu.be/oPxmlrvdOPo)
- [DRenderBar](https://youtu.be/5BFXZKRB7cg)
- [Issue Symbol Renderer When Change Render Type](https://youtu.be/CYx1tlsBMNY)
- [Color](https://youtu.be/cqgfzj9Elqg)
- [Action Listener](https://youtu.be/Df8nXgpTZgo)

### Time Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/time/dchart_time_bar.png" alt="dchart_bar1" width="340">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/time/dchart_time_line.png" alt="dchart_bar2" width="340">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/time/dchart_time_point.png" alt="dchart_bar3" width="340">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/time/dchart_time_target_line.png" alt="dchart_bar3" width="340">
</p>

### Time Example

```dart
DChartTime(
    chartRender: DRenderLine(),
    measureLabel: (value) => '${value}k',
    domainLabel: (dateTime) {
        // [DateFormat] from intl package
        return DateFormat('d MMM yy').format(dateTime!);
    },
    groupData: [
        DChartTimeGroup(
            id: 'Keyboard',
            color: Colors.blue,
            data: [
                DChartTimeData(time: DateTime(2023, 2, 1), value: 29),
                DChartTimeData(time: DateTime(2023, 2, 2), value: 73),
                DChartTimeData(time: DateTime(2023, 2, 4), value: 23),
                DChartTimeData(time: DateTime(2023, 2, 8), value: 56),
                DChartTimeData(time: DateTime(2023, 2, 9), value: 32),
                DChartTimeData(time: DateTime(2023, 2, 10), value: 21),
                DChartTimeData(time: DateTime(2023, 2, 12), value: 76),
                DChartTimeData(time: DateTime(2023, 2, 18), value: 91),
                DChartTimeData(time: DateTime(2023, 2, 20), value: 17),
            ],
        ),
    ],
),
```

<br>

## Scatter

Chart for Scatter Plot/Point Series, it can be group.\

Tutorial:

- [Intro Scatter Chart](https://youtu.be/J6Pg56IYrRI)

### Scatter Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/scatter/dchart_scatter.png" alt="dchart_scatter" width="340">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/scatter/dchart_scatter_2.png" alt="dchart_scatter" width="340">
</p>

### Scatter Example

```dart
final group1 = [
    DChartScatterData(
        domain: 1,
        measure: 23,
        size: 10,
        startPlot: DPlot(2, 10),
        type: SymbolType.rect,
    ),
    DChartScatterData(
        domain: 2,
        measure: 12,
        type: SymbolType.circle,
    ),
    DChartScatterData(domain: 3, measure: 19),
];
final group2 = [
    DChartScatterData(
        domain: 1,
        measure: 15,
        type: SymbolType.triangle,
    ),
    DChartScatterData(
        domain: 3, measure: 25, type: SymbolType.triangle, size: 15),
    DChartScatterData(domain: 5, measure: 7),
];

DChartScatter(
    trackType: TrackType.rectangle,
    borderWidth: (group, data, index) => 2,
    borderColor: (random, group, data) => Colors.red.withOpacity(0.8),
    groupData: [
        DChartScatterGroup(
            id: 'id',
            data: group1,
            color: Colors.amber,
        ),
        DChartScatterGroup(
            id: 'id2',
            data: group2,
            color: Colors.purple,
        ),
    ],
),
```

<br>

## Single Bar

This chart is devoted to making a comparison bar and progress bar display.\

Tutorial:

- [Intro Single Bar Chart](https://youtu.be/2JPnDN4VnV4)

### Single Bar Image

<p float="left">
    <img src="https://github.com/indratrisnar/d_chart/raw/master/pic/singlebar/dchart_singlebar.png" alt="dchart_scatter" width="340">
</p>

### Single Bar Example

```dart
DChartSingleBar(
    forgroundColor: Colors.green,
    value: 30,
    max: 80,
),
```

<br>

# Other

Support me for more feature & packages
[Donate](https://www.paypal.com/paypalme/indratrisnar)

Check my app : [Visit](https://indratrisnar.github.io/projects.html)

Check My Tutorial & Course : [Watch](https://www.youtube.com/channel/UC0d_xINEvCtlDCpWfBpnYpA)
