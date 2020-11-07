---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794278"
---
# <span data-ttu-id="f97e8-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f97e8-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f97e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f97e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f97e8-103">為負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="f97e8-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="f97e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f97e8-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f97e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="f97e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f97e8-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet 會為 Azure 負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="f97e8-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f97e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="f97e8-107">EXAMPLES</span></span>

### <span data-ttu-id="f97e8-108">範例1：為負載平衡器建立後端位址集區配置</span><span class="sxs-lookup"><span data-stu-id="f97e8-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="f97e8-109">這個命令會為負載平衡器建立名為 BackendAddressPool02 的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="f97e8-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="f97e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="f97e8-110">PARAMETERS</span></span>

### <span data-ttu-id="f97e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97e8-111">-DefaultProfile</span></span>
<span data-ttu-id="f97e8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f97e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97e8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f97e8-113">-Name</span></span>
<span data-ttu-id="f97e8-114">指定要建立的位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="f97e8-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97e8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97e8-115">CommonParameters</span></span>
<span data-ttu-id="f97e8-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f97e8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97e8-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f97e8-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97e8-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f97e8-118">INPUTS</span></span>

## <span data-ttu-id="f97e8-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f97e8-119">OUTPUTS</span></span>

### <span data-ttu-id="f97e8-120">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f97e8-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f97e8-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f97e8-121">NOTES</span></span>

## <span data-ttu-id="f97e8-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f97e8-122">RELATED LINKS</span></span>

[<span data-ttu-id="f97e8-123">附加 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f97e8-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f97e8-124">AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f97e8-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f97e8-125">移除-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f97e8-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


