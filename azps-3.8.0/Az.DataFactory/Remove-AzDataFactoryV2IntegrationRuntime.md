---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798841"
---
# <span data-ttu-id="46557-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="46557-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="46557-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46557-102">SYNOPSIS</span></span>
<span data-ttu-id="46557-103">移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46557-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="46557-104">句法</span><span class="sxs-lookup"><span data-stu-id="46557-104">SYNTAX</span></span>

### <span data-ttu-id="46557-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="46557-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46557-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46557-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46557-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="46557-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46557-108">說明</span><span class="sxs-lookup"><span data-stu-id="46557-108">DESCRIPTION</span></span>
<span data-ttu-id="46557-109">Remove-AzDataFactoryV2IntegrationRuntime Cmdlet 會移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46557-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="46557-110">示例</span><span class="sxs-lookup"><span data-stu-id="46557-110">EXAMPLES</span></span>

### <span data-ttu-id="46557-111">範例1：移除整合執行時間</span><span class="sxs-lookup"><span data-stu-id="46557-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="46557-112">這個命令會從名為「test-df」的資料工廠中，移除名為「test reserved-ir」的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46557-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="46557-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="46557-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="46557-114">參數</span><span class="sxs-lookup"><span data-stu-id="46557-114">PARAMETERS</span></span>

### <span data-ttu-id="46557-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="46557-115">-DataFactoryName</span></span>
<span data-ttu-id="46557-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="46557-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46557-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46557-117">-DefaultProfile</span></span>
<span data-ttu-id="46557-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46557-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46557-119">-Force</span><span class="sxs-lookup"><span data-stu-id="46557-119">-Force</span></span>
<span data-ttu-id="46557-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46557-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="46557-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46557-121">-InputObject</span></span>
<span data-ttu-id="46557-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="46557-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46557-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="46557-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="46557-124">連結的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="46557-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="46557-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="46557-125">-Name</span></span>
<span data-ttu-id="46557-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="46557-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46557-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46557-127">-ResourceGroupName</span></span>
<span data-ttu-id="46557-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46557-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46557-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46557-129">-ResourceId</span></span>
<span data-ttu-id="46557-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46557-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46557-131">-確認</span><span class="sxs-lookup"><span data-stu-id="46557-131">-Confirm</span></span>
<span data-ttu-id="46557-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46557-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46557-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46557-133">-WhatIf</span></span>
<span data-ttu-id="46557-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46557-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="46557-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46557-135">CommonParameters</span></span>
<span data-ttu-id="46557-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46557-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46557-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46557-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46557-138">輸入</span><span class="sxs-lookup"><span data-stu-id="46557-138">INPUTS</span></span>

### <span data-ttu-id="46557-139">System.object</span><span class="sxs-lookup"><span data-stu-id="46557-139">System.String</span></span>

### <span data-ttu-id="46557-140">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="46557-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="46557-141">輸出</span><span class="sxs-lookup"><span data-stu-id="46557-141">OUTPUTS</span></span>

### <span data-ttu-id="46557-142">System.void</span><span class="sxs-lookup"><span data-stu-id="46557-142">System.Void</span></span>

## <span data-ttu-id="46557-143">筆記</span><span class="sxs-lookup"><span data-stu-id="46557-143">NOTES</span></span>
<span data-ttu-id="46557-144">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="46557-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="46557-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="46557-145">RELATED LINKS</span></span>

[<span data-ttu-id="46557-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="46557-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="46557-147">AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="46557-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

