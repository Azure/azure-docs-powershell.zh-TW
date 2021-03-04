---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 3026f8774e08b3a5dd51b4ea905a5cb68dfd714a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903274"
---
# <span data-ttu-id="a6ef7-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6ef7-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="a6ef7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ef7-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-103">Removes a data factory.</span></span>

## <span data-ttu-id="a6ef7-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6ef7-104">SYNTAX</span></span>

### <span data-ttu-id="a6ef7-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a6ef7-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ef7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a6ef7-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ef7-107">描述</span><span class="sxs-lookup"><span data-stu-id="a6ef7-107">DESCRIPTION</span></span>
<span data-ttu-id="a6ef7-108">**Remove-AzDataFactory** Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="a6ef7-109">例子</span><span class="sxs-lookup"><span data-stu-id="a6ef7-109">EXAMPLES</span></span>

### <span data-ttu-id="a6ef7-110">範例 1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="a6ef7-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a6ef7-111">此命令會從名為 ADF 的資源群組移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="a6ef7-112">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="a6ef7-113">參數</span><span class="sxs-lookup"><span data-stu-id="a6ef7-113">PARAMETERS</span></span>

### <span data-ttu-id="a6ef7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6ef7-114">-DataFactory</span></span>
<span data-ttu-id="a6ef7-115">指定 **要移除的 PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="a6ef7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ef7-116">-DefaultProfile</span></span>
<span data-ttu-id="a6ef7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a6ef7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6ef7-118">-強制</span><span class="sxs-lookup"><span data-stu-id="a6ef7-118">-Force</span></span>
<span data-ttu-id="a6ef7-119">表示此 Cmdlet 會移除資料工廠，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a6ef7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6ef7-120">-Name</span></span>
<span data-ttu-id="a6ef7-121">指定要移除的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-121">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="a6ef7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ef7-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6ef7-123">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a6ef7-124">此 Cmdlet 會從此參數指定的群組移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6ef7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a6ef7-125">-Confirm</span></span>
<span data-ttu-id="a6ef7-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ef7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ef7-127">-WhatIf</span></span>
<span data-ttu-id="a6ef7-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ef7-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ef7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ef7-130">CommonParameters</span></span>
<span data-ttu-id="a6ef7-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ef7-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a6ef7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ef7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a6ef7-133">INPUTS</span></span>

### <span data-ttu-id="a6ef7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a6ef7-134">System.String</span></span>

### <span data-ttu-id="a6ef7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6ef7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a6ef7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a6ef7-136">OUTPUTS</span></span>

### <span data-ttu-id="a6ef7-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="a6ef7-137">System.Void</span></span>

## <span data-ttu-id="a6ef7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a6ef7-138">NOTES</span></span>
* <span data-ttu-id="a6ef7-139">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="a6ef7-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a6ef7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6ef7-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6ef7-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6ef7-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="a6ef7-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6ef7-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


