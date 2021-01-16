---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282947"
---
# <span data-ttu-id="7bf7a-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="7bf7a-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="7bf7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bf7a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf7a-103">取得或列出範本規格</span><span class="sxs-lookup"><span data-stu-id="7bf7a-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="7bf7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bf7a-104">SYNTAX</span></span>

### <span data-ttu-id="7bf7a-105">ListTemplateSpecsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7bf7a-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bf7a-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bf7a-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bf7a-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bf7a-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bf7a-108">說明</span><span class="sxs-lookup"><span data-stu-id="7bf7a-108">DESCRIPTION</span></span>
<span data-ttu-id="7bf7a-109">這個 Cmdlet 可用來列出訂閱/資源群組中的範本規格，或取得特定的範本規格（依名稱或 id）。以名稱/id 取得特定的範本規格時，可以選擇透過 **版本** 參數指定版本名稱來檢索特定版本。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="7bf7a-110">使用 **-版本** 時，只會在 \* 中顯示特定版本的詳細資料 *。* 傳回的範本規格物件上的版本。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="7bf7a-111">如果您在以名稱/識別碼來檢索範本規格時沒有指定特定的版本，所有版本都將出現在 \* 中 *。* 傳回物件的版本屬性。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="7bf7a-112">**注意**：列出訂閱或資源群組中的所有範本規格時，每個傳回的範本規格是 *"。[版本]* 屬性將會是 *null*。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="7bf7a-113">版本資訊只會包含在下列情況中提供的-名稱或-ResourceId 參數 (：您要求特定的範本規格/版本) 。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="7bf7a-114">示例</span><span class="sxs-lookup"><span data-stu-id="7bf7a-114">EXAMPLES</span></span>

### <span data-ttu-id="7bf7a-115">範例1：清單範本規格在目前的訂閱中</span><span class="sxs-lookup"><span data-stu-id="7bf7a-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="7bf7a-116">列出目前訂閱中的所有範本規格。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="7bf7a-117">範例2： [資源] 群組中的 [清單範本規格]</span><span class="sxs-lookup"><span data-stu-id="7bf7a-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="7bf7a-118">列出目前訂閱之資源群組 ' myRG」中的所有範本規格。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="7bf7a-119">範例3：取得範本規格 (，並以名稱) 所有版本</span><span class="sxs-lookup"><span data-stu-id="7bf7a-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="7bf7a-120">取得資源群組 "myRG" 中名為「MyTemplateSpec」的範本規範的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="7bf7a-121">**注意**：所有範本規格的版本都會出現在「中 *。* 返回物件的版本屬性。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="7bf7a-122">範例4：取得範本規格 (依名稱) 特定版本</span><span class="sxs-lookup"><span data-stu-id="7bf7a-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="7bf7a-123">取得資源群組 "myRG" 中名為「MyTemplateSpec」的範本規格版本 ' v 1.0」的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="7bf7a-124">**注意**：」 *。* 所傳回物件的版本屬性將只包含所要求的特定版本。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="7bf7a-125">範例5：取得範本規格 (，並以資源識別碼) 所有版本</span><span class="sxs-lookup"><span data-stu-id="7bf7a-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="7bf7a-126">取得訂閱 subId 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格資訊 \{ \} 。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="7bf7a-127">**注意**：所有範本規格的版本都會出現在「中 *。* 返回物件的版本屬性。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="7bf7a-128">範例6：取得範本規格 (由資源識別碼) 特定版本</span><span class="sxs-lookup"><span data-stu-id="7bf7a-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="7bf7a-129">取得訂閱 subId 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格的版本 "v 1.0" 的相關資訊 \{ \} 。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="7bf7a-130">**注意**：」 *。* 所傳回物件的版本屬性將只包含所要求的特定版本。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="7bf7a-131">參數</span><span class="sxs-lookup"><span data-stu-id="7bf7a-131">PARAMETERS</span></span>

### <span data-ttu-id="7bf7a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf7a-132">-DefaultProfile</span></span>
<span data-ttu-id="7bf7a-133">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bf7a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bf7a-134">-Name</span></span>
<span data-ttu-id="7bf7a-135">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="7bf7a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bf7a-136">-ResourceGroupName</span></span>
<span data-ttu-id="7bf7a-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="7bf7a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bf7a-138">-ResourceId</span></span>
<span data-ttu-id="7bf7a-139">範本規格的完全限定資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="7bf7a-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="7bf7a-140">-版本</span><span class="sxs-lookup"><span data-stu-id="7bf7a-140">-Version</span></span>
<span data-ttu-id="7bf7a-141">範本規格的版本。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="7bf7a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf7a-142">CommonParameters</span></span>
<span data-ttu-id="7bf7a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf7a-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bf7a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf7a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="7bf7a-145">INPUTS</span></span>

### <span data-ttu-id="7bf7a-146">System.object</span><span class="sxs-lookup"><span data-stu-id="7bf7a-146">System.String</span></span>

## <span data-ttu-id="7bf7a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="7bf7a-147">OUTPUTS</span></span>

### <span data-ttu-id="7bf7a-148">PSTemplateSpec 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="7bf7a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="7bf7a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="7bf7a-149">NOTES</span></span>

## <span data-ttu-id="7bf7a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bf7a-150">RELATED LINKS</span></span>
