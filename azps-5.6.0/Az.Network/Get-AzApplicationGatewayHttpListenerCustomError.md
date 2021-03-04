---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914758"
---
# <span data-ttu-id="53339-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="53339-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="53339-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53339-102">SYNOPSIS</span></span>
<span data-ttu-id="53339-103">從應用程式閘道 () 的 HTTP 聆聽者收到自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="53339-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="53339-104">語法</span><span class="sxs-lookup"><span data-stu-id="53339-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53339-105">描述</span><span class="sxs-lookup"><span data-stu-id="53339-105">DESCRIPTION</span></span>
<span data-ttu-id="53339-106">**Get-AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道的 HTTP () 取得自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="53339-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="53339-107">例子</span><span class="sxs-lookup"><span data-stu-id="53339-107">EXAMPLES</span></span>

### <span data-ttu-id="53339-108">範例 1：在 HTTP 聆聽者中收到自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="53339-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="53339-109">此命令會從 HTTP 聆聽程式 $listener 01 中，收到並返回 HTTP 狀態碼 502 的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="53339-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="53339-110">範例 2：在 HTTP 聆聽者中，獲得所有自訂錯誤的清單</span><span class="sxs-lookup"><span data-stu-id="53339-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="53339-111">此命令會從 HTTP 聆聽程式或網站中，獲得並$listener 01 的所有自訂錯誤清單。</span><span class="sxs-lookup"><span data-stu-id="53339-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="53339-112">參數</span><span class="sxs-lookup"><span data-stu-id="53339-112">PARAMETERS</span></span>

### <span data-ttu-id="53339-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53339-113">-DefaultProfile</span></span>
<span data-ttu-id="53339-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53339-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53339-115">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="53339-115">-HttpListener</span></span>
<span data-ttu-id="53339-116">應用程式閘道 HTTP Listener</span><span class="sxs-lookup"><span data-stu-id="53339-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53339-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="53339-117">-StatusCode</span></span>
<span data-ttu-id="53339-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="53339-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="53339-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53339-119">CommonParameters</span></span>
<span data-ttu-id="53339-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53339-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53339-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53339-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53339-122">輸入</span><span class="sxs-lookup"><span data-stu-id="53339-122">INPUTS</span></span>

### <span data-ttu-id="53339-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53339-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="53339-124">輸出</span><span class="sxs-lookup"><span data-stu-id="53339-124">OUTPUTS</span></span>

### <span data-ttu-id="53339-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="53339-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="53339-126">筆記</span><span class="sxs-lookup"><span data-stu-id="53339-126">NOTES</span></span>

## <span data-ttu-id="53339-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="53339-127">RELATED LINKS</span></span>

[<span data-ttu-id="53339-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="53339-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="53339-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="53339-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="53339-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="53339-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
