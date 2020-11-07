---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 3c034f3bbbd5edc77fb6f43c291b8bf7ca27cd38
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794199"
---
# <span data-ttu-id="7fe19-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fe19-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7fe19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fe19-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe19-103">從應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="7fe19-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="7fe19-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fe19-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fe19-105">說明</span><span class="sxs-lookup"><span data-stu-id="7fe19-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe19-106">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會從 Azure 應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="7fe19-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="7fe19-107">示例</span><span class="sxs-lookup"><span data-stu-id="7fe19-107">EXAMPLES</span></span>

### <span data-ttu-id="7fe19-108">範例1：從應用程式閘道移除要求路由規則</span><span class="sxs-lookup"><span data-stu-id="7fe19-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="7fe19-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7fe19-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="7fe19-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 Rule02 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="7fe19-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7fe19-111">參數</span><span class="sxs-lookup"><span data-stu-id="7fe19-111">PARAMETERS</span></span>

### <span data-ttu-id="7fe19-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fe19-112">-ApplicationGateway</span></span>
<span data-ttu-id="7fe19-113">指定要移除要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7fe19-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="7fe19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe19-114">-DefaultProfile</span></span>
<span data-ttu-id="7fe19-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fe19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe19-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fe19-116">-Name</span></span>
<span data-ttu-id="7fe19-117">指定此 Cmdlet 移除之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe19-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="7fe19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe19-118">CommonParameters</span></span>
<span data-ttu-id="7fe19-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fe19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe19-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7fe19-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe19-121">輸入</span><span class="sxs-lookup"><span data-stu-id="7fe19-121">INPUTS</span></span>

### <span data-ttu-id="7fe19-122">System.object</span><span class="sxs-lookup"><span data-stu-id="7fe19-122">System.String</span></span>

## <span data-ttu-id="7fe19-123">輸出</span><span class="sxs-lookup"><span data-stu-id="7fe19-123">OUTPUTS</span></span>

### <span data-ttu-id="7fe19-124">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7fe19-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7fe19-125">筆記</span><span class="sxs-lookup"><span data-stu-id="7fe19-125">NOTES</span></span>

## <span data-ttu-id="7fe19-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fe19-126">RELATED LINKS</span></span>

[<span data-ttu-id="7fe19-127">附加 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fe19-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7fe19-128">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fe19-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7fe19-129">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fe19-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7fe19-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fe19-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


