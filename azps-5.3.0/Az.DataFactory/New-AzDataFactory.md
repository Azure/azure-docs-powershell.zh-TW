---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439491"
---
# <span data-ttu-id="33266-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33266-101">New-AzDataFactory</span></span>

## <span data-ttu-id="33266-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33266-102">SYNOPSIS</span></span>
<span data-ttu-id="33266-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="33266-103">Creates a data factory.</span></span>

## <span data-ttu-id="33266-104">句法</span><span class="sxs-lookup"><span data-stu-id="33266-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33266-105">說明</span><span class="sxs-lookup"><span data-stu-id="33266-105">DESCRIPTION</span></span>
<span data-ttu-id="33266-106">**AzDataFactory** Cmdlet 會使用指定的資源群組名稱和位置來建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="33266-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="33266-107">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="33266-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="33266-108">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="33266-108">Create a data factory.</span></span> 
- <span data-ttu-id="33266-109">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="33266-109">Create linked services.</span></span> 
- <span data-ttu-id="33266-110">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="33266-110">Create datasets.</span></span> 
- <span data-ttu-id="33266-111">建立管線。</span><span class="sxs-lookup"><span data-stu-id="33266-111">Create a pipeline.</span></span>

## <span data-ttu-id="33266-112">示例</span><span class="sxs-lookup"><span data-stu-id="33266-112">EXAMPLES</span></span>

### <span data-ttu-id="33266-113">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="33266-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="33266-114">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="33266-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="33266-115">參數</span><span class="sxs-lookup"><span data-stu-id="33266-115">PARAMETERS</span></span>

### <span data-ttu-id="33266-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33266-116">-DefaultProfile</span></span>
<span data-ttu-id="33266-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="33266-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33266-118">-Force</span><span class="sxs-lookup"><span data-stu-id="33266-118">-Force</span></span>
<span data-ttu-id="33266-119">表示此 Cmdlet 會取代現有的資料工廠，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33266-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="33266-120">-位置</span><span class="sxs-lookup"><span data-stu-id="33266-120">-Location</span></span>
<span data-ttu-id="33266-121">指定資料工廠的位置，例如 WestUS 或 EastUS。</span><span class="sxs-lookup"><span data-stu-id="33266-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="33266-122">目前僅支援 WestUS。</span><span class="sxs-lookup"><span data-stu-id="33266-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="33266-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="33266-123">-Name</span></span>
<span data-ttu-id="33266-124">指定要建立的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="33266-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33266-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33266-125">-ResourceGroupName</span></span>
<span data-ttu-id="33266-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33266-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="33266-127">這個 Cmdlet 會建立屬於此參數指定之群組的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="33266-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33266-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="33266-128">-Tag</span></span>
<span data-ttu-id="33266-129">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="33266-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33266-130">-確認</span><span class="sxs-lookup"><span data-stu-id="33266-130">-Confirm</span></span>
<span data-ttu-id="33266-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33266-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33266-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33266-132">-WhatIf</span></span>
<span data-ttu-id="33266-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33266-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33266-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33266-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33266-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33266-135">CommonParameters</span></span>
<span data-ttu-id="33266-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33266-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33266-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33266-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33266-138">輸入</span><span class="sxs-lookup"><span data-stu-id="33266-138">INPUTS</span></span>

### <span data-ttu-id="33266-139">System.object</span><span class="sxs-lookup"><span data-stu-id="33266-139">System.String</span></span>

### <span data-ttu-id="33266-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="33266-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="33266-141">輸出</span><span class="sxs-lookup"><span data-stu-id="33266-141">OUTPUTS</span></span>

### <span data-ttu-id="33266-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="33266-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="33266-143">筆記</span><span class="sxs-lookup"><span data-stu-id="33266-143">NOTES</span></span>
* <span data-ttu-id="33266-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="33266-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="33266-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="33266-145">RELATED LINKS</span></span>

[<span data-ttu-id="33266-146">AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33266-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="33266-147">移除-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33266-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


