---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126970"
---
# <span data-ttu-id="43474-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43474-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="43474-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43474-102">SYNOPSIS</span></span>
<span data-ttu-id="43474-103">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="43474-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="43474-104">句法</span><span class="sxs-lookup"><span data-stu-id="43474-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43474-105">說明</span><span class="sxs-lookup"><span data-stu-id="43474-105">DESCRIPTION</span></span>
<span data-ttu-id="43474-106">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="43474-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="43474-107">示例</span><span class="sxs-lookup"><span data-stu-id="43474-107">EXAMPLES</span></span>

### <span data-ttu-id="43474-108">範例1</span><span class="sxs-lookup"><span data-stu-id="43474-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="43474-109">參數</span><span class="sxs-lookup"><span data-stu-id="43474-109">PARAMETERS</span></span>

### <span data-ttu-id="43474-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43474-110">-DefaultProfile</span></span>
<span data-ttu-id="43474-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43474-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43474-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="43474-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43474-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43474-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43474-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43474-114">CommonParameters</span></span>
<span data-ttu-id="43474-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43474-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43474-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43474-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43474-117">輸入</span><span class="sxs-lookup"><span data-stu-id="43474-117">INPUTS</span></span>

### <span data-ttu-id="43474-118">System.object</span><span class="sxs-lookup"><span data-stu-id="43474-118">System.String</span></span>

## <span data-ttu-id="43474-119">輸出</span><span class="sxs-lookup"><span data-stu-id="43474-119">OUTPUTS</span></span>

### <span data-ttu-id="43474-120">System.object</span><span class="sxs-lookup"><span data-stu-id="43474-120">System.String</span></span>

## <span data-ttu-id="43474-121">筆記</span><span class="sxs-lookup"><span data-stu-id="43474-121">NOTES</span></span>

## <span data-ttu-id="43474-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="43474-122">RELATED LINKS</span></span>

[<span data-ttu-id="43474-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43474-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="43474-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43474-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
