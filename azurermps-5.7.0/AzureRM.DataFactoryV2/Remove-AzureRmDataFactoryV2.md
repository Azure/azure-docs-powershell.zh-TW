---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444603"
---
# <span data-ttu-id="bcf20-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bcf20-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="bcf20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcf20-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf20-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="bcf20-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf20-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcf20-104">SYNTAX</span></span>

### <span data-ttu-id="bcf20-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="bcf20-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf20-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bcf20-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf20-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf20-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf20-108">說明</span><span class="sxs-lookup"><span data-stu-id="bcf20-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf20-109">Remove-AzureRmDataFactoryV2 Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="bcf20-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="bcf20-110">示例</span><span class="sxs-lookup"><span data-stu-id="bcf20-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf20-111">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="bcf20-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="bcf20-112">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="bcf20-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="bcf20-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="bcf20-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="bcf20-114">參數</span><span class="sxs-lookup"><span data-stu-id="bcf20-114">PARAMETERS</span></span>

### <span data-ttu-id="bcf20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf20-115">-DefaultProfile</span></span>
<span data-ttu-id="bcf20-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcf20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf20-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bcf20-117">-Force</span></span>
<span data-ttu-id="bcf20-118">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcf20-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="bcf20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcf20-119">-InputObject</span></span>
<span data-ttu-id="bcf20-120">指定要移除的 DataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="bcf20-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf20-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcf20-121">-Name</span></span>
<span data-ttu-id="bcf20-122">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf20-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf20-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcf20-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf20-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bcf20-125">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="bcf20-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf20-126">-ResourceId</span></span>
<span data-ttu-id="bcf20-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcf20-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf20-128">-確認</span><span class="sxs-lookup"><span data-stu-id="bcf20-128">-Confirm</span></span>
<span data-ttu-id="bcf20-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcf20-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf20-130">-WhatIf</span></span>
<span data-ttu-id="bcf20-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcf20-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="bcf20-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf20-132">CommonParameters</span></span>
<span data-ttu-id="bcf20-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcf20-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf20-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcf20-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf20-135">輸入</span><span class="sxs-lookup"><span data-stu-id="bcf20-135">INPUTS</span></span>

### <span data-ttu-id="bcf20-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bcf20-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="bcf20-137">System.object</span><span class="sxs-lookup"><span data-stu-id="bcf20-137">System.String</span></span>

## <span data-ttu-id="bcf20-138">輸出</span><span class="sxs-lookup"><span data-stu-id="bcf20-138">OUTPUTS</span></span>

### <span data-ttu-id="bcf20-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bcf20-139">System.Object</span></span>

## <span data-ttu-id="bcf20-140">筆記</span><span class="sxs-lookup"><span data-stu-id="bcf20-140">NOTES</span></span>
<span data-ttu-id="bcf20-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="bcf20-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bcf20-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcf20-142">RELATED LINKS</span></span>

[<span data-ttu-id="bcf20-143">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bcf20-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="bcf20-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bcf20-144">Set-AzureRmDataFactoryV2</span></span>]()
