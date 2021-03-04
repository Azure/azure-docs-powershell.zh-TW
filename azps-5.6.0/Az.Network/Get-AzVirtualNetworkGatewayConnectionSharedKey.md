---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 14a77eeaeb502c79663f9d95cbff3ffc199ddc67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907625"
---
# <span data-ttu-id="6cdb6-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cdb6-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6cdb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6cdb6-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdb6-103">顯示用於連接的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="6cdb6-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="6cdb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="6cdb6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cdb6-105">描述</span><span class="sxs-lookup"><span data-stu-id="6cdb6-105">DESCRIPTION</span></span>
<span data-ttu-id="6cdb6-106">顯示用於連接的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="6cdb6-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="6cdb6-107">例子</span><span class="sxs-lookup"><span data-stu-id="6cdb6-107">EXAMPLES</span></span>

### <span data-ttu-id="6cdb6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6cdb6-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="6cdb6-109">參數</span><span class="sxs-lookup"><span data-stu-id="6cdb6-109">PARAMETERS</span></span>

### <span data-ttu-id="6cdb6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdb6-110">-DefaultProfile</span></span>
<span data-ttu-id="6cdb6-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cdb6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cdb6-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cdb6-112">-Name</span></span>
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

### <span data-ttu-id="6cdb6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdb6-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6cdb6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdb6-114">CommonParameters</span></span>
<span data-ttu-id="6cdb6-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6cdb6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdb6-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cdb6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdb6-117">輸入</span><span class="sxs-lookup"><span data-stu-id="6cdb6-117">INPUTS</span></span>

### <span data-ttu-id="6cdb6-118">System.String</span><span class="sxs-lookup"><span data-stu-id="6cdb6-118">System.String</span></span>

## <span data-ttu-id="6cdb6-119">輸出</span><span class="sxs-lookup"><span data-stu-id="6cdb6-119">OUTPUTS</span></span>

### <span data-ttu-id="6cdb6-120">System.String</span><span class="sxs-lookup"><span data-stu-id="6cdb6-120">System.String</span></span>

## <span data-ttu-id="6cdb6-121">筆記</span><span class="sxs-lookup"><span data-stu-id="6cdb6-121">NOTES</span></span>

## <span data-ttu-id="6cdb6-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cdb6-122">RELATED LINKS</span></span>

[<span data-ttu-id="6cdb6-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cdb6-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6cdb6-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6cdb6-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
