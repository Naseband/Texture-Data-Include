# Texture Data Include

Contains data about object textures, namely material counts and all textures used by each model.
Since the ObjectTextures array is huge and makes the compiler slow (even if it is unused),
you must define OTD_INCLUDE_ALL_TEXTURES if you want to use it.

Data gathered and compiled using Dk22Pac's GTA SA Plugin SDK.

Functions:

``GetModelTextureCount(model)``

  Returns the amount of materials of an object model.
  Returns TEXTURE_DATA_INVALID_MODEL if the model is invalid.
  Returns TEXTURE_DATA_INVALID_TEXTURE if the model has no textures.

``GetModelTextureData(model, index, name[], mask[], size_name = sizeof(name), size_mask = sizeof(mask))``

  Gets texture name and alpha mask for a model and material index.
  Returns texture data index if found.
  Returns -1 if no data was found.

``FindModelsWithTexture(const search[], bool:ignorecase, model_array[], eOTDSearchMode:search_mode = OTD_SEARCH_FIND, size = sizeof(model_array))``

  Gets all models with any texture names matching the search string. The search modes are:
  - OTD_SEARCH_EXACT
  - OTD_SEARCH_FIND
  - OTD_SEARCH_START
  - OTD_SEARCH_END
  
  Returns the amount of found models.
  
``FindTextureIndexesForModel(model, const search[], bool:ignorecase, index_array[], eOTDSearchMode:search_mode = OTD_SEARCH_FIND, size = sizeof(index_array))``

  Gets all texture indexes for a model whose names match the search strings. For seach modes see above.
  
  Returns the amount of found indexes.
