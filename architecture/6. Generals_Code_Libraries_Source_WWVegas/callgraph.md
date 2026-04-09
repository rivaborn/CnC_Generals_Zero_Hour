# Call Graph & Dependency Diagrams

Auto-generated from per-file architecture docs.

## Function Call Graph

Showing functions with 2+ incoming calls. Limited to 150 edges.

```mermaid
%%{ init: { 'theme': 'dark', 'flowchart': { 'curve': 'basis' } } }%%
graph LR

  subgraph Generals
    _MultiListObjectClass__["~MultiListObjectClass()"]
    _PolygonInfoClass["~PolygonInfoClass"]
    Add_T_record__unsigned_key_["Add(T record, unsigned key)"]
    Add_Delayed_Release_Object["Add_Delayed_Release_Object"]
    Add_Files["Add_Files"]
    Add_Light["Add_Light"]
    Add_Object_Internal["Add_Object_Internal"]
    Base64_Decode["Base64_Decode"]
    Base64_Encode["Base64_Encode"]
    Base64Pipe__Flush["Base64Pipe::Flush"]
    Base64Pipe__Put["Base64Pipe::Put"]
    BasicTimerClass_T___operator_int["BasicTimerClass<T>::operator int"]
    BinaryHeapClass__Insert["BinaryHeapClass::Insert"]
    BinaryHeapClass__Percolate_Up["BinaryHeapClass::Percolate_Up"]
    BinaryHeapClass__Remove_Min["BinaryHeapClass::Remove_Min"]
    BinaryHeapClass__Resize_Array["BinaryHeapClass::Resize_Array"]
    Bit_Blit["Bit_Blit"]
    Bit_Blit__overload_1_["Bit_Blit (overload 1)"]
    Bitmap_Assert_bool_condition_["Bitmap_Assert(bool condition)"]
    Bitmap2DObjClass__copy_constructor_["Bitmap2DObjClass (copy constructor)"]
    Bitmap2DObjClass__filename_constructor_["Bitmap2DObjClass (filename constructor)"]
    Bitmap2DObjClass__texture_constructor_["Bitmap2DObjClass (texture constructor)"]
    Bitmap2DObjClass_const_char_filename______["Bitmap2DObjClass(const char filename, ...)"]
    Bitmap2DObjClass_TextureClass_texture______["Bitmap2DObjClass(TextureClass texture, ...)"]
    BitmapHandlerClass__Copy_Image__["BitmapHandlerClass::Copy_Image()"]
    BitmapHandlerClass__Copy_Image_Generate_Mipmap__["BitmapHandlerClass::Copy_Image_Generate_Mipmap()"]
    BitmapHandlerClass__Create_Mipmap_B8G8R8A8__["BitmapHandlerClass::Create_Mipmap_B8G8R8A8()"]
    Blit_Clip["Blit_Clip"]
    Blitter__Blit["Blitter::Blit"]
    BlowfishEngine__Decrypt["BlowfishEngine::Decrypt"]
    BlowfishEngine__Encrypt["BlowfishEngine::Encrypt"]
    BlowfishEngine__Submit_Key["BlowfishEngine::Submit_Key"]
    BooleanVectorClass__operator__["BooleanVectorClass::operator[]"]
    BoxRenderObjClass__Init__["BoxRenderObjClass::Init()"]
    Buff_Get["Buff_Get"]
    BufferPipe__Put["BufferPipe::Put"]
    BufferStraw__Get["BufferStraw::Get"]
    Build_AABTree["Build_AABTree"]
    Build_Sentence["Build_Sentence"]
    Build_Texture["Build_Texture"]
    Build_Textures["Build_Textures"]
    Build_W3D_AABTree_Recursive["Build_W3D_AABTree_Recursive"]
    BW_Render__Render_Triangle_Strip["BW_Render::Render_Triangle_Strip"]
    BW_Render__Render_Triangles["BW_Render::Render_Triangles"]
    BWRenderClass__Render_Triangle_Strip["BWRenderClass::Render_Triangle_Strip"]
    BWRenderClass__Render_Triangles["BWRenderClass::Render_Triangles"]
    Cast_AABox["Cast_AABox"]
    Cast_Ray["Cast_Ray"]
    Cast_Ray_Recursive["Cast_Ray_Recursive"]
    Cast_World_Space_AABox["Cast_World_Space_AABox"]
    CollisionMath__Overlap_Test_PlaneClass__AABoxClass_["CollisionMath::Overlap_Test(PlaneClass, AABoxClass)"]
    Color_to_Vector4["Color_to_Vector4"]
    Combine_Colors["Combine_Colors"]
    Compare_EXE_Version["Compare_EXE_Version"]
    Compute_Plane_Score["Compute_Plane_Score"]
    Copy_Emitter_Property_Struct["Copy_Emitter_Property_Struct"]
    CRC_Stringi["CRC_Stringi"]
    CRCPipe__Put["CRCPipe::Put"]
    CRCStraw__Get["CRCStraw::Get"]
    Create_Delayed_Release_Thread["Create_Delayed_Release_Thread"]
    Create_New_Particles["Create_New_Particles"]
    CriticalSectionClass__Lock__["CriticalSectionClass::Lock()"]
    CriticalSectionClass__Unlock__["CriticalSectionClass::Unlock()"]
    Cull["Cull"]
    DecalSystemClass__Lock_Decal_Generator["DecalSystemClass::Lock_Decal_Generator"]
    Delayed_Release_Thread_Proc["Delayed_Release_Thread_Proc"]
    DistLODDefClass__Load_W3D["DistLODDefClass::Load_W3D"]
    Do_Force_Links["Do_Force_Links"]
    Draw_Sentence["Draw_Sentence"]
    DynamicMeshClass__Set_Vertex_Color["DynamicMeshClass::Set_Vertex_Color"]
    DynamicMeshClass__Vertex["DynamicMeshClass::Vertex"]
    DynamicVectorClass_T___Add["DynamicVectorClass<T>::Add"]
    End_Delayed_Release_Thread["End_Delayed_Release_Thread"]
    End_Sample["End_Sample"]
    Evaluate["Evaluate"]
    file_auto_ptr__file_auto_ptr["file_auto_ptr/~file_auto_ptr"]
    file_auto_ptr_file_auto_ptr["file_auto_ptr/file_auto_ptr"]
    FileClass__Printf_char_buffer__int_bufferSize__char_str______["FileClass::Printf(char buffer, int bufferSize, char str, ...)"]
    FileClass__Printf_char_str______["FileClass::Printf(char str, ...)"]
    FileClass__Printf_Indented_unsigned_depth__char_str______["FileClass::Printf_Indented(unsigned depth, char str, ...)"]
    Filename_From_Asset_Name["Filename_From_Asset_Name"]
    Find_Factory_const_char_name_["Find_Factory(const char name)"]
    Find_POT["Find_POT"]
    Find_Tangents["Find_Tangents"]
    Flush["Flush"]
    Flush_Delayed_Release_Objects["Flush_Delayed_Release_Objects"]
    Font3DDataClass__Load_Font_Image["Font3DDataClass::Load_Font_Image"]
    Font3DDataClass__Make_Proportional["Font3DDataClass::Make_Proportional"]
    Font3DInstanceClass__String_Width["Font3DInstanceClass::String_Width"]
    Format["Format"]
    Format_Args["Format_Args"]
    FormatURLFromRegistry["FormatURLFromRegistry"]
    Free["Free"]
    Free_String["Free_String"]
    From_Buffer["From_Buffer"]
    Generate_APT["Generate_APT"]
    Generate_Prime["Generate_Prime"]
    GenericList__Delete["GenericList::Delete"]
    GenericNode__Link["GenericNode::Link"]
    Get_4x4_Block["Get_4x4_Block"]
    Get_Bounding_Sphere__["Get_Bounding_Sphere()"]
    Get_Bytes_Per_Pixel["Get_Bytes_Per_Pixel"]
    get_far_extent["get_far_extent"]
    Get_File_Id_String["Get_File_Id_String"]
    Get_First_uint32_superclass_id_["Get_First(uint32 superclass_id)"]
    Get_Image_File_Header__HINSTANCE_version_["Get_Image_File_Header (HINSTANCE version)"]
    Get_Material["Get_Material"]
    Get_Next_DefinitionFactoryClass_curr_factory__uint32_superclass_id_["Get_Next(DefinitionFactoryClass curr_factory, uint32 superclass_id)"]
    Get_Pixel["Get_Pixel"]
    Get_Render_Object["Get_Render_Object"]
    Get_Sample_Loop_Count["Get_Sample_Loop_Count"]
    Get_Sample_MS_Position["Get_Sample_MS_Position"]
    Get_Sample_Pan["Get_Sample_Pan"]
    Get_Sample_User_Data["Get_Sample_User_Data"]
    Get_Sample_Volume["Get_Sample_Volume"]
    Get_String["Get_String"]
    Get_Texture["Get_Texture"]
    Get_WW3D_Format["Get_WW3D_Format"]
    GetFileCreationTime["GetFileCreationTime"]
    getMipmapData_MultiRequest__m_["getMipmapData(MultiRequest& m)"]
    GetVersionInfo["GetVersionInfo"]
    HashTableClass__Add["HashTableClass::Add"]
    HashTableClass__Find["HashTableClass::Find"]
    HashTableClass__Hash["HashTableClass::Hash"]
    HashTableClass__Remove["HashTableClass::Remove"]
    HashTableIteratorClass__First["HashTableIteratorClass::First"]
    HashTableIteratorClass__Next["HashTableIteratorClass::Next"]
    Hires_Load["Hires_Load"]
    HModelLoaderClass__Load_W3D["HModelLoaderClass::Load_W3D"]
    HRawAnimClass__Get_Orientation["HRawAnimClass::Get_Orientation"]
    HRawAnimClass__Get_Transform["HRawAnimClass::Get_Transform"]
    HRawAnimClass__Load_W3D["HRawAnimClass::Load_W3D"]
    HTreeClass__Combo_Update["HTreeClass::Combo_Update"]
    HTreeClass__Load_W3D["HTreeClass::Load_W3D"]
    HTreeClass__Scale["HTreeClass::Scale"]
    IDBufferClass__Render_Triangle["IDBufferClass::Render_Triangle"]
    Init["Init"]
    Initialize["Initialize"]
    InputLightStruct__Init["InputLightStruct::Init"]
    Insert_After["Insert_After"]
    Insert_Before["Insert_Before"]
    Insert_To_Sorting_Pool["Insert_To_Sorting_Pool"]
    Insert_Triangles__overloads_["Insert_Triangles (overloads)"]
    Insert_VolumeParticle["Insert_VolumeParticle"]
    Int__exp_b_mod_c["Int::exp_b_mod_c"]
    Int__Inverse["Int::Inverse"]
    Internal_Remove__["Internal_Remove()"]
    Intersect_IntersectionClass___IntersectionResultClass__["Intersect(IntersectionClass , IntersectionResultClass )"]
    Intersect_Object_Array["Intersect_Object_Array"]
    Intersect_Sphere["Intersect_Sphere"]
    Intersect_Sphere_Quick["Intersect_Sphere_Quick"]
    Intersection_Test["Intersection_Test"]
    Is_Texture_Valid["Is_Texture_Valid"]
    LaunchWebBrowser["LaunchWebBrowser"]
    Load["Load"]
    Load_Alloc_Data["Load_Alloc_Data"]
    Load_Texture["Load_Texture"]
    Load_Variables["Load_Variables"]
    Load_Variables__["Load_Variables()"]
    Load_W3D["Load_W3D"]
    Load_W3D__["Load_W3D()"]
    Load_W3D_Save_W3D["Load_W3D/Save_W3D"]
    Lock_Parameter["Lock_Parameter"]
    Log["Log"]
    Log_Textures["Log_Textures"]
    LookupTableMgrClass__Get_Table["LookupTableMgrClass::Get_Table"]
    MaterialCollectorClass__Collect_Materials["MaterialCollectorClass::Collect_Materials"]
    MaterialRemapperClass__Remap_Mesh["MaterialRemapperClass::Remap_Mesh"]
    MeshLoaderClass__Load_W3D["MeshLoaderClass::Load_W3D"]
    MeshMatDescClass__Post_Load_Process["MeshMatDescClass::Post_Load_Process"]
    MeshModelClass__Load_W3D["MeshModelClass::Load_W3D"]
    Message_Handler["Message_Handler"]
    MetalMapManagerClass_INIClass__ini_["MetalMapManagerClass(INIClass &ini)"]
    MultiFixedPoolDecalSystemClass__Clear_Decal_Slot["MultiFixedPoolDecalSystemClass::Clear_Decal_Slot"]
    MultiFixedPoolDecalSystemClass__Unlock_Decal_Generator["MultiFixedPoolDecalSystemClass::Unlock_Decal_Generator"]
    MultiListObjectClass___MultiListObjectClass["MultiListObjectClass::~MultiListObjectClass"]
    MutexClass__Lock_int_time_["MutexClass::Lock(int time)"]
    MutexClass__Unlock__["MutexClass::Unlock()"]
    NTreeLeafClass_T___Add["NTreeLeafClass<T>::Add"]
    NullLoaderClass__Load_W3D["NullLoaderClass::Load_W3D"]
    ObjectPoolClass__Allocate_Object["ObjectPoolClass::Allocate_Object"]
    ObjectPoolClass__Free_Object["ObjectPoolClass::Free_Object"]
    On_Event["On_Event"]
    operator____DummyPtrType_["operator!= (DummyPtrType)"]
    operator___overloads_["operator+ (overloads)"]
    operator____DummyPtrType_["operator== (DummyPtrType)"]
    Optimize_Strip_Order["Optimize_Strip_Order"]
    Optimize_Triangle_Order["Optimize_Triangle_Order"]
    Overlap_Test_const_OBBoxClass____const_LineSegClass___["Overlap_Test(const OBBoxClass &, const LineSegClass &)"]
    Overlap_Test_const_SphereClass____const_AABoxClass___["Overlap_Test(const SphereClass &, const AABoxClass &)"]
    Overlap_Test_const_SphereClass____const_OBBoxClass___["Overlap_Test(const SphereClass &, const OBBoxClass &)"]
    Overlap_Test_PlaneClass__OBBoxClass_["Overlap_Test(PlaneClass, OBBoxClass)"]
    ParticleBufferClass__["ParticleBufferClass()"]
    ParticleEmitterDefClass__Load_W3D["ParticleEmitterDefClass::Load_W3D"]
    ParticleEmitterDefClass__Save_W3D["ParticleEmitterDefClass::Save_W3D"]
    ParticleEmitterLoaderClass__Load_W3D["ParticleEmitterLoaderClass::Load_W3D"]
    Partition["Partition"]
    PKey__Decrypt["PKey::Decrypt"]
    PKey__Encode_Exponent___Decode_Exponent["PKey::Encode_Exponent / Decode_Exponent"]
    PKey__Encode_Modulus___Decode_Modulus["PKey::Encode_Modulus / Decode_Modulus"]
    PKey__Encrypt["PKey::Encrypt"]
    PKey__Generate["PKey::Generate"]
    Play["Play"]
    PointGroupClass___Shutdown["PointGroupClass::_Shutdown"]
    PointGroupClass__RenderVolumeParticle["PointGroupClass::RenderVolumeParticle"]
    PointGroupClass__Update_Arrays["PointGroupClass::Update_Arrays"]
    Pop_Material_Pass["Pop_Material_Pass"]
    Pop_Override_Flags["Pop_Override_Flags"]
    Post_Load_Processing["Post_Load_Processing"]
    PriorityMultiListIterator__Process_Head["PriorityMultiListIterator::Process_Head"]
    Process__["Process()"]
    Process_DD_Result["Process_DD_Result"]
    Process_Head["Process_Head"]
    Push_Material_Pass["Push_Material_Pass"]
    Push_Override_Flags["Push_Override_Flags"]
    Put_Key_Message["Put_Key_Message"]
    Put_Mouse_Message["Put_Mouse_Message"]
    RawFileClass__Bias["RawFileClass::Bias"]
    RawFileClass__Open["RawFileClass::Open"]
    RawFileClass__Read["RawFileClass::Read"]
    RawFileClass__Seek["RawFileClass::Seek"]
    RawFileClass__Write["RawFileClass::Write"]
    Read["Read"]
    read_header["read_header"]
    Read_PCX_File["Read_PCX_File"]
    read_vertices["read_vertices"]
    RefMultiListClass__Add["RefMultiListClass::Add"]
    Register_Factory_DefinitionFactoryClass_factory_["Register_Factory(DefinitionFactoryClass factory)"]
    Remove["Remove"]
    Remove_All["Remove_All"]
    Remove_Head["Remove_Head"]
    Remove_Tail["Remove_Tail"]
    Render["Render"]
    Render_Preprocessed_Triangle["Render_Preprocessed_Triangle"]
    Render_Seg_Line["Render_Seg_Line"]
    Render_Streak_Line["Render_Streak_Line"]
    Render_Triangle_Strip["Render_Triangle_Strip"]
    Render_Triangles["Render_Triangles"]
    Render2DClass__Add_Quad["Render2DClass::Add_Quad"]
    Render2DClass__Add_Quad__["Render2DClass::Add_Quad()"]
    Render2DTextClass__Draw_Char["Render2DTextClass::Draw_Char"]
    Render2DTextClass__Draw_Text["Render2DTextClass::Draw_Text"]
    Render2DTextClass__Draw_Text__["Render2DTextClass::Draw_Text()"]
    RenderDeviceDescClass__operator_["RenderDeviceDescClass::operator="]
    RenderStreak["RenderStreak"]
    Reset["Reset"]
    Reset_Model["Reset_Model"]
    Resize["Resize"]
    Resume_Sample["Resume_Sample"]
    Return_Render_Object["Return_Render_Object"]
    RGB_to_CIEY["RGB_to_CIEY"]
    RGB565_To_ARGB8888["RGB565_To_ARGB8888"]
    RLE_Blit__overload_1_["RLE_Blit (overload 1)"]
    RLE_Blit__overload_2_["RLE_Blit (overload 2)"]
    Save["Save"]
    Save_Texture["Save_Texture"]
    Save_Variables__["Save_Variables()"]
    Save_W3D__["Save_W3D()"]
    Seek["Seek"]
    Select_Splitting_Plane["Select_Splitting_Plane"]
    Set_Animation["Set_Animation"]
    Set_Arrays["Set_Arrays"]
    Set_LocsWidthsColors["Set_LocsWidthsColors"]
    Set_Material["Set_Material"]
    Set_Palette["Set_Palette"]
    Set_Sample_Loop_Count["Set_Sample_Loop_Count"]
    Set_Sample_MS_Position["Set_Sample_MS_Position"]
    Set_Sample_Pan["Set_Sample_Pan"]
    Set_Sample_User_Data["Set_Sample_User_Data"]
    Set_Sample_Volume["Set_Sample_Volume"]
    Set_Shader["Set_Shader"]
    Set_Texture["Set_Texture"]
    Set_Transform["Set_Transform"]
    Set_Video_Mode["Set_Video_Mode"]
    Setup_Mix_File["Setup_Mix_File"]
    ShaderClass__Enable_Fog["ShaderClass::Enable_Fog"]
    ShaderClass__Guess_Sort_Level["ShaderClass::Guess_Sort_Level"]
    SHAEngine__Hash["SHAEngine::Hash"]
    SHAEngine__Process_Block["SHAEngine::Process_Block"]
    SHAEngine__Result["SHAEngine::Result"]
    SHAPipe__Put["SHAPipe::Put"]
    SHAPipe__Result["SHAPipe::Result"]
    SHAStraw__Get["SHAStraw::Get"]
    Shutdown["Shutdown"]
    SimpleDynVecClass__Add["SimpleDynVecClass::Add"]
    SimpleDynVecClass__Delete["SimpleDynVecClass::Delete"]
    SimpleDynVecClass__Grow["SimpleDynVecClass::Grow"]
    SimpleDynVecClass__Shrink["SimpleDynVecClass::Shrink"]
    SimpleFileFactoryClass__Get_File["SimpleFileFactoryClass::Get_File"]
    SimplePersistFactoryClass__Load["SimplePersistFactoryClass::Load"]
    SimpleVecClass__Resize["SimpleVecClass::Resize"]
    Single_Anim_Progress["Single_Anim_Progress"]
    Sort_Vertices["Sort_Vertices"]
    SortedNTreeLeafClass_T___Add_Sorted["SortedNTreeLeafClass<T>::Add_Sorted"]
    SpecialRenderInfoClass_CameraClass____int_["SpecialRenderInfoClass(CameraClass &, int)"]
    SphereRenderObjClass__Render["SphereRenderObjClass::Render"]
    Start_Sample["Start_Sample"]
    Stop["Stop"]
    Stop_Sample["Stop_Sample"]
    Stripify__stripify["Stripify::stripify"]
    strtok_r["strtok_r"]
    subdivision_util["subdivision_util"]
    Submit_Vertex["Submit_Vertex"]
    SuperClassID_From_ClassID["SuperClassID_From_ClassID"]
    TextTextureClass__Build_Texture["TextTextureClass::Build_Texture"]
    TextureFileClass__getMipmapData["TextureFileClass::getMipmapData"]
    TextureFileClass__Process_Reduction["TextureFileClass::Process_Reduction"]
    TextureLoader__Add_Load_Task["TextureLoader::Add_Load_Task"]
    ThumbnailClass__Deinit__["ThumbnailClass::Deinit()"]
    ThumbnailClass__Init__["ThumbnailClass::Init()"]
    To_ASCII["To_ASCII"]
    To_Buffer["To_Buffer"]
    TwiddlerClass__Load["TwiddlerClass::Load"]
    TwiddlerClass__Save["TwiddlerClass::Save"]
    TwiddlerClass__Twiddle["TwiddlerClass::Twiddle"]
    Uninitialised_Grow["Uninitialised_Grow"]
    UniqueArrayClass_T___UniqueArrayClass["UniqueArrayClass<T>::UniqueArrayClass"]
    Unregister_Factory_DefinitionFactoryClass_factory_["Unregister_Factory(DefinitionFactoryClass factory)"]
    Update__["Update()"]
    Update_Arc_List["Update_Arc_List"]
    Update_Arrays["Update_Arrays"]
    Update_Bounding_Boxes_Recursive["Update_Bounding_Boxes_Recursive"]
    Update_Culling["Update_Culling"]
    Update_Sub_Object_Transforms["Update_Sub_Object_Transforms"]
    Validate_Texture["Validate_Texture"]
    Vector4_to_Color["Vector4_to_Color"]
    VectorClass_T___Resize["VectorClass<T>::Resize"]
    VehicleCurveClass__Evaluate["VehicleCurveClass::Evaluate"]
    VehicleCurveClass__Save_Load["VehicleCurveClass::Save/Load"]
    WideStringClass__Convert_From["WideStringClass::Convert_From"]
    Windows_Message_Handler["Windows_Message_Handler"]
    Write["Write"]
    WW3DAssetManager__Find_Prototype["WW3DAssetManager::Find_Prototype"]
    WW3DAssetManager__Get_Font3DData["WW3DAssetManager::Get_Font3DData"]
    WWFontClass__Print["WWFontClass::Print"]
    WWFontClass__String_Pixel_Width["WWFontClass::String_Pixel_Width"]
    WWKeyboardClass__Message_Handler["WWKeyboardClass::Message_Handler"]
    WWMath__Init["WWMath::Init"]
    WWMath__Random_Float["WWMath::Random_Float"]
    WWProfile_Get_Tick_Rate["WWProfile_Get_Tick_Rate"]
    WWProfile_Get_Ticks["WWProfile_Get_Ticks"]
    WWProfileHierachyNodeClass__Call["WWProfileHierachyNodeClass::Call"]
    WWProfileHierachyNodeClass__Return["WWProfileHierachyNodeClass::Return"]
    WWProfileManager__Start_Profile["WWProfileManager::Start_Profile"]
    WWProfileManager__Stop_Profile["WWProfileManager::Stop_Profile"]
    XSurface__Blit_From["XSurface::Blit_From"]
    XSurface__Blit_Plain["XSurface::Blit_Plain"]
    XSurface__Blit_Trans["XSurface::Blit_Trans"]
    XSurface__Draw_Line["XSurface::Draw_Line"]
    XSurface__Fill_Rect["XSurface::Fill_Rect"]
  end

  Cast_Ray --> Cast_Ray_Recursive
  Build_AABTree --> Reset
  Select_Splitting_Plane --> Compute_Plane_Score
  Render --> Single_Anim_Progress
  Render --> Update_Sub_Object_Transforms
  Log_Textures --> WWDEBUG_SAY
  WW3DAssetManager__Find_Prototype --> CRC_Stringi
  Bitmap_Assert_bool_condition_ --> WWASSERT
  BitmapHandlerClass__Create_Mipmap_B8G8R8A8__ --> Combine_A8R8G8B8
  BitmapHandlerClass__Copy_Image_Generate_Mipmap__ --> Combine_A8R8G8B8
  BitmapHandlerClass__Copy_Image_Generate_Mipmap__ --> Read_B8G8R8A8
  BitmapHandlerClass__Copy_Image_Generate_Mipmap__ --> Write_B8G8R8A8
  BitmapHandlerClass__Copy_Image_Generate_Mipmap__ --> Get_Bytes_Per_Pixel
  BitmapHandlerClass__Copy_Image__ --> WWASSERT
  BitmapHandlerClass__Copy_Image__ --> Read_B8G8R8A8
  BitmapHandlerClass__Copy_Image__ --> Write_B8G8R8A8
  BitmapHandlerClass__Copy_Image__ --> Get_Bytes_Per_Pixel
  BitmapHandlerClass__Copy_Image__ --> Combine_A8R8G8B8
  Bitmap2DObjClass_const_char_filename______ --> Find_POT
  Bitmap2DObjClass_const_char_filename______ --> Set_Texture
  Bitmap2DObjClass_const_char_filename______ --> Begin_Tri_Strip
  Bitmap2DObjClass_const_char_filename______ --> Vertex
  Bitmap2DObjClass_const_char_filename______ --> End_Tri_Strip
  Bitmap2DObjClass_TextureClass_texture______ --> Set_Texture
  Bitmap2DObjClass_TextureClass_texture______ --> Begin_Tri_Strip
  Bitmap2DObjClass_TextureClass_texture______ --> Vertex
  Bitmap2DObjClass_TextureClass_texture______ --> End_Tri_Strip
  Bitmap2DObjClass__filename_constructor_ --> DynamicScreenMeshClass
  Bitmap2DObjClass__texture_constructor_ --> DynamicScreenMeshClass
  Bitmap2DObjClass__copy_constructor_ --> DynamicScreenMeshClass
  Render_Triangle_Strip --> Cull
  Render_Triangle_Strip --> Render_Preprocessed_Triangle
  Render_Triangles --> Cull
  Render_Triangles --> Render_Preprocessed_Triangle
  BW_Render__Render_Triangles --> Render_Preprocessed_Triangle
  BW_Render__Render_Triangle_Strip --> Render_Preprocessed_Triangle
  BWRenderClass__Render_Triangles --> Render_Preprocessed_Triangle
  BWRenderClass__Render_Triangle_Strip --> Render_Preprocessed_Triangle
  Get_Pixel --> RGB565_To_ARGB8888
  Get_Pixel --> Combine_Colors
  Get_4x4_Block --> RGB565_To_ARGB8888
  Get_4x4_Block --> Combine_Colors
  DecalSystemClass__Lock_Decal_Generator --> W3DNEW
  MultiFixedPoolDecalSystemClass__Unlock_Decal_Generator --> find_logical_decal
  MultiFixedPoolDecalSystemClass__Clear_Decal_Slot --> find_logical_decal
  DistLODDefClass__Load_W3D --> read_header
  Log --> WWDEBUG_SAY
  Shutdown --> delete
  Remove --> delete
  Font3DDataClass__Load_Font_Image --> Minimize_Font_Image
  Font3DDataClass__Make_Proportional --> Minimize_Font_Image
  Load_W3D --> read_channel
  Load_W3D --> read_bit_channel
  Load_W3D --> add_channel
  Load_W3D --> add_bit_channel
  Load_W3D --> read_header
  HRawAnimClass__Load_W3D --> Free
  HRawAnimClass__Load_W3D --> read_channel
  HRawAnimClass__Load_W3D --> read_bit_channel
  HRawAnimClass__Load_W3D --> add_channel
  HRawAnimClass__Load_W3D --> add_bit_channel
  HRawAnimClass__Get_Orientation --> Fast_Slerp
  HRawAnimClass__Get_Transform --> Fast_Slerp
  HTreeClass__Load_W3D --> Free
  HTreeClass__Combo_Update --> Release_Ref
  HTreeClass__Combo_Update --> Get_Translation
  HTreeClass__Combo_Update --> Fast_Slerp
  HTreeClass__Scale --> Get_Translation
  Intersect_Sphere --> Intersect_Sphere_Quick
  MaterialRemapperClass__Remap_Mesh --> Set_Material
  MaterialRemapperClass__Remap_Mesh --> Set_Texture
  Set_Texture --> REF_PTR_SET
  Set_Material --> REF_PTR_SET
  Get_Texture --> Add_Ref
  Get_Material --> Add_Ref
  Sort_Vertices --> qsort
  Load_W3D --> read_vertices
  Load_W3D --> read_chunks
  Load_W3D --> read_texcoords
  MeshModelClass__Load_W3D --> read_chunks
  MeshModelClass__Load_W3D --> Reset
  MeshModelClass__Load_W3D --> Set_Name
  MeshModelClass__Load_W3D --> read_vertices
  MeshModelClass__Load_W3D --> read_texcoords
  NullLoaderClass__Load_W3D --> W3DNEW
  ParticleBufferClass__ --> Calculate_Cost_Value_Arrays
  Update__ --> Calculate_Cost_Value_Arrays
  Copy_Emitter_Property_Struct --> W3DNEWARRAY
  Copy_Emitter_Property_Struct --> memcpy
  ParticleEmitterDefClass__Load_W3D --> Read_Info
  ParticleEmitterDefClass__Load_W3D --> Read_Props
  ParticleEmitterDefClass__Save_W3D --> Save_Header
  ParticleEmitterDefClass__Save_W3D --> Save_Info
  Load_W3D_Save_W3D --> Read_Info
  Load_W3D_Save_W3D --> Read_Props
  Load_W3D_Save_W3D --> Save_Header
  Load_W3D_Save_W3D --> Save_Info
  PointGroupClass__RenderVolumeParticle --> Render
  PointGroupClass__RenderVolumeParticle --> Update_Arrays
  PointGroupClass___Shutdown --> REF_PTR_RELEASE
  Set_Arrays --> Update_Arrays
  Render --> Update_Arrays
  Set_Shader --> W3DNEW
  _PolygonInfoClass --> delete
  Render2DClass__Add_Quad__ --> Internal_Add_Quad_Indicies
  Render2DClass__Add_Quad__ --> Internal_Add_Quad_Vertices
  Render2DClass__Add_Quad__ --> Internal_Add_Quad_UVs
  Render2DClass__Add_Quad__ --> Internal_Add_Quad_Colors
  Render2DTextClass__Draw_Text__ --> Draw_Char
  Render2DClass__Add_Quad --> Internal_Add_Quad_Vertices
  Render2DClass__Add_Quad --> Internal_Add_Quad_UVs
  Render2DClass__Add_Quad --> Internal_Add_Quad_Colors
  Render2DClass__Add_Quad --> Internal_Add_Quad_Indicies
  Render2DTextClass__Draw_Text --> Draw_Char
  Get_Render_Object --> stricmp
  Get_Render_Object --> Reset_Model
  Reset_Model --> Release_Ref
  Reset_Model --> Set_Animation
  Intersect_IntersectionClass___IntersectionResultClass__ --> Intersect_Sphere_Quick
  Push_Material_Pass --> WWASSERT
  Pop_Material_Pass --> WWASSERT
  Push_Override_Flags --> WWASSERT
  Pop_Override_Flags --> WWASSERT
  SpecialRenderInfoClass_CameraClass____int_ --> RenderInfoClass
  Render --> Render_Seg_Line
  Render --> subdivision_util
  Render --> RenderInfoClass
  Insert_Triangles__overloads_ --> Insert_To_Sorting_Pool
  Insert_VolumeParticle --> Insert_To_Sorting_Pool
  Render --> Render_Streak_Line
  Render_Seg_Line --> StreakRendererClass
  Render_Streak_Line --> StreakRendererClass
  RenderStreak --> subdivision_util
  Save_Texture --> Open_Texture_Handle
  Load_Texture --> Open_Texture_Handle
  Validate_Texture --> Save_Texture
  Load_Texture --> ChunkLoadClass
  Save_Texture --> ChunkSaveClass
  TextureFileClass__getMipmapData --> Fill_Multi_Request_From_Surface
  getMipmapData_MultiRequest__m_ --> Fill_Multi_Request_From_Surface
  ThumbnailClass__Deinit__ --> delete
  Build_Texture --> Is_Texture_Valid
  Build_Texture --> Find_POT
  Build_Texture --> Blit_From
  TextTextureClass__Build_Texture --> Is_Texture_Valid
  Load_W3D__ --> ChunkLoadClass
  Save_W3D__ --> ChunkSaveClass
  Vector4_to_Color --> RGB_to_CIEY
  Color_to_Vector4 --> RGB_to_CIEY
  Set_Transform --> Get_Translation
```

## Subsystem Dependencies

Cross-subsystem call edges. Arrow labels show call counts.

```mermaid
%%{ init: { 'theme': 'dark' } }%%
graph TD

  Generals["Generals (2656 funcs)"]

```

## Statistics

- Total functions documented: 2656
- Total call edges: 658
- Subsystems: 1

