---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902870"
---
# <span data-ttu-id="e30d9-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e30d9-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e30d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e30d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e30d9-103">為負載平衡器建立後端位址資料庫組組。</span><span class="sxs-lookup"><span data-stu-id="e30d9-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e30d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e30d9-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30d9-105">描述</span><span class="sxs-lookup"><span data-stu-id="e30d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e30d9-106">**New-AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會為 Azure 負載平衡器建立後端位址集區組。</span><span class="sxs-lookup"><span data-stu-id="e30d9-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e30d9-107">例子</span><span class="sxs-lookup"><span data-stu-id="e30d9-107">EXAMPLES</span></span>

### <span data-ttu-id="e30d9-108">範例 1：為負載平衡器建立後端位址資料庫組</span><span class="sxs-lookup"><span data-stu-id="e30d9-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e30d9-109">此命令會為負載平衡器建立名為後端位址資料庫的後端位址資料庫組，名為後端AddressPool02。</span><span class="sxs-lookup"><span data-stu-id="e30d9-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e30d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e30d9-110">PARAMETERS</span></span>

### <span data-ttu-id="e30d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30d9-111">-DefaultProfile</span></span>
<span data-ttu-id="e30d9-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e30d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e30d9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e30d9-113">-Name</span></span>
<span data-ttu-id="e30d9-114">指定要建立的位址區組組組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e30d9-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="e30d9-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e30d9-115">-Confirm</span></span>
<span data-ttu-id="e30d9-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e30d9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e30d9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30d9-117">-WhatIf</span></span>
<span data-ttu-id="e30d9-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e30d9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e30d9-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e30d9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e30d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30d9-120">CommonParameters</span></span>
<span data-ttu-id="e30d9-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e30d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30d9-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e30d9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30d9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e30d9-123">INPUTS</span></span>

### <span data-ttu-id="e30d9-124">沒有</span><span class="sxs-lookup"><span data-stu-id="e30d9-124">None</span></span>

## <span data-ttu-id="e30d9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e30d9-125">OUTPUTS</span></span>

### <span data-ttu-id="e30d9-126">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e30d9-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e30d9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e30d9-127">NOTES</span></span>

## <span data-ttu-id="e30d9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e30d9-128">RELATED LINKS</span></span>

[<span data-ttu-id="e30d9-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e30d9-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e30d9-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e30d9-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e30d9-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e30d9-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


