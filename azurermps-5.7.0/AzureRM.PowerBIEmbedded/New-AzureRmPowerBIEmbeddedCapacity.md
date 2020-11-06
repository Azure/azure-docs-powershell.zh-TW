---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447000"
---
# <span data-ttu-id="c3633-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c3633-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c3633-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3633-102">SYNOPSIS</span></span>
<span data-ttu-id="c3633-103">建立新的 PowerBI 內嵌容量。</span><span class="sxs-lookup"><span data-stu-id="c3633-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3633-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3633-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="c3633-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3633-105">DESCRIPTION</span></span>
<span data-ttu-id="c3633-106">New-AzureRmPowerBIEmbeddedCapacity Cmdlet 會建立新的 PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="c3633-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c3633-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3633-107">EXAMPLES</span></span>

### <span data-ttu-id="c3633-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c3633-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="c3633-109">在 Azure 地區的 [美國] 和 [資源群組] testRG 中，建立名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="c3633-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="c3633-110">容量的 sku 層級會是 A1。</span><span class="sxs-lookup"><span data-stu-id="c3633-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="c3633-111">參數</span><span class="sxs-lookup"><span data-stu-id="c3633-111">PARAMETERS</span></span>

### <span data-ttu-id="c3633-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3633-112">-ResourceGroupName</span></span>
<span data-ttu-id="c3633-113">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c3633-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3633-114">-Name</span></span>
<span data-ttu-id="c3633-115">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="c3633-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-116">-位置</span><span class="sxs-lookup"><span data-stu-id="c3633-116">-Location</span></span>
<span data-ttu-id="c3633-117">存放 PowerBI 內嵌容量的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="c3633-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-118">-Sku</span><span class="sxs-lookup"><span data-stu-id="c3633-118">-Sku</span></span>
<span data-ttu-id="c3633-119">容量的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="c3633-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-120">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="c3633-120">-Administrator</span></span>
<span data-ttu-id="c3633-121">以逗號分隔的容量名稱，在容量上設定為系統管理員</span><span class="sxs-lookup"><span data-stu-id="c3633-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3633-122">-Tag</span></span>
<span data-ttu-id="c3633-123">雜湊資料表形式的鍵值對，在容量中設為標記。</span><span class="sxs-lookup"><span data-stu-id="c3633-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c3633-124">-Confirm</span></span>
<span data-ttu-id="c3633-125">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="c3633-125">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3633-126">-WhatIf</span></span>
<span data-ttu-id="c3633-127">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="c3633-127">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3633-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3633-128">CommonParameters</span></span>
<span data-ttu-id="c3633-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3633-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3633-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3633-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3633-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c3633-131">INPUTS</span></span>

### <span data-ttu-id="c3633-132">所有</span><span class="sxs-lookup"><span data-stu-id="c3633-132">None</span></span>
<span data-ttu-id="c3633-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c3633-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3633-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c3633-134">OUTPUTS</span></span>

### <span data-ttu-id="c3633-135">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="c3633-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c3633-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c3633-136">NOTES</span></span>

## <span data-ttu-id="c3633-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3633-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3633-138">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c3633-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c3633-139">移除-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c3633-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
