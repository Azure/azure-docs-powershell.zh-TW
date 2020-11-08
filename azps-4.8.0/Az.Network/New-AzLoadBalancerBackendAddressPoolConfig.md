---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136277"
---
# <span data-ttu-id="9b770-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b770-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="9b770-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b770-102">SYNOPSIS</span></span>
<span data-ttu-id="9b770-103">為負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="9b770-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="9b770-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b770-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b770-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b770-105">DESCRIPTION</span></span>
<span data-ttu-id="9b770-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會為 Azure 負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="9b770-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9b770-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b770-107">EXAMPLES</span></span>

### <span data-ttu-id="9b770-108">範例1：為負載平衡器建立後端位址集區配置</span><span class="sxs-lookup"><span data-stu-id="9b770-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="9b770-109">這個命令會為負載平衡器建立名為 BackendAddressPool02 的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="9b770-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="9b770-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b770-110">PARAMETERS</span></span>

### <span data-ttu-id="9b770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b770-111">-DefaultProfile</span></span>
<span data-ttu-id="9b770-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b770-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b770-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b770-113">-Name</span></span>
<span data-ttu-id="9b770-114">指定要建立的位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="9b770-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b770-115">-確認</span><span class="sxs-lookup"><span data-stu-id="9b770-115">-Confirm</span></span>
<span data-ttu-id="9b770-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b770-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b770-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b770-117">-WhatIf</span></span>
<span data-ttu-id="9b770-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b770-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b770-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b770-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b770-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b770-120">CommonParameters</span></span>
<span data-ttu-id="9b770-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b770-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b770-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b770-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b770-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9b770-123">INPUTS</span></span>

### <span data-ttu-id="9b770-124">所有</span><span class="sxs-lookup"><span data-stu-id="9b770-124">None</span></span>

## <span data-ttu-id="9b770-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9b770-125">OUTPUTS</span></span>

### <span data-ttu-id="9b770-126">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9b770-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9b770-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9b770-127">NOTES</span></span>

## <span data-ttu-id="9b770-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b770-128">RELATED LINKS</span></span>

[<span data-ttu-id="9b770-129">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b770-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9b770-130">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b770-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9b770-131">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9b770-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


