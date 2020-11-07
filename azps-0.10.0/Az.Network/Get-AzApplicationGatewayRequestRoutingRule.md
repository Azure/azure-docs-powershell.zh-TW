---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794463"
---
# <span data-ttu-id="e733e-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e733e-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e733e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e733e-102">SYNOPSIS</span></span>
<span data-ttu-id="e733e-103">取得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e733e-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="e733e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e733e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e733e-105">說明</span><span class="sxs-lookup"><span data-stu-id="e733e-105">DESCRIPTION</span></span>
<span data-ttu-id="e733e-106">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會取得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e733e-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="e733e-107">示例</span><span class="sxs-lookup"><span data-stu-id="e733e-107">EXAMPLES</span></span>

### <span data-ttu-id="e733e-108">範例1：取得特定的要求路由規則</span><span class="sxs-lookup"><span data-stu-id="e733e-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="e733e-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e733e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e733e-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道取得名為 Rule01 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e733e-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="e733e-111">範例2：取得要求路由規則清單</span><span class="sxs-lookup"><span data-stu-id="e733e-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="e733e-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e733e-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e733e-113">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="e733e-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="e733e-114">參數</span><span class="sxs-lookup"><span data-stu-id="e733e-114">PARAMETERS</span></span>

### <span data-ttu-id="e733e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e733e-115">-ApplicationGateway</span></span>
<span data-ttu-id="e733e-116">指定包含要求路由規則的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="e733e-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="e733e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e733e-117">-DefaultProfile</span></span>
<span data-ttu-id="e733e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e733e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e733e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e733e-119">-Name</span></span>
<span data-ttu-id="e733e-120">指定此 Cmdlet 取得的要求路由規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e733e-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e733e-121">CommonParameters</span></span>
<span data-ttu-id="e733e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e733e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e733e-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e733e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e733e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e733e-124">INPUTS</span></span>

### <span data-ttu-id="e733e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e733e-125">System.String</span></span>

## <span data-ttu-id="e733e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e733e-126">OUTPUTS</span></span>

### <span data-ttu-id="e733e-127">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e733e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e733e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e733e-128">NOTES</span></span>

## <span data-ttu-id="e733e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e733e-129">RELATED LINKS</span></span>

[<span data-ttu-id="e733e-130">附加 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e733e-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e733e-131">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e733e-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e733e-132">移除-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e733e-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e733e-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e733e-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


