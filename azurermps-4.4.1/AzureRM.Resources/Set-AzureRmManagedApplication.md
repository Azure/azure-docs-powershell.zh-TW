---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448000"
---
# <span data-ttu-id="719cf-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="719cf-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="719cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="719cf-102">SYNOPSIS</span></span>
<span data-ttu-id="719cf-103">更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="719cf-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="719cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="719cf-104">SYNTAX</span></span>

### <span data-ttu-id="719cf-105">已設定受管理的應用程式名稱參數。</span><span class="sxs-lookup"><span data-stu-id="719cf-105">The managed application name parameter set.</span></span> <span data-ttu-id="719cf-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="719cf-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719cf-107">已設定受管理的應用程式識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="719cf-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719cf-108">說明</span><span class="sxs-lookup"><span data-stu-id="719cf-108">DESCRIPTION</span></span>
<span data-ttu-id="719cf-109">**AzureRmManagedApplication** Cmdlet 會更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="719cf-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="719cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="719cf-110">EXAMPLES</span></span>

### <span data-ttu-id="719cf-111">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="719cf-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="719cf-112">這個命令會更新受管理的應用程式描述</span><span class="sxs-lookup"><span data-stu-id="719cf-112">This command updates the managed application description</span></span>

## <span data-ttu-id="719cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="719cf-113">PARAMETERS</span></span>

### <span data-ttu-id="719cf-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="719cf-114">-ApiVersion</span></span>
<span data-ttu-id="719cf-115">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="719cf-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="719cf-116">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="719cf-116">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719cf-117">-DefaultProfile</span></span>
<span data-ttu-id="719cf-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="719cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-119">類型</span><span class="sxs-lookup"><span data-stu-id="719cf-119">-Kind</span></span>
<span data-ttu-id="719cf-120">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="719cf-120">The managed application kind.</span></span>
<span data-ttu-id="719cf-121">其中一個 marketplace 或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="719cf-121">One of marketplace or servicecatalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="719cf-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="719cf-123">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="719cf-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719cf-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="719cf-125">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="719cf-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="719cf-126">-Name</span></span>
<span data-ttu-id="719cf-127">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="719cf-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-128">-參數</span><span class="sxs-lookup"><span data-stu-id="719cf-128">-Parameter</span></span>
<span data-ttu-id="719cf-129">受管理的應用程式之參數的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="719cf-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="719cf-130">此路徑可以是包含參數的檔案名或 uri 路徑，或字串形式的參數。</span><span class="sxs-lookup"><span data-stu-id="719cf-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-131">-方案</span><span class="sxs-lookup"><span data-stu-id="719cf-131">-Plan</span></span>
<span data-ttu-id="719cf-132">代表受管理的應用程式方案屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="719cf-132">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-133">-預先</span><span class="sxs-lookup"><span data-stu-id="719cf-133">-Pre</span></span>
<span data-ttu-id="719cf-134">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="719cf-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719cf-135">-ResourceGroupName</span></span>
<span data-ttu-id="719cf-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="719cf-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="719cf-137">-Tag</span></span>
<span data-ttu-id="719cf-138">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="719cf-138">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-139">-確認</span><span class="sxs-lookup"><span data-stu-id="719cf-139">-Confirm</span></span>
<span data-ttu-id="719cf-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="719cf-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719cf-141">-WhatIf</span></span>
<span data-ttu-id="719cf-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="719cf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719cf-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="719cf-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-144">-識別碼</span><span class="sxs-lookup"><span data-stu-id="719cf-144">-Id</span></span>
<span data-ttu-id="719cf-145">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="719cf-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="719cf-146">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="719cf-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719cf-147">CommonParameters</span></span>
<span data-ttu-id="719cf-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="719cf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719cf-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="719cf-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719cf-150">輸入</span><span class="sxs-lookup"><span data-stu-id="719cf-150">INPUTS</span></span>

### <span data-ttu-id="719cf-151">System.object</span><span class="sxs-lookup"><span data-stu-id="719cf-151">System.String</span></span>
<span data-ttu-id="719cf-152">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="719cf-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="719cf-153">輸出</span><span class="sxs-lookup"><span data-stu-id="719cf-153">OUTPUTS</span></span>

### <span data-ttu-id="719cf-154">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="719cf-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="719cf-155">筆記</span><span class="sxs-lookup"><span data-stu-id="719cf-155">NOTES</span></span>

## <span data-ttu-id="719cf-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="719cf-156">RELATED LINKS</span></span>

