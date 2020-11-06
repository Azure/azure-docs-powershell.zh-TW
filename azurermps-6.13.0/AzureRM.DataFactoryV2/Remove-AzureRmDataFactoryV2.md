---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: a4446fb64ed8d279e24b3cf3d6c82701b48ab754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443912"
---
# <span data-ttu-id="be47c-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="be47c-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="be47c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be47c-102">SYNOPSIS</span></span>
<span data-ttu-id="be47c-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="be47c-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be47c-104">句法</span><span class="sxs-lookup"><span data-stu-id="be47c-104">SYNTAX</span></span>

### <span data-ttu-id="be47c-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="be47c-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be47c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be47c-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be47c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be47c-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be47c-108">說明</span><span class="sxs-lookup"><span data-stu-id="be47c-108">DESCRIPTION</span></span>
<span data-ttu-id="be47c-109">Remove-AzureRmDataFactoryV2 Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="be47c-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="be47c-110">示例</span><span class="sxs-lookup"><span data-stu-id="be47c-110">EXAMPLES</span></span>

### <span data-ttu-id="be47c-111">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="be47c-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="be47c-112">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="be47c-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="be47c-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="be47c-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="be47c-114">參數</span><span class="sxs-lookup"><span data-stu-id="be47c-114">PARAMETERS</span></span>

### <span data-ttu-id="be47c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be47c-115">-DefaultProfile</span></span>
<span data-ttu-id="be47c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be47c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be47c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="be47c-117">-Force</span></span>
<span data-ttu-id="be47c-118">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be47c-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="be47c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be47c-119">-InputObject</span></span>
<span data-ttu-id="be47c-120">指定要移除的 DataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="be47c-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be47c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="be47c-121">-Name</span></span>
<span data-ttu-id="be47c-122">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="be47c-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be47c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be47c-123">-ResourceGroupName</span></span>
<span data-ttu-id="be47c-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be47c-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="be47c-125">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="be47c-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be47c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be47c-126">-ResourceId</span></span>
<span data-ttu-id="be47c-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="be47c-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="be47c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="be47c-128">-Confirm</span></span>
<span data-ttu-id="be47c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be47c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be47c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be47c-130">-WhatIf</span></span>
<span data-ttu-id="be47c-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be47c-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="be47c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be47c-132">CommonParameters</span></span>
<span data-ttu-id="be47c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be47c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be47c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be47c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be47c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="be47c-135">INPUTS</span></span>

### <span data-ttu-id="be47c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="be47c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="be47c-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="be47c-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="be47c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="be47c-138">System.String</span></span>

## <span data-ttu-id="be47c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="be47c-139">OUTPUTS</span></span>

### <span data-ttu-id="be47c-140">System.void</span><span class="sxs-lookup"><span data-stu-id="be47c-140">System.Void</span></span>

## <span data-ttu-id="be47c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="be47c-141">NOTES</span></span>
<span data-ttu-id="be47c-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="be47c-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="be47c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="be47c-143">RELATED LINKS</span></span>

[<span data-ttu-id="be47c-144">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="be47c-144">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="be47c-145">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="be47c-145">Set-AzureRmDataFactoryV2</span></span>]()
