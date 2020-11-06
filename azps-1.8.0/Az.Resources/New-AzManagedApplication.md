---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 8286bdd365f43881f09787dfb051e873d2fdeb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620839"
---
# <span data-ttu-id="ac56e-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="ac56e-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="ac56e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac56e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac56e-103">建立 Azure 管理的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac56e-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="ac56e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac56e-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac56e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac56e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac56e-106">**新的-AzManagedApplication** Cmdlet 會建立 Azure 管理的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac56e-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="ac56e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac56e-107">EXAMPLES</span></span>

### <span data-ttu-id="ac56e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ac56e-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="ac56e-109">這個命令會建立受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="ac56e-109">This command creates a managed application</span></span>

## <span data-ttu-id="ac56e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac56e-110">PARAMETERS</span></span>

### <span data-ttu-id="ac56e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ac56e-111">-ApiVersion</span></span>
<span data-ttu-id="ac56e-112">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ac56e-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ac56e-113">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="ac56e-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ac56e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac56e-114">-DefaultProfile</span></span>
<span data-ttu-id="ac56e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac56e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac56e-116">類型</span><span class="sxs-lookup"><span data-stu-id="ac56e-116">-Kind</span></span>
<span data-ttu-id="ac56e-117">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="ac56e-117">The managed application kind.</span></span>
<span data-ttu-id="ac56e-118">其中一個 marketplace 或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="ac56e-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-119">-位置</span><span class="sxs-lookup"><span data-stu-id="ac56e-119">-Location</span></span>
<span data-ttu-id="ac56e-120">資源位置。</span><span class="sxs-lookup"><span data-stu-id="ac56e-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ac56e-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="ac56e-122">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ac56e-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="ac56e-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac56e-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="ac56e-124">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ac56e-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac56e-125">-Name</span></span>
<span data-ttu-id="ac56e-126">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ac56e-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-127">-參數</span><span class="sxs-lookup"><span data-stu-id="ac56e-127">-Parameter</span></span>
<span data-ttu-id="ac56e-128">受管理的應用程式之參數的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="ac56e-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="ac56e-129">此路徑可以是包含參數的檔案名或 uri 路徑，或字串形式的參數。</span><span class="sxs-lookup"><span data-stu-id="ac56e-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="ac56e-130">-方案</span><span class="sxs-lookup"><span data-stu-id="ac56e-130">-Plan</span></span>
<span data-ttu-id="ac56e-131">代表受管理的應用程式方案屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ac56e-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="ac56e-132">-預先</span><span class="sxs-lookup"><span data-stu-id="ac56e-132">-Pre</span></span>
<span data-ttu-id="ac56e-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="ac56e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ac56e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac56e-134">-ResourceGroupName</span></span>
<span data-ttu-id="ac56e-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac56e-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac56e-136">-Tag</span></span>
<span data-ttu-id="ac56e-137">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ac56e-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ac56e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ac56e-138">-Confirm</span></span>
<span data-ttu-id="ac56e-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac56e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac56e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac56e-140">-WhatIf</span></span>
<span data-ttu-id="ac56e-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac56e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac56e-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac56e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac56e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac56e-143">CommonParameters</span></span>
<span data-ttu-id="ac56e-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac56e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac56e-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac56e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac56e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ac56e-146">INPUTS</span></span>

### <span data-ttu-id="ac56e-147">System.object</span><span class="sxs-lookup"><span data-stu-id="ac56e-147">System.String</span></span>

### <span data-ttu-id="ac56e-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ac56e-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ac56e-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ac56e-149">OUTPUTS</span></span>

### <span data-ttu-id="ac56e-150">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="ac56e-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ac56e-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ac56e-151">NOTES</span></span>

## <span data-ttu-id="ac56e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac56e-152">RELATED LINKS</span></span>
