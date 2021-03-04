---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 86531beb13ef70f8c35de7f4921277b0f9fa0bf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902286"
---
# <span data-ttu-id="38c48-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="38c48-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="38c48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38c48-102">SYNOPSIS</span></span>
<span data-ttu-id="38c48-103">建立新的 PowerBI 內嵌容量。</span><span class="sxs-lookup"><span data-stu-id="38c48-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="38c48-104">語法</span><span class="sxs-lookup"><span data-stu-id="38c48-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c48-105">描述</span><span class="sxs-lookup"><span data-stu-id="38c48-105">DESCRIPTION</span></span>
<span data-ttu-id="38c48-106">Cmdlet New-AzPowerBIEmbeddedCapacity建立新的 PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="38c48-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="38c48-107">例子</span><span class="sxs-lookup"><span data-stu-id="38c48-107">EXAMPLES</span></span>

### <span data-ttu-id="38c48-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="38c48-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="38c48-109">在 Azure 區域美國中西部和資源群組 testRG 中建立名為 test一個容量。</span><span class="sxs-lookup"><span data-stu-id="38c48-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="38c48-110">容量的 SKU 層級為 A1。</span><span class="sxs-lookup"><span data-stu-id="38c48-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="38c48-111">參數</span><span class="sxs-lookup"><span data-stu-id="38c48-111">PARAMETERS</span></span>

### <span data-ttu-id="38c48-112">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="38c48-112">-Administrator</span></span>
<span data-ttu-id="38c48-113">在容量上設定為系統管理員的逗號分隔名稱</span><span class="sxs-lookup"><span data-stu-id="38c48-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c48-114">-DefaultProfile</span></span>
<span data-ttu-id="38c48-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38c48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c48-116">-位置</span><span class="sxs-lookup"><span data-stu-id="38c48-116">-Location</span></span>
<span data-ttu-id="38c48-117">託管 PowerBI 內嵌容量的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="38c48-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="38c48-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="38c48-118">-Name</span></span>
<span data-ttu-id="38c48-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="38c48-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="38c48-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c48-120">-ResourceGroupName</span></span>
<span data-ttu-id="38c48-121">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="38c48-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="38c48-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="38c48-122">-Sku</span></span>
<span data-ttu-id="38c48-123">容量的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="38c48-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c48-124">-標記</span><span class="sxs-lookup"><span data-stu-id="38c48-124">-Tag</span></span>
<span data-ttu-id="38c48-125">以雜湊表格形式將索引鍵值組設為容量上的標記。</span><span class="sxs-lookup"><span data-stu-id="38c48-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c48-126">-確認</span><span class="sxs-lookup"><span data-stu-id="38c48-126">-Confirm</span></span>
<span data-ttu-id="38c48-127">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="38c48-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c48-128">-WhatIf</span></span>
<span data-ttu-id="38c48-129">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="38c48-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c48-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c48-130">CommonParameters</span></span>
<span data-ttu-id="38c48-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38c48-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c48-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="38c48-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c48-133">輸入</span><span class="sxs-lookup"><span data-stu-id="38c48-133">INPUTS</span></span>

### <span data-ttu-id="38c48-134">System.String</span><span class="sxs-lookup"><span data-stu-id="38c48-134">System.String</span></span>

### <span data-ttu-id="38c48-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="38c48-135">System.String[]</span></span>

### <span data-ttu-id="38c48-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="38c48-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="38c48-137">輸出</span><span class="sxs-lookup"><span data-stu-id="38c48-137">OUTPUTS</span></span>

### <span data-ttu-id="38c48-138">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="38c48-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="38c48-139">筆記</span><span class="sxs-lookup"><span data-stu-id="38c48-139">NOTES</span></span>

## <span data-ttu-id="38c48-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="38c48-140">RELATED LINKS</span></span>

[<span data-ttu-id="38c48-141">Get-AzPowerBIEmbedded可說</span><span class="sxs-lookup"><span data-stu-id="38c48-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="38c48-142">Remove-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="38c48-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
