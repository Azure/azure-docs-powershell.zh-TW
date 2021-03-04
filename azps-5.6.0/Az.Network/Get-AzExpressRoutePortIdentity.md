---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: a64bbe0dfad8e9e82138c50e6ff436a445f68392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903177"
---
# <span data-ttu-id="44acc-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="44acc-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="44acc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44acc-102">SYNOPSIS</span></span>
<span data-ttu-id="44acc-103">將身分識別指派給 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="44acc-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="44acc-104">語法</span><span class="sxs-lookup"><span data-stu-id="44acc-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44acc-105">描述</span><span class="sxs-lookup"><span data-stu-id="44acc-105">DESCRIPTION</span></span>
<span data-ttu-id="44acc-106">**Get-AzExpressRoutePortIdentity Cmdlet** 會指派身分識別給本地 Azure ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="44acc-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="44acc-107">例子</span><span class="sxs-lookup"><span data-stu-id="44acc-107">EXAMPLES</span></span>

### <span data-ttu-id="44acc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="44acc-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="44acc-109">參數</span><span class="sxs-lookup"><span data-stu-id="44acc-109">PARAMETERS</span></span>

### <span data-ttu-id="44acc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44acc-110">-DefaultProfile</span></span>
<span data-ttu-id="44acc-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44acc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44acc-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44acc-112">-ExpressRoutePort</span></span>
<span data-ttu-id="44acc-113">ExpressRoute 埠</span><span class="sxs-lookup"><span data-stu-id="44acc-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44acc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44acc-114">CommonParameters</span></span>
<span data-ttu-id="44acc-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44acc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44acc-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44acc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44acc-117">輸入</span><span class="sxs-lookup"><span data-stu-id="44acc-117">INPUTS</span></span>

### <span data-ttu-id="44acc-118">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="44acc-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="44acc-119">輸出</span><span class="sxs-lookup"><span data-stu-id="44acc-119">OUTPUTS</span></span>

### <span data-ttu-id="44acc-120">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="44acc-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="44acc-121">筆記</span><span class="sxs-lookup"><span data-stu-id="44acc-121">NOTES</span></span>

## <span data-ttu-id="44acc-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="44acc-122">RELATED LINKS</span></span>
[<span data-ttu-id="44acc-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="44acc-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="44acc-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="44acc-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="44acc-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="44acc-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)