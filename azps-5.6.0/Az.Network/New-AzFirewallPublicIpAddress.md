---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: 2e7c1b0468ed3faf37c8f11bc0cb1eca707195bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903558"
---
# <span data-ttu-id="9344c-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9344c-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="9344c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9344c-102">SYNOPSIS</span></span>
<span data-ttu-id="9344c-103">這是可用於 Azure 防火牆上多點子之 Ip 位址的預留位置。</span><span class="sxs-lookup"><span data-stu-id="9344c-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="9344c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9344c-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9344c-105">描述</span><span class="sxs-lookup"><span data-stu-id="9344c-105">DESCRIPTION</span></span>
<span data-ttu-id="9344c-106">這是可用於 Azure 防火牆上多點子之 Ip 位址的預留位置。</span><span class="sxs-lookup"><span data-stu-id="9344c-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="9344c-107">例子</span><span class="sxs-lookup"><span data-stu-id="9344c-107">EXAMPLES</span></span>

### <span data-ttu-id="9344c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9344c-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="9344c-109">$publicIp ip 位址 20.2.3.4 的預留位置</span><span class="sxs-lookup"><span data-stu-id="9344c-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="9344c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9344c-110">PARAMETERS</span></span>

### <span data-ttu-id="9344c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="9344c-111">-Address</span></span>
<span data-ttu-id="9344c-112">附加至中樞之防火牆的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="9344c-112">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9344c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9344c-113">-DefaultProfile</span></span>
<span data-ttu-id="9344c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9344c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9344c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="9344c-115">-Confirm</span></span>
<span data-ttu-id="9344c-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9344c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9344c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9344c-117">-WhatIf</span></span>
<span data-ttu-id="9344c-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9344c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9344c-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9344c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9344c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9344c-120">CommonParameters</span></span>
<span data-ttu-id="9344c-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9344c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9344c-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9344c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9344c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9344c-123">INPUTS</span></span>

### <span data-ttu-id="9344c-124">沒有</span><span class="sxs-lookup"><span data-stu-id="9344c-124">None</span></span>

## <span data-ttu-id="9344c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9344c-125">OUTPUTS</span></span>

### <span data-ttu-id="9344c-126">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9344c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="9344c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9344c-127">NOTES</span></span>

## <span data-ttu-id="9344c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9344c-128">RELATED LINKS</span></span>
