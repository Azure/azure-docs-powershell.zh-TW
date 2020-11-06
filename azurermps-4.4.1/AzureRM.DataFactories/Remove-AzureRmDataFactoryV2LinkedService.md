---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450792"
---
# <span data-ttu-id="971e8-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="971e8-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="971e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="971e8-102">SYNOPSIS</span></span>
<span data-ttu-id="971e8-103">從資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="971e8-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="971e8-104">SYNTAX</span></span>

### <span data-ttu-id="971e8-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="971e8-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="971e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="971e8-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971e8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="971e8-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971e8-108">說明</span><span class="sxs-lookup"><span data-stu-id="971e8-108">DESCRIPTION</span></span>
<span data-ttu-id="971e8-109">Remove-AzureRmDataFactoryV2LinkedService Cmdlet 會從 Azure 資料工廠中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="971e8-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="971e8-110">示例</span><span class="sxs-lookup"><span data-stu-id="971e8-110">EXAMPLES</span></span>

### <span data-ttu-id="971e8-111">範例1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="971e8-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="971e8-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="971e8-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="971e8-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="971e8-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="971e8-114">參數</span><span class="sxs-lookup"><span data-stu-id="971e8-114">PARAMETERS</span></span>

### <span data-ttu-id="971e8-115">-確認</span><span class="sxs-lookup"><span data-stu-id="971e8-115">-Confirm</span></span>
<span data-ttu-id="971e8-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="971e8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971e8-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="971e8-117">-DataFactoryName</span></span>
<span data-ttu-id="971e8-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="971e8-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="971e8-119">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="971e8-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="971e8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="971e8-120">-Force</span></span>
<span data-ttu-id="971e8-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="971e8-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="971e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="971e8-122">-InputObject</span></span>
<span data-ttu-id="971e8-123">指定要移除的 LinkedService 物件。</span><span class="sxs-lookup"><span data-stu-id="971e8-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="971e8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="971e8-124">-Name</span></span>
<span data-ttu-id="971e8-125">指定要移除之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="971e8-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="971e8-126">連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="971e8-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="971e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="971e8-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="971e8-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="971e8-129">這個 Cmdlet 會從此參數指定的群組中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="971e8-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="971e8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="971e8-130">-ResourceId</span></span>
<span data-ttu-id="971e8-131">要移除之連結服務的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="971e8-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="971e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971e8-132">-WhatIf</span></span>
<span data-ttu-id="971e8-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="971e8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="971e8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971e8-134">-DefaultProfile</span></span>
<span data-ttu-id="971e8-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="971e8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971e8-136">CommonParameters</span></span>
<span data-ttu-id="971e8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="971e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971e8-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="971e8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971e8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="971e8-139">INPUTS</span></span>

### <span data-ttu-id="971e8-140">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="971e8-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="971e8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="971e8-141">System.String</span></span>

## <span data-ttu-id="971e8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="971e8-142">OUTPUTS</span></span>

### <span data-ttu-id="971e8-143">System.object</span><span class="sxs-lookup"><span data-stu-id="971e8-143">System.Object</span></span>

## <span data-ttu-id="971e8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="971e8-144">NOTES</span></span>
<span data-ttu-id="971e8-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="971e8-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="971e8-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="971e8-146">RELATED LINKS</span></span>

[<span data-ttu-id="971e8-147">AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="971e8-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="971e8-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="971e8-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

