# Algo1.0 - Combined Tactical Indicator Suite

## 📊 Descripción

**Algo1.0** es un indicador técnico avanzado para TradingView que combina múltiples estrategias de análisis técnico en una sola herramienta poderosa. Integra conceptos de Smart Money, detección de divergencias, análisis de tendencias ATR y dashboards informativos.

## 🎯 Características Principales

### 1. **ATR Trend Module**
Sistema de seguimiento de tendencias basado en ATR (Average True Range) con múltiples configuraciones:
- **10 tipos de ATR**: HMA, Classic ATR (RMA), LSMA, Ehlers Super Smoother, Optimum Elliptic Filter, Butterworth 2 Pole, Hann, SMA, EMA, WMA
- **Fast Trend**: Línea de tendencia rápida para señales tempranas
- **Smoothed Range Channel**: Canales dinámicos basados en rangos suavizados
- **Señales de compra/venta**: Alertas visuales cuando cambia la tendencia
- **Color coding avanzado**: Identificación visual de cambios de tendencia

### 2. **Mxwll Suite - Smart Money Concepts**
Implementación completa de conceptos institucionales:

#### External & Internal Structure
- **Break of Structure (BoS)**: Identificación de rupturas de estructura
- **Change of Character (CHoCH)**: Detección de cambios en el carácter del mercado
- **Swing Points**: HH, HL, LH, LL (Higher High, Higher Low, Lower High, Lower Low)
- **Sensibilidad ajustable**: 3 niveles (10, 25, 50 para externo / 3, 5, 8 para interno)

#### Order Blocks
- Visualización de zonas de órdenes institucionales
- Control de cantidad máxima a mostrar
- Eliminación automática cuando el precio las atraviesa

#### Fair Value Gaps (FVG)
- Detección de gaps de valor justo
- Opción de contracción cuando son parcialmente rellenados
- Modo "closest only" para mostrar solo los FVG más cercanos

#### Auto Fibonacci
Niveles de Fibonacci automáticos entre pivotes principales:
- 0.236, 0.382, 0.500, 0.618, 0.786
- Colores y visibilidad configurables por nivel

#### High/Low Levels
- Previous Day High/Low (1D)
- Rolling 4-Hour High/Low
- Etiquetas opcionales

#### Area of Interest (AOE)
Zonas de consolidación basadas en los últimos 50 candles

#### Session Zones
Zonas de sesión con colores de fondo:
- **NY Session**: 9:30 - 16:00 EST
- **Asia Session**: 20:00 - 02:00 EST
- **London Session**: 03:00 - 11:30 EST
- Control individual de visibilidad, color y transparencia para cada sesión

#### Session Dashboard
Panel informativo con:
- Sesión actual activa
- Tiempo restante hasta el cierre
- Tiempo hasta la próxima sesión
- Actividad de volumen

### 3. **Divergence Detection**
Sistema de detección de divergencias multi-indicador:

#### Indicadores Soportados
- MACD & MACD Histogram
- RSI
- Stochastic
- CCI
- Momentum
- OBV
- VWmacd
- Chaikin Money Flow
- Money Flow Index

#### Tipos de Divergencias
- **Regular**: Divergencias clásicas
- **Hidden**: Divergencias ocultas
- **Regular/Hidden**: Ambas simultáneamente

#### Configuración
- Período de pivot ajustable (1-50)
- Puntos de pivot máximos a revisar (1-20)
- Barras máximas a revisar (30-200)
- Opción de mostrar solo la última divergencia
- Visualización de números y líneas de divergencia

### 4. **RSI Dashboard**
Panel de información de RSI multi-timeframe:
- **9 posiciones** disponibles en pantalla
- **Tamaños configurables**: Auto, Tiny, Small, Normal, Large, Huge
- **Niveles personalizables**: Sobrecompra/Sobreventa
- **Código de colores**: Visual para identificar zonas rápidamente

## ⚙️ Configuración por Defecto

