---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3f2515a1c1039dbf9ff4a0635111c95a610d9834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791686"
---
# <span data-ttu-id="4a836-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a836-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a836-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a836-102">SYNOPSIS</span></span>
<span data-ttu-id="4a836-103">建立新的 PowerBI 內嵌容量。</span><span class="sxs-lookup"><span data-stu-id="4a836-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4a836-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a836-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a836-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a836-105">DESCRIPTION</span></span>
<span data-ttu-id="4a836-106">New-AzPowerBIEmbeddedCapacity Cmdlet 會建立新的 PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="4a836-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4a836-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a836-107">EXAMPLES</span></span>

### <span data-ttu-id="4a836-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4a836-108">Example 1</span></span>
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

<span data-ttu-id="4a836-109">在 Azure 地區的 [美國] 和 [資源群組] testRG 中，建立名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="4a836-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="4a836-110">容量的 sku 層級會是 A1。</span><span class="sxs-lookup"><span data-stu-id="4a836-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="4a836-111">參數</span><span class="sxs-lookup"><span data-stu-id="4a836-111">PARAMETERS</span></span>

### <span data-ttu-id="4a836-112">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="4a836-112">-Administrator</span></span>
<span data-ttu-id="4a836-113">在容量上將逗號分隔的名稱設定為系統管理員</span><span class="sxs-lookup"><span data-stu-id="4a836-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="4a836-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a836-114">-DefaultProfile</span></span>
<span data-ttu-id="4a836-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a836-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a836-116">-位置</span><span class="sxs-lookup"><span data-stu-id="4a836-116">-Location</span></span>
<span data-ttu-id="4a836-117">存放 PowerBI 內嵌容量的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="4a836-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="4a836-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a836-118">-Name</span></span>
<span data-ttu-id="4a836-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="4a836-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4a836-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a836-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a836-121">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4a836-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4a836-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="4a836-122">-Sku</span></span>
<span data-ttu-id="4a836-123">容量的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="4a836-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="4a836-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a836-124">-Tag</span></span>
<span data-ttu-id="4a836-125">雜湊資料表形式的鍵值對，在容量中設為標記。</span><span class="sxs-lookup"><span data-stu-id="4a836-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="4a836-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4a836-126">-Confirm</span></span>
<span data-ttu-id="4a836-127">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="4a836-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4a836-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a836-128">-WhatIf</span></span>
<span data-ttu-id="4a836-129">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="4a836-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4a836-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a836-130">CommonParameters</span></span>
<span data-ttu-id="4a836-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a836-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a836-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a836-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a836-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4a836-133">INPUTS</span></span>

### <span data-ttu-id="4a836-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4a836-134">System.String</span></span>

### <span data-ttu-id="4a836-135">System.object []</span><span class="sxs-lookup"><span data-stu-id="4a836-135">System.String[]</span></span>

### <span data-ttu-id="4a836-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a836-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a836-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4a836-137">OUTPUTS</span></span>

### <span data-ttu-id="4a836-138">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="4a836-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a836-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4a836-139">NOTES</span></span>

## <span data-ttu-id="4a836-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a836-140">RELATED LINKS</span></span>

[<span data-ttu-id="4a836-141">AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a836-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4a836-142">移除-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a836-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
