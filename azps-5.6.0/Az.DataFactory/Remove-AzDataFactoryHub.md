---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 8144d1989f6bec9c1342613cf4776a6dae0a9c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906937"
---
# <span data-ttu-id="77929-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="77929-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="77929-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77929-102">SYNOPSIS</span></span>
<span data-ttu-id="77929-103">從 Azure Data Factory 移除中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="77929-104">語法</span><span class="sxs-lookup"><span data-stu-id="77929-104">SYNTAX</span></span>

### <span data-ttu-id="77929-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="77929-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77929-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="77929-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77929-107">描述</span><span class="sxs-lookup"><span data-stu-id="77929-107">DESCRIPTION</span></span>
<span data-ttu-id="77929-108">**Remove-AzDataFactoryHub** Cmdlet 會從指定的 Azure 資源群組和指定資料工廠中的 Azure Data Factory 移除中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="77929-109">如果您移除中樞，也會移除中樞中所有連結的服務和管線。</span><span class="sxs-lookup"><span data-stu-id="77929-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="77929-110">例子</span><span class="sxs-lookup"><span data-stu-id="77929-110">EXAMPLES</span></span>

### <span data-ttu-id="77929-111">範例 1：移除中樞</span><span class="sxs-lookup"><span data-stu-id="77929-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="77929-112">此命令會從名為 ADFResourceGroup 的 Azure 資源群組和名為 ADFDataFactory 的資料工廠移除名為 ContosoDataHub 的中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="77929-113">參數</span><span class="sxs-lookup"><span data-stu-id="77929-113">PARAMETERS</span></span>

### <span data-ttu-id="77929-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="77929-114">-DataFactory</span></span>
<span data-ttu-id="77929-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="77929-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="77929-116">此 Cmdlet 會從此參數指定的資料工廠移除中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="77929-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="77929-117">-DataFactoryName</span></span>
<span data-ttu-id="77929-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="77929-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="77929-119">此 Cmdlet 會從此參數指定的資料工廠移除中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="77929-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77929-120">-DefaultProfile</span></span>
<span data-ttu-id="77929-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="77929-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77929-122">-強制</span><span class="sxs-lookup"><span data-stu-id="77929-122">-Force</span></span>
<span data-ttu-id="77929-123">表示此 Cmdlet 會移除中樞，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="77929-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="77929-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="77929-124">-Name</span></span>
<span data-ttu-id="77929-125">指定要移除的中樞名稱。</span><span class="sxs-lookup"><span data-stu-id="77929-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77929-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77929-126">-ResourceGroupName</span></span>
<span data-ttu-id="77929-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77929-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="77929-128">此 Cmdlet 會從此參數指定的群組移除中樞。</span><span class="sxs-lookup"><span data-stu-id="77929-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="77929-129">-確認</span><span class="sxs-lookup"><span data-stu-id="77929-129">-Confirm</span></span>
<span data-ttu-id="77929-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="77929-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77929-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77929-131">-WhatIf</span></span>
<span data-ttu-id="77929-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77929-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77929-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77929-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77929-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77929-134">CommonParameters</span></span>
<span data-ttu-id="77929-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77929-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77929-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="77929-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77929-137">輸入</span><span class="sxs-lookup"><span data-stu-id="77929-137">INPUTS</span></span>

### <span data-ttu-id="77929-138">System.String</span><span class="sxs-lookup"><span data-stu-id="77929-138">System.String</span></span>

### <span data-ttu-id="77929-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="77929-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="77929-140">輸出</span><span class="sxs-lookup"><span data-stu-id="77929-140">OUTPUTS</span></span>

### <span data-ttu-id="77929-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77929-141">System.Boolean</span></span>

## <span data-ttu-id="77929-142">筆記</span><span class="sxs-lookup"><span data-stu-id="77929-142">NOTES</span></span>
* <span data-ttu-id="77929-143">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="77929-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="77929-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="77929-144">RELATED LINKS</span></span>

[<span data-ttu-id="77929-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="77929-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="77929-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="77929-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


