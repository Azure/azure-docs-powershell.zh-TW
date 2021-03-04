---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 459880d6ab771e48a9fe2d5ba69abffae35db7b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913501"
---
# <span data-ttu-id="b4285-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b4285-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4285-102">SYNOPSIS</span></span>
<span data-ttu-id="b4285-103">從應用程式閘道 (自訂) 自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="b4285-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="b4285-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4285-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4285-105">描述</span><span class="sxs-lookup"><span data-stu-id="b4285-105">DESCRIPTION</span></span>
<span data-ttu-id="b4285-106">**Get-AzApplicationGatewayCustomError** Cmdlet 會從 (閘道) 自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="b4285-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="b4285-107">例子</span><span class="sxs-lookup"><span data-stu-id="b4285-107">EXAMPLES</span></span>

### <span data-ttu-id="b4285-108">範例 1：在應用程式閘道中收到自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="b4285-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="b4285-109">此命令會從應用程式閘道或應用程式閘道中，收到並$appgw。</span><span class="sxs-lookup"><span data-stu-id="b4285-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="b4285-110">範例 2：在應用程式閘道中獲得所有自訂錯誤的清單</span><span class="sxs-lookup"><span data-stu-id="b4285-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="b4285-111">此命令會從應用程式閘道或應用程式閘道中，獲得並$appgw。</span><span class="sxs-lookup"><span data-stu-id="b4285-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="b4285-112">參數</span><span class="sxs-lookup"><span data-stu-id="b4285-112">PARAMETERS</span></span>

### <span data-ttu-id="b4285-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4285-113">-ApplicationGateway</span></span>
<span data-ttu-id="b4285-114">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="b4285-114">The Application Gateway</span></span>

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

### <span data-ttu-id="b4285-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4285-115">-DefaultProfile</span></span>
<span data-ttu-id="b4285-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4285-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4285-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b4285-117">-StatusCode</span></span>
<span data-ttu-id="b4285-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="b4285-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4285-119">CommonParameters</span></span>
<span data-ttu-id="b4285-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4285-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4285-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4285-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4285-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b4285-122">INPUTS</span></span>

### <span data-ttu-id="b4285-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4285-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4285-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b4285-124">OUTPUTS</span></span>

### <span data-ttu-id="b4285-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b4285-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b4285-126">NOTES</span></span>

## <span data-ttu-id="b4285-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4285-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4285-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4285-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4285-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4285-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4285-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
