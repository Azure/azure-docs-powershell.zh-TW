---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128784"
---
# <span data-ttu-id="04b22-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04b22-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="04b22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04b22-102">SYNOPSIS</span></span>
<span data-ttu-id="04b22-103">從 Azure 資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="04b22-104">句法</span><span class="sxs-lookup"><span data-stu-id="04b22-104">SYNTAX</span></span>

### <span data-ttu-id="04b22-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="04b22-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b22-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="04b22-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b22-107">說明</span><span class="sxs-lookup"><span data-stu-id="04b22-107">DESCRIPTION</span></span>
<span data-ttu-id="04b22-108">**AzDataFactoryLinkedService** Cmdlet 會從 Azure 資料工廠中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="04b22-109">示例</span><span class="sxs-lookup"><span data-stu-id="04b22-109">EXAMPLES</span></span>

### <span data-ttu-id="04b22-110">範例1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="04b22-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="04b22-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="04b22-112">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="04b22-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="04b22-113">參數</span><span class="sxs-lookup"><span data-stu-id="04b22-113">PARAMETERS</span></span>

### <span data-ttu-id="04b22-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="04b22-114">-DataFactory</span></span>
<span data-ttu-id="04b22-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="04b22-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="04b22-116">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="04b22-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="04b22-117">-DataFactoryName</span></span>
<span data-ttu-id="04b22-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="04b22-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="04b22-119">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="04b22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b22-120">-DefaultProfile</span></span>
<span data-ttu-id="04b22-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="04b22-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04b22-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04b22-122">-Force</span></span>
<span data-ttu-id="04b22-123">表示此 Cmdlet 會移除連結的服務，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04b22-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="04b22-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="04b22-124">-Name</span></span>
<span data-ttu-id="04b22-125">指定要移除之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="04b22-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b22-126">-ResourceGroupName</span></span>
<span data-ttu-id="04b22-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04b22-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="04b22-128">這個 Cmdlet 會從此參數指定的群組中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="04b22-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="04b22-129">-確認</span><span class="sxs-lookup"><span data-stu-id="04b22-129">-Confirm</span></span>
<span data-ttu-id="04b22-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04b22-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b22-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b22-131">-WhatIf</span></span>
<span data-ttu-id="04b22-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04b22-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b22-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04b22-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b22-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b22-134">CommonParameters</span></span>
<span data-ttu-id="04b22-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04b22-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b22-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04b22-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b22-137">輸入</span><span class="sxs-lookup"><span data-stu-id="04b22-137">INPUTS</span></span>

### <span data-ttu-id="04b22-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="04b22-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="04b22-139">System.object</span><span class="sxs-lookup"><span data-stu-id="04b22-139">System.String</span></span>

## <span data-ttu-id="04b22-140">輸出</span><span class="sxs-lookup"><span data-stu-id="04b22-140">OUTPUTS</span></span>

### <span data-ttu-id="04b22-141">System.void</span><span class="sxs-lookup"><span data-stu-id="04b22-141">System.Void</span></span>

## <span data-ttu-id="04b22-142">筆記</span><span class="sxs-lookup"><span data-stu-id="04b22-142">NOTES</span></span>
* <span data-ttu-id="04b22-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="04b22-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="04b22-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="04b22-144">RELATED LINKS</span></span>

[<span data-ttu-id="04b22-145">AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04b22-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="04b22-146">新-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04b22-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

