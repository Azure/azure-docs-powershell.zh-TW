---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141406"
---
# <span data-ttu-id="028fa-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="028fa-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="028fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="028fa-102">SYNOPSIS</span></span>
<span data-ttu-id="028fa-103">取得指派給 ExpressRoutePort 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="028fa-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="028fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="028fa-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="028fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="028fa-105">DESCRIPTION</span></span>
<span data-ttu-id="028fa-106">**AzExpressRoutePortIdentity** Cmdlet 會取得指派給本機 Azure ExpressRoutePort 物件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="028fa-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="028fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="028fa-107">EXAMPLES</span></span>

### <span data-ttu-id="028fa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="028fa-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="028fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="028fa-109">PARAMETERS</span></span>

### <span data-ttu-id="028fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028fa-110">-DefaultProfile</span></span>
<span data-ttu-id="028fa-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="028fa-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="028fa-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="028fa-112">-ExpressRoutePort</span></span>
<span data-ttu-id="028fa-113">ExpressRoute 埠</span><span class="sxs-lookup"><span data-stu-id="028fa-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="028fa-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028fa-114">CommonParameters</span></span>
<span data-ttu-id="028fa-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="028fa-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028fa-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="028fa-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028fa-117">輸入</span><span class="sxs-lookup"><span data-stu-id="028fa-117">INPUTS</span></span>

### <span data-ttu-id="028fa-118">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="028fa-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="028fa-119">輸出</span><span class="sxs-lookup"><span data-stu-id="028fa-119">OUTPUTS</span></span>

### <span data-ttu-id="028fa-120">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="028fa-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="028fa-121">筆記</span><span class="sxs-lookup"><span data-stu-id="028fa-121">NOTES</span></span>

## <span data-ttu-id="028fa-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="028fa-122">RELATED LINKS</span></span>
[<span data-ttu-id="028fa-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="028fa-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="028fa-124">新-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="028fa-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="028fa-125">移除-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="028fa-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)