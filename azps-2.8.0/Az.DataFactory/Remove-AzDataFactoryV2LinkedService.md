---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: f84973c29d83e8c7c01c3505d17166275a833460
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612933"
---
# <span data-ttu-id="5f064-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5f064-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="5f064-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f064-102">SYNOPSIS</span></span>
<span data-ttu-id="5f064-103">從資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="5f064-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="5f064-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f064-104">SYNTAX</span></span>

### <span data-ttu-id="5f064-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5f064-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f064-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f064-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f064-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f064-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f064-108">說明</span><span class="sxs-lookup"><span data-stu-id="5f064-108">DESCRIPTION</span></span>
<span data-ttu-id="5f064-109">Remove-AzDataFactoryV2LinkedService Cmdlet 會從 Azure 資料工廠中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="5f064-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="5f064-110">示例</span><span class="sxs-lookup"><span data-stu-id="5f064-110">EXAMPLES</span></span>

### <span data-ttu-id="5f064-111">範例1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="5f064-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="5f064-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="5f064-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="5f064-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="5f064-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="5f064-114">參數</span><span class="sxs-lookup"><span data-stu-id="5f064-114">PARAMETERS</span></span>

### <span data-ttu-id="5f064-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f064-115">-DataFactoryName</span></span>
<span data-ttu-id="5f064-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f064-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5f064-117">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="5f064-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f064-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f064-118">-DefaultProfile</span></span>
<span data-ttu-id="5f064-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f064-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f064-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5f064-120">-Force</span></span>
<span data-ttu-id="5f064-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f064-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5f064-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f064-122">-InputObject</span></span>
<span data-ttu-id="5f064-123">指定要移除的 LinkedService 物件。</span><span class="sxs-lookup"><span data-stu-id="5f064-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f064-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f064-124">-Name</span></span>
<span data-ttu-id="5f064-125">指定要移除之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f064-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="5f064-126">連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f064-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f064-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f064-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f064-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f064-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5f064-129">這個 Cmdlet 會從此參數指定的群組中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="5f064-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f064-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f064-130">-ResourceId</span></span>
<span data-ttu-id="5f064-131">要移除之連結服務的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f064-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f064-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5f064-132">-Confirm</span></span>
<span data-ttu-id="5f064-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f064-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f064-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f064-134">-WhatIf</span></span>
<span data-ttu-id="5f064-135">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f064-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5f064-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f064-136">CommonParameters</span></span>
<span data-ttu-id="5f064-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f064-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f064-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f064-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f064-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5f064-139">INPUTS</span></span>

### <span data-ttu-id="5f064-140">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="5f064-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="5f064-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5f064-141">System.String</span></span>

## <span data-ttu-id="5f064-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5f064-142">OUTPUTS</span></span>

### <span data-ttu-id="5f064-143">System.void</span><span class="sxs-lookup"><span data-stu-id="5f064-143">System.Void</span></span>

## <span data-ttu-id="5f064-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5f064-144">NOTES</span></span>
<span data-ttu-id="5f064-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="5f064-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5f064-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f064-146">RELATED LINKS</span></span>

[<span data-ttu-id="5f064-147">AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5f064-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="5f064-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5f064-148">Set-AzDataFactoryV2LinkedService</span></span>]()

