---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 0f8bd59f6215a2f9cc2bdbcc993da0cb373f70af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788138"
---
# <span data-ttu-id="fc5c0-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc5c0-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="fc5c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5c0-103">從 Azure 資料工廠移除閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="fc5c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc5c0-104">SYNTAX</span></span>

### <span data-ttu-id="fc5c0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fc5c0-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fc5c0-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc5c0-107">DESCRIPTION</span></span>
<span data-ttu-id="fc5c0-108">**AzDataFactoryGateway** Cmdlet 會從 Azure 資料工廠中移除指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="fc5c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc5c0-109">EXAMPLES</span></span>

### <span data-ttu-id="fc5c0-110">範例1：移除閘道</span><span class="sxs-lookup"><span data-stu-id="fc5c0-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="fc5c0-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 ContosoGateway 的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="fc5c0-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc5c0-112">PARAMETERS</span></span>

### <span data-ttu-id="fc5c0-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fc5c0-113">-DataFactory</span></span>
<span data-ttu-id="fc5c0-114">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fc5c0-115">這個 Cmdlet 會從資料工廠中移除此參數指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc5c0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fc5c0-116">-DataFactoryName</span></span>
<span data-ttu-id="fc5c0-117">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fc5c0-118">這個 Cmdlet 會從資料工廠中移除此參數指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc5c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5c0-119">-DefaultProfile</span></span>
<span data-ttu-id="fc5c0-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fc5c0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc5c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fc5c0-121">-Force</span></span>
<span data-ttu-id="fc5c0-122">指出這個 Cmdlet 不會提示您確認就移除閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fc5c0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc5c0-123">-Name</span></span>
<span data-ttu-id="fc5c0-124">指定要移除之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc5c0-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fc5c0-127">這個 Cmdlet 會移除屬於此參數指定之群組的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc5c0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fc5c0-128">-Confirm</span></span>
<span data-ttu-id="fc5c0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5c0-130">-WhatIf</span></span>
<span data-ttu-id="fc5c0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5c0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5c0-133">CommonParameters</span></span>
<span data-ttu-id="fc5c0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5c0-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc5c0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5c0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fc5c0-136">INPUTS</span></span>

### <span data-ttu-id="fc5c0-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fc5c0-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fc5c0-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fc5c0-138">System.String</span></span>

## <span data-ttu-id="fc5c0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fc5c0-139">OUTPUTS</span></span>

### <span data-ttu-id="fc5c0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fc5c0-140">System.Boolean</span></span>

## <span data-ttu-id="fc5c0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fc5c0-141">NOTES</span></span>
* <span data-ttu-id="fc5c0-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="fc5c0-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fc5c0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc5c0-143">RELATED LINKS</span></span>

[<span data-ttu-id="fc5c0-144">AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc5c0-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="fc5c0-145">新-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc5c0-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="fc5c0-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc5c0-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


