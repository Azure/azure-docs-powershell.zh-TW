---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613316"
---
# <span data-ttu-id="9959f-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9959f-101">New-AzHostGroup</span></span>

## <span data-ttu-id="9959f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9959f-102">SYNOPSIS</span></span>
<span data-ttu-id="9959f-103">建立主機群組。</span><span class="sxs-lookup"><span data-stu-id="9959f-103">Creates a host group.</span></span>

## <span data-ttu-id="9959f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9959f-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9959f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9959f-105">DESCRIPTION</span></span>
<span data-ttu-id="9959f-106">這個 Cmdlet 會建立主機群組。</span><span class="sxs-lookup"><span data-stu-id="9959f-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="9959f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9959f-107">EXAMPLES</span></span>

### <span data-ttu-id="9959f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9959f-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="9959f-109">這個命令會在指定的位置和區域中建立主機群組。</span><span class="sxs-lookup"><span data-stu-id="9959f-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="9959f-110">參數</span><span class="sxs-lookup"><span data-stu-id="9959f-110">PARAMETERS</span></span>

### <span data-ttu-id="9959f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9959f-111">-AsJob</span></span>
<span data-ttu-id="9959f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9959f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9959f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9959f-113">-DefaultProfile</span></span>
<span data-ttu-id="9959f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9959f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9959f-115">-位置</span><span class="sxs-lookup"><span data-stu-id="9959f-115">-Location</span></span>
<span data-ttu-id="9959f-116">指定位置。</span><span class="sxs-lookup"><span data-stu-id="9959f-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9959f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9959f-117">-Name</span></span>
<span data-ttu-id="9959f-118">指定主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9959f-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9959f-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="9959f-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="9959f-120">指定主機群組可以跨越的容錯網域數目。</span><span class="sxs-lookup"><span data-stu-id="9959f-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="9959f-121">最小值為1，最大值為3。</span><span class="sxs-lookup"><span data-stu-id="9959f-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9959f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9959f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9959f-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9959f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="9959f-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="9959f-124">-Tag</span></span>
<span data-ttu-id="9959f-125">指定標記</span><span class="sxs-lookup"><span data-stu-id="9959f-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9959f-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="9959f-126">-Zone</span></span>
<span data-ttu-id="9959f-127">指定主機群組的區域。</span><span class="sxs-lookup"><span data-stu-id="9959f-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9959f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="9959f-128">-Confirm</span></span>
<span data-ttu-id="9959f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9959f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9959f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9959f-130">-WhatIf</span></span>
<span data-ttu-id="9959f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9959f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9959f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9959f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9959f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9959f-133">CommonParameters</span></span>
<span data-ttu-id="9959f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9959f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9959f-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9959f-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9959f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9959f-136">INPUTS</span></span>

### <span data-ttu-id="9959f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="9959f-137">System.String</span></span>

## <span data-ttu-id="9959f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9959f-138">OUTPUTS</span></span>

### <span data-ttu-id="9959f-139">PSHostGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9959f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9959f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9959f-140">NOTES</span></span>

## <span data-ttu-id="9959f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9959f-141">RELATED LINKS</span></span>