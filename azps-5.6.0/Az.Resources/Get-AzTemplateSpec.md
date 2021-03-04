---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903950"
---
# <span data-ttu-id="dc678-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="dc678-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="dc678-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc678-102">SYNOPSIS</span></span>
<span data-ttu-id="dc678-103">獲取或列出範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="dc678-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc678-104">SYNTAX</span></span>

### <span data-ttu-id="dc678-105">ListTemplateSpecsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc678-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc678-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc678-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc678-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc678-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc678-108">描述</span><span class="sxs-lookup"><span data-stu-id="dc678-108">DESCRIPTION</span></span>
<span data-ttu-id="dc678-109">此 Cmdlet 可用來列出訂閱/資源群組中的範本規格，或按名稱或識別碼取得特定的範本規格。取得特定範本規格時，可透過 **-Version** 參數指定版本名稱，以選擇性地取得特定版本。</span><span class="sxs-lookup"><span data-stu-id="dc678-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="dc678-110">使用 **-Version** 時，\* 中只會顯示特定的版本詳細資料 *。所返回* 的範本規格物件上的版本。</span><span class="sxs-lookup"><span data-stu-id="dc678-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="dc678-111">如果在按名稱/id 來取回範本規格時未指定特定版本，所有版本都會在 \* 內 *顯示。所返回物件的 Versions* 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc678-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="dc678-112">**注意**：當列出訂閱或資源群組內的所有範本規格時，每個會退回的範本規格 *"。Versions"* 屬性為 *Null。*</span><span class="sxs-lookup"><span data-stu-id="dc678-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="dc678-113">版本資訊只有在提供 -Name 或 -ResourceId 參數時 (例如：您要求特定的範本規格/版本) 。</span><span class="sxs-lookup"><span data-stu-id="dc678-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="dc678-114">例子</span><span class="sxs-lookup"><span data-stu-id="dc678-114">EXAMPLES</span></span>

### <span data-ttu-id="dc678-115">範例 1：列出目前訂閱中的範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="dc678-116">列出目前訂閱中所有的範本規格。</span><span class="sxs-lookup"><span data-stu-id="dc678-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="dc678-117">範例 2：資源群組中的清單範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="dc678-118">列出目前訂閱之資源群組 "myRG" 中所有的範本規格。</span><span class="sxs-lookup"><span data-stu-id="dc678-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="dc678-119">範例 3：取得所有 (範本規格) 名稱</span><span class="sxs-lookup"><span data-stu-id="dc678-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="dc678-120">在資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc678-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="dc678-121">**注意**：所有範本規格的版本都會在 "中顯示 *。Return 物件的 Versions*" 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc678-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="dc678-122">範例 4：根據名稱取得 (範本規格) 範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="dc678-123">在資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格版本 "v1.0" 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc678-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="dc678-124">\**注意\*\*\*："。所退回物件的 Versions"* 屬性只會包含要求的特定版本。</span><span class="sxs-lookup"><span data-stu-id="dc678-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="dc678-125">範例 5：使用所有 (資源識別碼取得範本規格) 範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="dc678-126">在訂閱子Id 的資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格 \{ 相關資訊 \} 。</span><span class="sxs-lookup"><span data-stu-id="dc678-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="dc678-127">**注意**：所有範本規格的版本都會在 "中顯示 *。Return 物件的 Versions*" 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc678-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="dc678-128">範例 6：根據資源識別碼 (範本規格) 範本規格</span><span class="sxs-lookup"><span data-stu-id="dc678-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="dc678-129">在訂閱子Id 的資源群組 "myRG" 中，獲得名為 "MyTemplateSpec" 的範本規格版本 "v1.0" \{ 相關資訊 \} 。</span><span class="sxs-lookup"><span data-stu-id="dc678-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="dc678-130">\**注意\*\*\*："。所退回物件的 Versions"* 屬性只會包含要求的特定版本。</span><span class="sxs-lookup"><span data-stu-id="dc678-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="dc678-131">參數</span><span class="sxs-lookup"><span data-stu-id="dc678-131">PARAMETERS</span></span>

### <span data-ttu-id="dc678-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc678-132">-DefaultProfile</span></span>
<span data-ttu-id="dc678-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc678-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc678-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc678-134">-Name</span></span>
<span data-ttu-id="dc678-135">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc678-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc678-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc678-136">-ResourceGroupName</span></span>
<span data-ttu-id="dc678-137">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc678-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc678-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc678-138">-ResourceId</span></span>
<span data-ttu-id="dc678-139">範本規格的完全合格的資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="dc678-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc678-140">-版本</span><span class="sxs-lookup"><span data-stu-id="dc678-140">-Version</span></span>
<span data-ttu-id="dc678-141">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="dc678-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc678-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc678-142">CommonParameters</span></span>
<span data-ttu-id="dc678-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc678-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc678-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc678-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc678-145">輸入</span><span class="sxs-lookup"><span data-stu-id="dc678-145">INPUTS</span></span>

### <span data-ttu-id="dc678-146">System.String</span><span class="sxs-lookup"><span data-stu-id="dc678-146">System.String</span></span>

## <span data-ttu-id="dc678-147">輸出</span><span class="sxs-lookup"><span data-stu-id="dc678-147">OUTPUTS</span></span>

### <span data-ttu-id="dc678-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="dc678-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="dc678-149">筆記</span><span class="sxs-lookup"><span data-stu-id="dc678-149">NOTES</span></span>

## <span data-ttu-id="dc678-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc678-150">RELATED LINKS</span></span>
