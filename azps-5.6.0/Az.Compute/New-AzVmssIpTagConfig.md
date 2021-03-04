---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916222"
---
# <span data-ttu-id="be207-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="be207-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="be207-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be207-102">SYNOPSIS</span></span>
<span data-ttu-id="be207-103">為 VMSS 的網路介面建立 IP 標記物件。</span><span class="sxs-lookup"><span data-stu-id="be207-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="be207-104">語法</span><span class="sxs-lookup"><span data-stu-id="be207-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be207-105">描述</span><span class="sxs-lookup"><span data-stu-id="be207-105">DESCRIPTION</span></span>
<span data-ttu-id="be207-106">**New-Az VmssIpTagConfig** Cmdlet 會針對虛擬機器規模集 (VMSS) 的網路介面建立 IP 標記) 。</span><span class="sxs-lookup"><span data-stu-id="be207-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="be207-107">指定此 Cmdlet 的設定為 *New-AzVmssIpConfig* Cmdlet 的 IPTag 參數。</span><span class="sxs-lookup"><span data-stu-id="be207-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="be207-108">例子</span><span class="sxs-lookup"><span data-stu-id="be207-108">EXAMPLES</span></span>

### <span data-ttu-id="be207-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="be207-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="be207-110">此命令會建立具有 'FirstPartyUsage' 類型和 'Sql' 標記的 IP 標記本機物件，然後建立具有此 IP 標記的 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="be207-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="be207-111">參數</span><span class="sxs-lookup"><span data-stu-id="be207-111">PARAMETERS</span></span>

### <span data-ttu-id="be207-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be207-112">-DefaultProfile</span></span>
<span data-ttu-id="be207-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="be207-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be207-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="be207-114">-IpTagType</span></span>
<span data-ttu-id="be207-115">指定 IP 標記類型。</span><span class="sxs-lookup"><span data-stu-id="be207-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="be207-116">-標記</span><span class="sxs-lookup"><span data-stu-id="be207-116">-Tag</span></span>
<span data-ttu-id="be207-117">指定 IP 標記值。</span><span class="sxs-lookup"><span data-stu-id="be207-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be207-118">-確認</span><span class="sxs-lookup"><span data-stu-id="be207-118">-Confirm</span></span>
<span data-ttu-id="be207-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="be207-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be207-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be207-120">-WhatIf</span></span>
<span data-ttu-id="be207-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be207-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be207-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be207-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be207-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be207-123">CommonParameters</span></span>
<span data-ttu-id="be207-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be207-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be207-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be207-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be207-126">輸入</span><span class="sxs-lookup"><span data-stu-id="be207-126">INPUTS</span></span>

### <span data-ttu-id="be207-127">System.String</span><span class="sxs-lookup"><span data-stu-id="be207-127">System.String</span></span>

## <span data-ttu-id="be207-128">輸出</span><span class="sxs-lookup"><span data-stu-id="be207-128">OUTPUTS</span></span>

### <span data-ttu-id="be207-129">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="be207-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="be207-130">筆記</span><span class="sxs-lookup"><span data-stu-id="be207-130">NOTES</span></span>

## <span data-ttu-id="be207-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="be207-131">RELATED LINKS</span></span>
