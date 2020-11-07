---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800401"
---
# <span data-ttu-id="75a79-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75a79-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="75a79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a79-102">SYNOPSIS</span></span>
<span data-ttu-id="75a79-103">從應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="75a79-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a79-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a79-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a79-105">說明</span><span class="sxs-lookup"><span data-stu-id="75a79-105">DESCRIPTION</span></span>
<span data-ttu-id="75a79-106">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會從 Azure 應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="75a79-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="75a79-107">示例</span><span class="sxs-lookup"><span data-stu-id="75a79-107">EXAMPLES</span></span>

### <span data-ttu-id="75a79-108">範例1：從應用程式閘道移除要求路由規則</span><span class="sxs-lookup"><span data-stu-id="75a79-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="75a79-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="75a79-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="75a79-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 Rule02 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="75a79-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="75a79-111">參數</span><span class="sxs-lookup"><span data-stu-id="75a79-111">PARAMETERS</span></span>

### <span data-ttu-id="75a79-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75a79-112">-ApplicationGateway</span></span>
<span data-ttu-id="75a79-113">指定要移除要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="75a79-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a79-114">-DefaultProfile</span></span>
<span data-ttu-id="75a79-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75a79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a79-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="75a79-116">-Name</span></span>
<span data-ttu-id="75a79-117">指定此 Cmdlet 移除之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a79-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="75a79-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a79-118">CommonParameters</span></span>
<span data-ttu-id="75a79-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a79-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a79-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75a79-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a79-121">輸入</span><span class="sxs-lookup"><span data-stu-id="75a79-121">INPUTS</span></span>

### <span data-ttu-id="75a79-122">System.object</span><span class="sxs-lookup"><span data-stu-id="75a79-122">System.String</span></span>

## <span data-ttu-id="75a79-123">輸出</span><span class="sxs-lookup"><span data-stu-id="75a79-123">OUTPUTS</span></span>

### <span data-ttu-id="75a79-124">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75a79-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="75a79-125">筆記</span><span class="sxs-lookup"><span data-stu-id="75a79-125">NOTES</span></span>

## <span data-ttu-id="75a79-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a79-126">RELATED LINKS</span></span>

[<span data-ttu-id="75a79-127">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75a79-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="75a79-128">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75a79-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="75a79-129">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75a79-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="75a79-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75a79-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


