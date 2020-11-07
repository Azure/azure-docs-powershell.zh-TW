---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 8fb6c2d299799849d1e9f2183621e9fc31cc0acd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800301"
---
# <span data-ttu-id="728ae-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="728ae-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="728ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="728ae-102">SYNOPSIS</span></span>
<span data-ttu-id="728ae-103">更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="728ae-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="728ae-104">SYNTAX</span></span>

### <span data-ttu-id="728ae-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="728ae-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728ae-106">SetById</span><span class="sxs-lookup"><span data-stu-id="728ae-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728ae-107">說明</span><span class="sxs-lookup"><span data-stu-id="728ae-107">DESCRIPTION</span></span>
<span data-ttu-id="728ae-108">**AzureRmManagedApplication** Cmdlet 會更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="728ae-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="728ae-109">示例</span><span class="sxs-lookup"><span data-stu-id="728ae-109">EXAMPLES</span></span>

### <span data-ttu-id="728ae-110">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="728ae-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="728ae-111">這個命令會更新受管理的應用程式描述</span><span class="sxs-lookup"><span data-stu-id="728ae-111">This command updates the managed application description</span></span>

## <span data-ttu-id="728ae-112">參數</span><span class="sxs-lookup"><span data-stu-id="728ae-112">PARAMETERS</span></span>

### <span data-ttu-id="728ae-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="728ae-113">-ApiVersion</span></span>
<span data-ttu-id="728ae-114">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="728ae-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="728ae-115">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="728ae-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="728ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728ae-116">-DefaultProfile</span></span>
<span data-ttu-id="728ae-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="728ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728ae-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="728ae-118">-Id</span></span>
<span data-ttu-id="728ae-119">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="728ae-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="728ae-120">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ae-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="728ae-121">類型</span><span class="sxs-lookup"><span data-stu-id="728ae-121">-Kind</span></span>
<span data-ttu-id="728ae-122">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="728ae-122">The managed application kind.</span></span>
<span data-ttu-id="728ae-123">其中一個 marketplace 或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="728ae-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="728ae-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="728ae-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="728ae-125">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="728ae-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="728ae-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ae-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="728ae-127">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="728ae-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="728ae-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="728ae-128">-Name</span></span>
<span data-ttu-id="728ae-129">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="728ae-129">The managed application name.</span></span>

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

### <span data-ttu-id="728ae-130">-參數</span><span class="sxs-lookup"><span data-stu-id="728ae-130">-Parameter</span></span>
<span data-ttu-id="728ae-131">受管理的應用程式之參數的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="728ae-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="728ae-132">此路徑可以是包含參數的檔案名或 uri 路徑，或字串形式的參數。</span><span class="sxs-lookup"><span data-stu-id="728ae-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="728ae-133">-方案</span><span class="sxs-lookup"><span data-stu-id="728ae-133">-Plan</span></span>
<span data-ttu-id="728ae-134">代表受管理的應用程式方案屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="728ae-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="728ae-135">-預先</span><span class="sxs-lookup"><span data-stu-id="728ae-135">-Pre</span></span>
<span data-ttu-id="728ae-136">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="728ae-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="728ae-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ae-137">-ResourceGroupName</span></span>
<span data-ttu-id="728ae-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="728ae-138">The resource group name.</span></span>

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

### <span data-ttu-id="728ae-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="728ae-139">-Tag</span></span>
<span data-ttu-id="728ae-140">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="728ae-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="728ae-141">-確認</span><span class="sxs-lookup"><span data-stu-id="728ae-141">-Confirm</span></span>
<span data-ttu-id="728ae-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="728ae-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728ae-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728ae-143">-WhatIf</span></span>
<span data-ttu-id="728ae-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="728ae-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728ae-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="728ae-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728ae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728ae-146">CommonParameters</span></span>
<span data-ttu-id="728ae-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="728ae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728ae-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="728ae-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728ae-149">輸入</span><span class="sxs-lookup"><span data-stu-id="728ae-149">INPUTS</span></span>

### <span data-ttu-id="728ae-150">System.object</span><span class="sxs-lookup"><span data-stu-id="728ae-150">System.String</span></span>
<span data-ttu-id="728ae-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="728ae-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="728ae-152">輸出</span><span class="sxs-lookup"><span data-stu-id="728ae-152">OUTPUTS</span></span>

### <span data-ttu-id="728ae-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="728ae-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="728ae-154">筆記</span><span class="sxs-lookup"><span data-stu-id="728ae-154">NOTES</span></span>

## <span data-ttu-id="728ae-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="728ae-155">RELATED LINKS</span></span>
