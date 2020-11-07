---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798849"
---
# <span data-ttu-id="b215d-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b215d-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="b215d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b215d-102">SYNOPSIS</span></span>
<span data-ttu-id="b215d-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b215d-103">Removes a data factory.</span></span>

## <span data-ttu-id="b215d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b215d-104">SYNTAX</span></span>

### <span data-ttu-id="b215d-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b215d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b215d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b215d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b215d-107">說明</span><span class="sxs-lookup"><span data-stu-id="b215d-107">DESCRIPTION</span></span>
<span data-ttu-id="b215d-108">**AzDataFactory** Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b215d-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="b215d-109">示例</span><span class="sxs-lookup"><span data-stu-id="b215d-109">EXAMPLES</span></span>

### <span data-ttu-id="b215d-110">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="b215d-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b215d-111">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b215d-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="b215d-112">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="b215d-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="b215d-113">參數</span><span class="sxs-lookup"><span data-stu-id="b215d-113">PARAMETERS</span></span>

### <span data-ttu-id="b215d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b215d-114">-DataFactory</span></span>
<span data-ttu-id="b215d-115">指定要移除的 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="b215d-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b215d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b215d-116">-DefaultProfile</span></span>
<span data-ttu-id="b215d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b215d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b215d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b215d-118">-Force</span></span>
<span data-ttu-id="b215d-119">表示此 Cmdlet 會移除資料工廠，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b215d-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b215d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b215d-120">-Name</span></span>
<span data-ttu-id="b215d-121">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b215d-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b215d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b215d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b215d-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b215d-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b215d-124">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b215d-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b215d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b215d-125">-Confirm</span></span>
<span data-ttu-id="b215d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b215d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b215d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b215d-127">-WhatIf</span></span>
<span data-ttu-id="b215d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b215d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b215d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b215d-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b215d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b215d-130">CommonParameters</span></span>
<span data-ttu-id="b215d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b215d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b215d-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b215d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b215d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b215d-133">INPUTS</span></span>

### <span data-ttu-id="b215d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b215d-134">System.String</span></span>

### <span data-ttu-id="b215d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b215d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b215d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b215d-136">OUTPUTS</span></span>

### <span data-ttu-id="b215d-137">System.void</span><span class="sxs-lookup"><span data-stu-id="b215d-137">System.Void</span></span>

## <span data-ttu-id="b215d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b215d-138">NOTES</span></span>
* <span data-ttu-id="b215d-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b215d-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b215d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b215d-140">RELATED LINKS</span></span>

[<span data-ttu-id="b215d-141">AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b215d-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="b215d-142">新-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b215d-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


