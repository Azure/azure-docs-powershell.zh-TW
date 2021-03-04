---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914746"
---
# <span data-ttu-id="3ad1a-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="3ad1a-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="3ad1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ad1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad1a-103">將身分識別指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3ad1a-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="3ad1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ad1a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ad1a-105">描述</span><span class="sxs-lookup"><span data-stu-id="3ad1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad1a-106">**Get-AzApplicationGatewayIdentity** Cmdlet 會指派身分識別至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3ad1a-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="3ad1a-107">例子</span><span class="sxs-lookup"><span data-stu-id="3ad1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ad1a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3ad1a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="3ad1a-109">此範例顯示如何從應用程式閘道取得應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="3ad1a-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="3ad1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ad1a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ad1a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ad1a-111">-ApplicationGateway</span></span>
<span data-ttu-id="3ad1a-112">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="3ad1a-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad1a-113">-DefaultProfile</span></span>
<span data-ttu-id="3ad1a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ad1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad1a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad1a-115">CommonParameters</span></span>
<span data-ttu-id="3ad1a-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ad1a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad1a-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ad1a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad1a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="3ad1a-118">INPUTS</span></span>

### <span data-ttu-id="3ad1a-119">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ad1a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ad1a-120">輸出</span><span class="sxs-lookup"><span data-stu-id="3ad1a-120">OUTPUTS</span></span>

### <span data-ttu-id="3ad1a-121">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3ad1a-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="3ad1a-122">筆記</span><span class="sxs-lookup"><span data-stu-id="3ad1a-122">NOTES</span></span>

## <span data-ttu-id="3ad1a-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ad1a-123">RELATED LINKS</span></span>
