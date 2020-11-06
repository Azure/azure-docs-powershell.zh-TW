---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447841"
---
# <span data-ttu-id="4879a-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="4879a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4879a-102">SYNOPSIS</span></span>
<span data-ttu-id="4879a-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="4879a-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4879a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4879a-104">SYNTAX</span></span>

### <span data-ttu-id="4879a-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4879a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4879a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4879a-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4879a-107">說明</span><span class="sxs-lookup"><span data-stu-id="4879a-107">DESCRIPTION</span></span>
<span data-ttu-id="4879a-108">**AzureRmDataFactory** Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="4879a-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="4879a-109">示例</span><span class="sxs-lookup"><span data-stu-id="4879a-109">EXAMPLES</span></span>

### <span data-ttu-id="4879a-110">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="4879a-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4879a-111">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="4879a-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="4879a-112">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="4879a-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="4879a-113">參數</span><span class="sxs-lookup"><span data-stu-id="4879a-113">PARAMETERS</span></span>

### <span data-ttu-id="4879a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-114">-DataFactory</span></span>
<span data-ttu-id="4879a-115">指定要移除的 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4879a-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="4879a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4879a-116">-DefaultProfile</span></span>
<span data-ttu-id="4879a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4879a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4879a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4879a-118">-Force</span></span>
<span data-ttu-id="4879a-119">表示此 Cmdlet 會移除資料工廠，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4879a-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4879a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4879a-120">-Name</span></span>
<span data-ttu-id="4879a-121">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4879a-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4879a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4879a-122">-ResourceGroupName</span></span>
<span data-ttu-id="4879a-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4879a-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4879a-124">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="4879a-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4879a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4879a-125">-Confirm</span></span>
<span data-ttu-id="4879a-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4879a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4879a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4879a-127">-WhatIf</span></span>
<span data-ttu-id="4879a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4879a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4879a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4879a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4879a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4879a-130">CommonParameters</span></span>
<span data-ttu-id="4879a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4879a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4879a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4879a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4879a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4879a-133">INPUTS</span></span>

### <span data-ttu-id="4879a-134">所有</span><span class="sxs-lookup"><span data-stu-id="4879a-134">None</span></span>
<span data-ttu-id="4879a-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4879a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4879a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4879a-136">OUTPUTS</span></span>

### <span data-ttu-id="4879a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4879a-137">System.Boolean</span></span>

## <span data-ttu-id="4879a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4879a-138">NOTES</span></span>
* <span data-ttu-id="4879a-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="4879a-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4879a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4879a-140">RELATED LINKS</span></span>

[<span data-ttu-id="4879a-141">AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="4879a-142">新-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


