---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800785"
---
# <span data-ttu-id="a3b40-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3b40-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a3b40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3b40-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b40-103">為負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a3b40-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3b40-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3b40-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3b40-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3b40-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b40-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會為 Azure 負載平衡器建立後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a3b40-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a3b40-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3b40-107">EXAMPLES</span></span>

### <span data-ttu-id="a3b40-108">範例1：為負載平衡器建立後端位址集區配置</span><span class="sxs-lookup"><span data-stu-id="a3b40-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="a3b40-109">這個命令會為負載平衡器建立名為 BackendAddressPool02 的後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="a3b40-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="a3b40-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3b40-110">PARAMETERS</span></span>

### <span data-ttu-id="a3b40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b40-111">-DefaultProfile</span></span>
<span data-ttu-id="a3b40-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3b40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3b40-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3b40-113">-Name</span></span>
<span data-ttu-id="a3b40-114">指定要建立的位址集區配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a3b40-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="a3b40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b40-115">CommonParameters</span></span>
<span data-ttu-id="a3b40-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3b40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b40-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3b40-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b40-118">輸入</span><span class="sxs-lookup"><span data-stu-id="a3b40-118">INPUTS</span></span>

## <span data-ttu-id="a3b40-119">輸出</span><span class="sxs-lookup"><span data-stu-id="a3b40-119">OUTPUTS</span></span>

### <span data-ttu-id="a3b40-120">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3b40-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a3b40-121">筆記</span><span class="sxs-lookup"><span data-stu-id="a3b40-121">NOTES</span></span>

## <span data-ttu-id="a3b40-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3b40-122">RELATED LINKS</span></span>

[<span data-ttu-id="a3b40-123">附加 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3b40-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a3b40-124">AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3b40-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a3b40-125">移除-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3b40-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


