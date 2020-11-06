---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444963"
---
# <span data-ttu-id="78d4b-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="78d4b-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="78d4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="78d4b-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="78d4b-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78d4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="78d4b-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78d4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="78d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="78d4b-106">**AzureRmDataFactory** Cmdlet 會使用指定的資源群組名稱和位置來建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="78d4b-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="78d4b-107">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="78d4b-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="78d4b-108">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="78d4b-108">Create a data factory.</span></span> 
- <span data-ttu-id="78d4b-109">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="78d4b-109">Create linked services.</span></span> 
- <span data-ttu-id="78d4b-110">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="78d4b-110">Create datasets.</span></span> 
- <span data-ttu-id="78d4b-111">建立管線。</span><span class="sxs-lookup"><span data-stu-id="78d4b-111">Create a pipeline.</span></span>

## <span data-ttu-id="78d4b-112">示例</span><span class="sxs-lookup"><span data-stu-id="78d4b-112">EXAMPLES</span></span>

### <span data-ttu-id="78d4b-113">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="78d4b-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="78d4b-114">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="78d4b-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="78d4b-115">參數</span><span class="sxs-lookup"><span data-stu-id="78d4b-115">PARAMETERS</span></span>

### <span data-ttu-id="78d4b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="78d4b-116">-Force</span></span>
<span data-ttu-id="78d4b-117">表示此 Cmdlet 會取代現有的資料工廠，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78d4b-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="78d4b-118">-位置</span><span class="sxs-lookup"><span data-stu-id="78d4b-118">-Location</span></span>
<span data-ttu-id="78d4b-119">指定資料工廠的位置，例如 WestUS 或 EastUS。</span><span class="sxs-lookup"><span data-stu-id="78d4b-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="78d4b-120">目前僅支援 WestUS。</span><span class="sxs-lookup"><span data-stu-id="78d4b-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="78d4b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="78d4b-121">-Name</span></span>
<span data-ttu-id="78d4b-122">指定要建立的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="78d4b-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="78d4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="78d4b-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78d4b-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="78d4b-125">這個 Cmdlet 會建立屬於此參數指定之群組的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="78d4b-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78d4b-126">-標記</span><span class="sxs-lookup"><span data-stu-id="78d4b-126">-Tags</span></span>
<span data-ttu-id="78d4b-127">指定資料工廠的標記。</span><span class="sxs-lookup"><span data-stu-id="78d4b-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="78d4b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="78d4b-128">-Confirm</span></span>
<span data-ttu-id="78d4b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78d4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d4b-130">-WhatIf</span></span>
<span data-ttu-id="78d4b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78d4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d4b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78d4b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d4b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d4b-133">-DefaultProfile</span></span>
<span data-ttu-id="78d4b-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78d4b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d4b-135">CommonParameters</span></span>
<span data-ttu-id="78d4b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78d4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d4b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78d4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d4b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="78d4b-138">INPUTS</span></span>

## <span data-ttu-id="78d4b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="78d4b-139">OUTPUTS</span></span>

### <span data-ttu-id="78d4b-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78d4b-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="78d4b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="78d4b-141">NOTES</span></span>
* <span data-ttu-id="78d4b-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="78d4b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="78d4b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="78d4b-143">RELATED LINKS</span></span>

[<span data-ttu-id="78d4b-144">AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="78d4b-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="78d4b-145">移除-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="78d4b-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