### ATR Trend
- **ATR Type**: HMA
- **ATR Weight**: 9.0
- **Fast ATR Weight**: 2.0
- **Show Fast Trend**: ✅ Activado
- **Show Buy/Sell Signals**: ✅ Activado
- **Advanced Color Coding**: ❌ Desactivado
- **Fill Fast Trend**: ✅ Activado
- **Fill Price/Trend**: ✅ Activado
- **Show Smoothed Range Channel**: ❌ Desactivado

### Mxwll Suite
- **External Structure**: ✅ Activado (Sensibilidad: 25)
- **Show HH/LH Labels**: ❌ Desactivado
- **Show HL/LL Labels**: ❌ Desactivado
- **Internal Structure**: ✅ Activado (Sensibilidad: 3)
- **Order Blocks**: ✅ Activado (Max: 10)
- **Fair Value Gaps**: ✅ Activado
- **Auto Fibs**: ✅ Activado (Todos los niveles)
- **High/Low Levels**: ✅ Activado (1D y 4H)
- **Area of Interest**: ✅ Activado
- **Session Zones**: ✅ Todas activadas (NY, Asia, London)
- **Session Dashboard**: ✅ Activado

### Divergences
- **Divergence Type**: Regular/Hidden
- **Maximum Pivot Points**: 20
- **Maximum Bars**: 200
- **Show Only Last**: ✅ Activado
- **Show Lines**: ❌ Desactivado
- **Show Indicator Names**: Don't Show

### RSI Dashboard
- **Position**: Bottom Right
- **Size**: Normal
- **Overbought**: 70
- **Oversold**: 30

## 🚀 Instalación

1. Abre TradingView
2. Navega a **Pine Editor**
3. Crea un nuevo indicador
4. Copia y pega el código de `algo1.0.pine`
5. Haz clic en **"Add to Chart"**

## 📖 Uso

### Señales de Trading

#### Compra (Buy)
- Triángulo verde hacia arriba aparece cuando:
  - ATR Trend cambia a alcista
  - Fast Trend cruza al alza
  - Precio rompe canal superior

#### Venta (Sell)
- Triángulo rojo hacia abajo aparece cuando:
  - ATR Trend cambia a bajista
  - Fast Trend cruza a la baja
  - Precio rompe canal inferior

### Interpretación de Colores

#### ATR Trend
- **Cyan (#00cbff)**: Tendencia alcista
- **Magenta (#ff0099)**: Tendencia bajista
- **Naranja (#ff4100)**: Cambio de tendencia pendiente de confirmación

#### Smart Money
- **Verde (#14D990)**: Alcista / Bullish
- **Rojo (#F24968)**: Bajista / Bearish
- **Amarillo (#F2B807)**: Fair Value Gaps

## 🎨 Personalización

Todos los módulos pueden ser habilitados/deshabilitados independientemente:
```
Enable ATR Trend
Enable Mxwll Suite
Enable Divergence Detection
Show RSI Dashboard
```

Cada sesión puede controlarse por separado con su propio color y transparencia.

## 📊 Compatibilidad

- **Versión Pine Script**: v6
- **TradingView**: Premium/Pro/Pro+ (para algunos timeframes inferiores)
- **Timeframes**: Todos (optimizado para 1m a 1D)
- **Mercados**: Forex, Crypto, Stocks, Indices, Commodities

## ⚠️ Limitaciones

- Máximo **500 labels, lines, boxes** simultáneos
- Máximo **500 bars back** para cálculos históricos
- Algunos features requieren timeframes específicos (sesiones, volumen)

## 📝 Créditos

Este indicador combina e integra conceptos de:
- **ATR Trend** por Daniel_Ge
- **Mxwll Suite** por Mxwll Capital
- **Divergence Detection** por LonesomeTheBlue

## 📄 Licencia

Mozilla Public License 2.0

## 🔄 Versión

**v1.0** - Diciembre 2025

## 📞 Soporte

Para reportar bugs o sugerir mejoras, abre un issue en el repositorio.

---

**⚡ Tip**: Comienza con la configuración por defecto y ajusta gradualmente según tu estilo de trading.
