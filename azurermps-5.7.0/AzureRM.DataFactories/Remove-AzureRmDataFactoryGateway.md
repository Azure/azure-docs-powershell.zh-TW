---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449387"
---
# <span data-ttu-id="dc38f-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="dc38f-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="dc38f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc38f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc38f-103">從 Azure 資料工廠移除閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc38f-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc38f-104">SYNTAX</span></span>

### <span data-ttu-id="dc38f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="dc38f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc38f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dc38f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc38f-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc38f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc38f-108">**AzureRmDataFactoryGateway** Cmdlet 會從 Azure 資料工廠中移除指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="dc38f-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc38f-109">EXAMPLES</span></span>

### <span data-ttu-id="dc38f-110">範例1：移除閘道</span><span class="sxs-lookup"><span data-stu-id="dc38f-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="dc38f-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 ContosoGateway 的閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="dc38f-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc38f-112">PARAMETERS</span></span>

### <span data-ttu-id="dc38f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc38f-113">-DataFactory</span></span>
<span data-ttu-id="dc38f-114">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="dc38f-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dc38f-115">這個 Cmdlet 會從資料工廠中移除此參數指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dc38f-116">-DataFactoryName</span></span>
<span data-ttu-id="dc38f-117">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc38f-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dc38f-118">這個 Cmdlet 會從資料工廠中移除此參數指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc38f-119">-DefaultProfile</span></span>
<span data-ttu-id="dc38f-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc38f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc38f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc38f-121">-Force</span></span>
<span data-ttu-id="dc38f-122">指出這個 Cmdlet 不會提示您確認就移除閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dc38f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc38f-123">-Name</span></span>
<span data-ttu-id="dc38f-124">指定要移除之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc38f-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc38f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc38f-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc38f-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dc38f-127">這個 Cmdlet 會移除屬於此參數指定之群組的閘道。</span><span class="sxs-lookup"><span data-stu-id="dc38f-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="dc38f-128">-Confirm</span></span>
<span data-ttu-id="dc38f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc38f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc38f-130">-WhatIf</span></span>
<span data-ttu-id="dc38f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc38f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc38f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc38f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc38f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc38f-133">CommonParameters</span></span>
<span data-ttu-id="dc38f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc38f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc38f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc38f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc38f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dc38f-136">INPUTS</span></span>

### <span data-ttu-id="dc38f-137">所有</span><span class="sxs-lookup"><span data-stu-id="dc38f-137">None</span></span>
<span data-ttu-id="dc38f-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dc38f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc38f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="dc38f-139">OUTPUTS</span></span>

### <span data-ttu-id="dc38f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="dc38f-140">System.Boolean</span></span>

## <span data-ttu-id="dc38f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="dc38f-141">NOTES</span></span>
* <span data-ttu-id="dc38f-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="dc38f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dc38f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc38f-143">RELATED LINKS</span></span>

[<span data-ttu-id="dc38f-144">AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="dc38f-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="dc38f-145">新-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="dc38f-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="dc38f-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="dc38f-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


