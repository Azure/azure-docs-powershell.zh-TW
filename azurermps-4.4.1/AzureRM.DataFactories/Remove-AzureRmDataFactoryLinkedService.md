---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: d3ea4c3f221a3d05c9d43e780cde359ff36843f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624326"
---
# <span data-ttu-id="7dc50-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7dc50-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="7dc50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dc50-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc50-103">從 Azure 資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc50-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dc50-104">SYNTAX</span></span>

### <span data-ttu-id="7dc50-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="7dc50-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7dc50-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7dc50-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dc50-107">說明</span><span class="sxs-lookup"><span data-stu-id="7dc50-107">DESCRIPTION</span></span>
<span data-ttu-id="7dc50-108">**AzureRmDataFactoryLinkedService** Cmdlet 會從 Azure 資料工廠中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="7dc50-109">示例</span><span class="sxs-lookup"><span data-stu-id="7dc50-109">EXAMPLES</span></span>

### <span data-ttu-id="7dc50-110">範例1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="7dc50-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="7dc50-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="7dc50-112">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="7dc50-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="7dc50-113">參數</span><span class="sxs-lookup"><span data-stu-id="7dc50-113">PARAMETERS</span></span>

### <span data-ttu-id="7dc50-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7dc50-114">-DataFactory</span></span>
<span data-ttu-id="7dc50-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dc50-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7dc50-116">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7dc50-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7dc50-117">-DataFactoryName</span></span>
<span data-ttu-id="7dc50-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc50-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7dc50-119">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7dc50-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7dc50-120">-Force</span></span>
<span data-ttu-id="7dc50-121">表示此 Cmdlet 會移除連結的服務，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7dc50-121">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7dc50-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dc50-122">-Name</span></span>
<span data-ttu-id="7dc50-123">指定要移除之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc50-123">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="7dc50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc50-124">-ResourceGroupName</span></span>
<span data-ttu-id="7dc50-125">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc50-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7dc50-126">這個 Cmdlet 會從此參數指定的群組中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7dc50-126">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7dc50-127">-確認</span><span class="sxs-lookup"><span data-stu-id="7dc50-127">-Confirm</span></span>
<span data-ttu-id="7dc50-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7dc50-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc50-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc50-129">-WhatIf</span></span>
<span data-ttu-id="7dc50-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7dc50-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dc50-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dc50-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc50-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc50-132">-DefaultProfile</span></span>
<span data-ttu-id="7dc50-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dc50-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc50-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc50-134">CommonParameters</span></span>
<span data-ttu-id="7dc50-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dc50-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc50-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dc50-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc50-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7dc50-137">INPUTS</span></span>

## <span data-ttu-id="7dc50-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7dc50-138">OUTPUTS</span></span>

### <span data-ttu-id="7dc50-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7dc50-139">System.Boolean</span></span>

## <span data-ttu-id="7dc50-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7dc50-140">NOTES</span></span>
* <span data-ttu-id="7dc50-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="7dc50-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7dc50-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dc50-142">RELATED LINKS</span></span>

[<span data-ttu-id="7dc50-143">AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7dc50-143">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="7dc50-144">新-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="7dc50-144">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

