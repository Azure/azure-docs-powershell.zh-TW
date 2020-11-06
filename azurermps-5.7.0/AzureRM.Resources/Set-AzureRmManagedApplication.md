---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 870769c6bb2557b2a654b4625d3f2c7ea1b4293e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447664"
---
# <span data-ttu-id="ebbc8-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="ebbc8-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="ebbc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbc8-103">更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="ebbc8-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebbc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebbc8-104">SYNTAX</span></span>

### <span data-ttu-id="ebbc8-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="ebbc8-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbc8-106">SetById</span><span class="sxs-lookup"><span data-stu-id="ebbc8-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebbc8-107">說明</span><span class="sxs-lookup"><span data-stu-id="ebbc8-107">DESCRIPTION</span></span>
<span data-ttu-id="ebbc8-108">**AzureRmManagedApplication** Cmdlet 會更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="ebbc8-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="ebbc8-109">示例</span><span class="sxs-lookup"><span data-stu-id="ebbc8-109">EXAMPLES</span></span>

### <span data-ttu-id="ebbc8-110">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="ebbc8-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="ebbc8-111">這個命令會更新受管理的應用程式描述</span><span class="sxs-lookup"><span data-stu-id="ebbc8-111">This command updates the managed application description</span></span>

## <span data-ttu-id="ebbc8-112">參數</span><span class="sxs-lookup"><span data-stu-id="ebbc8-112">PARAMETERS</span></span>

### <span data-ttu-id="ebbc8-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ebbc8-113">-ApiVersion</span></span>
<span data-ttu-id="ebbc8-114">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ebbc8-115">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbc8-116">-DefaultProfile</span></span>
<span data-ttu-id="ebbc8-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ebbc8-118">-Id</span></span>
<span data-ttu-id="ebbc8-119">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="ebbc8-120">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbc8-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-121">類型</span><span class="sxs-lookup"><span data-stu-id="ebbc8-121">-Kind</span></span>
<span data-ttu-id="ebbc8-122">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-122">The managed application kind.</span></span>
<span data-ttu-id="ebbc8-123">其中一個 marketplace 或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="ebbc8-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ebbc8-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="ebbc8-125">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-125">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbc8-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="ebbc8-127">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-127">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebbc8-128">-Name</span></span>
<span data-ttu-id="ebbc8-129">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-129">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-130">-參數</span><span class="sxs-lookup"><span data-stu-id="ebbc8-130">-Parameter</span></span>
<span data-ttu-id="ebbc8-131">受管理的應用程式之參數的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="ebbc8-132">此路徑可以是包含參數的檔案名或 uri 路徑，或字串形式的參數。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-133">-方案</span><span class="sxs-lookup"><span data-stu-id="ebbc8-133">-Plan</span></span>
<span data-ttu-id="ebbc8-134">代表受管理的應用程式方案屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-135">-預先</span><span class="sxs-lookup"><span data-stu-id="ebbc8-135">-Pre</span></span>
<span data-ttu-id="ebbc8-136">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbc8-137">-ResourceGroupName</span></span>
<span data-ttu-id="ebbc8-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ebbc8-139">-Tag</span></span>
<span data-ttu-id="ebbc8-140">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-140">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-141">-確認</span><span class="sxs-lookup"><span data-stu-id="ebbc8-141">-Confirm</span></span>
<span data-ttu-id="ebbc8-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbc8-143">-WhatIf</span></span>
<span data-ttu-id="ebbc8-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbc8-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbc8-146">CommonParameters</span></span>
<span data-ttu-id="ebbc8-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbc8-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebbc8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbc8-149">輸入</span><span class="sxs-lookup"><span data-stu-id="ebbc8-149">INPUTS</span></span>

### <span data-ttu-id="ebbc8-150">System.object</span><span class="sxs-lookup"><span data-stu-id="ebbc8-150">System.String</span></span>
<span data-ttu-id="ebbc8-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ebbc8-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ebbc8-152">輸出</span><span class="sxs-lookup"><span data-stu-id="ebbc8-152">OUTPUTS</span></span>

### <span data-ttu-id="ebbc8-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="ebbc8-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ebbc8-154">筆記</span><span class="sxs-lookup"><span data-stu-id="ebbc8-154">NOTES</span></span>

## <span data-ttu-id="ebbc8-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebbc8-155">RELATED LINKS</span></span>
