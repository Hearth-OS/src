serenity_component(
    PixelPaint
    RECOMMENDED
    TARGETS PixelPaint
    DEPENDS ImageDecoder
)

compile_gml(PixelPaintWindow.gml PixelPaintWindowGML.h pixel_paint_window_gml)

set(SOURCES
    BrushTool.cpp
    BucketTool.cpp
    CreateNewImageDialog.cpp
    CreateNewLayerDialog.cpp
    EllipseTool.cpp
    EraseTool.cpp
    Image.cpp
    ImageEditor.cpp
    Layer.cpp
    LayerListWidget.cpp
    LayerPropertiesWidget.cpp
    LineTool.cpp
    main.cpp
    MoveTool.cpp
    PaletteWidget.cpp
    PenTool.cpp
    PickerTool.cpp
    PixelPaintWindowGML.h
    RectangleTool.cpp
    RectangleSelectTool.cpp
    Selection.cpp
    SprayTool.cpp
    ToolboxWidget.cpp
    ToolPropertiesWidget.cpp
    Tool.cpp
    ZoomTool.cpp
)

serenity_app(PixelPaint ICON app-pixel-paint)
target_link_libraries(PixelPaint LibImageDecoderClient LibGUI LibGfx)
