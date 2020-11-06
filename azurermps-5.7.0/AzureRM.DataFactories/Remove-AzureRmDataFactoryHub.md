---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 4ee22c46a3754bcb8378acb3b37da96bd11090fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449389"
---
# <span data-ttu-id="d1e42-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d1e42-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="d1e42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1e42-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e42-103">從 Azure 資料工廠移除中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e42-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1e42-104">SYNTAX</span></span>

### <span data-ttu-id="d1e42-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d1e42-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e42-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d1e42-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e42-107">說明</span><span class="sxs-lookup"><span data-stu-id="d1e42-107">DESCRIPTION</span></span>
<span data-ttu-id="d1e42-108">**AzureRmDataFactoryHub** Cmdlet 會從 Azure 資料工廠，在指定的資料工廠中移除來自 Azure 資料工廠的中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="d1e42-109">如果您移除中樞，系統會同時移除中樞中所有連結的服務和管線。</span><span class="sxs-lookup"><span data-stu-id="d1e42-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="d1e42-110">示例</span><span class="sxs-lookup"><span data-stu-id="d1e42-110">EXAMPLES</span></span>

### <span data-ttu-id="d1e42-111">範例1：移除中樞</span><span class="sxs-lookup"><span data-stu-id="d1e42-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="d1e42-112">這個命令會從名為 [ADFResourceGroup] 的 Azure 資源群組和名為 [ADFDataFactory] 的資料工廠中移除名為 ContosoDataHub 的中心。</span><span class="sxs-lookup"><span data-stu-id="d1e42-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="d1e42-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1e42-113">PARAMETERS</span></span>

### <span data-ttu-id="d1e42-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1e42-114">-DataFactory</span></span>
<span data-ttu-id="d1e42-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="d1e42-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d1e42-116">這個 Cmdlet 會從資料工廠中移除此參數指定的中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1e42-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d1e42-117">-DataFactoryName</span></span>
<span data-ttu-id="d1e42-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1e42-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d1e42-119">這個 Cmdlet 會從資料工廠中移除此參數指定的中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1e42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e42-120">-DefaultProfile</span></span>
<span data-ttu-id="d1e42-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d1e42-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1e42-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d1e42-122">-Force</span></span>
<span data-ttu-id="d1e42-123">表示此 Cmdlet 不會提示您確認就移除中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d1e42-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1e42-124">-Name</span></span>
<span data-ttu-id="d1e42-125">指定要移除之中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1e42-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e42-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e42-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1e42-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1e42-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d1e42-128">這個 Cmdlet 會從此參數指定的群組中移除中樞。</span><span class="sxs-lookup"><span data-stu-id="d1e42-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1e42-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d1e42-129">-Confirm</span></span>
<span data-ttu-id="d1e42-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1e42-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e42-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e42-131">-WhatIf</span></span>
<span data-ttu-id="d1e42-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1e42-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e42-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1e42-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e42-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e42-134">CommonParameters</span></span>
<span data-ttu-id="d1e42-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1e42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e42-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1e42-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e42-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d1e42-137">INPUTS</span></span>

### <span data-ttu-id="d1e42-138">所有</span><span class="sxs-lookup"><span data-stu-id="d1e42-138">None</span></span>
<span data-ttu-id="d1e42-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d1e42-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1e42-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d1e42-140">OUTPUTS</span></span>

### <span data-ttu-id="d1e42-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d1e42-141">System.Boolean</span></span>

## <span data-ttu-id="d1e42-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d1e42-142">NOTES</span></span>
* <span data-ttu-id="d1e42-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="d1e42-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d1e42-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1e42-144">RELATED LINKS</span></span>

[<span data-ttu-id="d1e42-145">AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d1e42-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="d1e42-146">新-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d1e42-146">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


