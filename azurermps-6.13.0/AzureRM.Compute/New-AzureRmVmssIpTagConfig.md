---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443967"
---
# <span data-ttu-id="e2c39-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="e2c39-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="e2c39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2c39-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c39-103">為 VMSS 的網路介面建立 IP Tag 物件。</span><span class="sxs-lookup"><span data-stu-id="e2c39-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2c39-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2c39-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c39-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2c39-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c39-106">**新的-AzureRmVmssIpTagConfig** Cmdlet 會為虛擬電腦規模集 (VMSS) 的網路介面建立 IP 標籤設定物件。</span><span class="sxs-lookup"><span data-stu-id="e2c39-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e2c39-107">將此 Cmdlet 的配置指定為 New-AzureRmVmssIpConfig Cmdlet 的 *IPTag* 參數。</span><span class="sxs-lookup"><span data-stu-id="e2c39-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="e2c39-108">示例</span><span class="sxs-lookup"><span data-stu-id="e2c39-108">EXAMPLES</span></span>

### <span data-ttu-id="e2c39-109">範例1</span><span class="sxs-lookup"><span data-stu-id="e2c39-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="e2c39-110">這個命令會建立含 "FirstPartyUsage" 類型和 "Sql" 標記的 IP 標籤局部物件，然後建立具有此 IP 標籤的 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e2c39-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="e2c39-111">參數</span><span class="sxs-lookup"><span data-stu-id="e2c39-111">PARAMETERS</span></span>

### <span data-ttu-id="e2c39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c39-112">-DefaultProfile</span></span>
<span data-ttu-id="e2c39-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2c39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2c39-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="e2c39-114">-IpTagType</span></span>
<span data-ttu-id="e2c39-115">指定 IP 標記類型。</span><span class="sxs-lookup"><span data-stu-id="e2c39-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="e2c39-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2c39-116">-Tag</span></span>
<span data-ttu-id="e2c39-117">指定 IP 標記值。</span><span class="sxs-lookup"><span data-stu-id="e2c39-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="e2c39-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e2c39-118">-Confirm</span></span>
<span data-ttu-id="e2c39-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2c39-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2c39-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c39-120">-WhatIf</span></span>
<span data-ttu-id="e2c39-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2c39-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2c39-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2c39-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2c39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c39-123">CommonParameters</span></span>
<span data-ttu-id="e2c39-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2c39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c39-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2c39-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c39-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e2c39-126">INPUTS</span></span>

### <span data-ttu-id="e2c39-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e2c39-127">System.String</span></span>

## <span data-ttu-id="e2c39-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e2c39-128">OUTPUTS</span></span>

### <span data-ttu-id="e2c39-129">VirtualMachineScaleSetIpTag 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="e2c39-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="e2c39-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e2c39-130">NOTES</span></span>

## <span data-ttu-id="e2c39-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2c39-131">RELATED LINKS</span></span>
