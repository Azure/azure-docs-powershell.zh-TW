---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449036"
---
# <span data-ttu-id="26dd8-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26dd8-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="26dd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="26dd8-103">為負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="26dd8-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26dd8-104">句法</span><span class="sxs-lookup"><span data-stu-id="26dd8-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26dd8-105">說明</span><span class="sxs-lookup"><span data-stu-id="26dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="26dd8-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會為 Azure 負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="26dd8-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="26dd8-107">示例</span><span class="sxs-lookup"><span data-stu-id="26dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="26dd8-108">範例1：為負載平衡器建立後端位址集區配置</span><span class="sxs-lookup"><span data-stu-id="26dd8-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="26dd8-109">這個命令會為負載平衡器建立名為 BackendAddressPool02 的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="26dd8-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="26dd8-110">參數</span><span class="sxs-lookup"><span data-stu-id="26dd8-110">PARAMETERS</span></span>

### <span data-ttu-id="26dd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dd8-111">-DefaultProfile</span></span>
<span data-ttu-id="26dd8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26dd8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26dd8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="26dd8-113">-Name</span></span>
<span data-ttu-id="26dd8-114">指定要建立的位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="26dd8-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="26dd8-115">-確認</span><span class="sxs-lookup"><span data-stu-id="26dd8-115">-Confirm</span></span>
<span data-ttu-id="26dd8-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26dd8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26dd8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26dd8-117">-WhatIf</span></span>
<span data-ttu-id="26dd8-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26dd8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26dd8-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26dd8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26dd8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dd8-120">CommonParameters</span></span>
<span data-ttu-id="26dd8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26dd8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dd8-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26dd8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dd8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="26dd8-123">INPUTS</span></span>

### <span data-ttu-id="26dd8-124">所有</span><span class="sxs-lookup"><span data-stu-id="26dd8-124">None</span></span>

## <span data-ttu-id="26dd8-125">輸出</span><span class="sxs-lookup"><span data-stu-id="26dd8-125">OUTPUTS</span></span>

### <span data-ttu-id="26dd8-126">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26dd8-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="26dd8-127">筆記</span><span class="sxs-lookup"><span data-stu-id="26dd8-127">NOTES</span></span>

## <span data-ttu-id="26dd8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="26dd8-128">RELATED LINKS</span></span>

[<span data-ttu-id="26dd8-129">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26dd8-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="26dd8-130">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26dd8-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="26dd8-131">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26dd8-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)

