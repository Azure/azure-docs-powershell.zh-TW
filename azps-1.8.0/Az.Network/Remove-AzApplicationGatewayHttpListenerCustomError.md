---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8a0ce9d3e2c2a5272f6544b5c98ef763b9b288ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621658"
---
# <span data-ttu-id="7eae2-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7eae2-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7eae2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eae2-102">SYNOPSIS</span></span>
<span data-ttu-id="7eae2-103">從應用程式閘道的 HTTP 攔截器中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="7eae2-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7eae2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eae2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eae2-105">說明</span><span class="sxs-lookup"><span data-stu-id="7eae2-105">DESCRIPTION</span></span>
<span data-ttu-id="7eae2-106">**AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道的 HTTP 攔截器中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="7eae2-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7eae2-107">示例</span><span class="sxs-lookup"><span data-stu-id="7eae2-107">EXAMPLES</span></span>

### <span data-ttu-id="7eae2-108">範例1：移除來自 HTTP 偵聽程式的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="7eae2-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="7eae2-109">這個命令會從 HTTP 偵聽程式 $listener 01 中移除 HTTP 狀態碼502的自訂錯誤，並傳回更新的監聽程式。</span><span class="sxs-lookup"><span data-stu-id="7eae2-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="7eae2-110">參數</span><span class="sxs-lookup"><span data-stu-id="7eae2-110">PARAMETERS</span></span>

### <span data-ttu-id="7eae2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eae2-111">-DefaultProfile</span></span>
<span data-ttu-id="7eae2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7eae2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eae2-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7eae2-113">-HttpListener</span></span>
<span data-ttu-id="7eae2-114">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="7eae2-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="7eae2-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7eae2-115">-StatusCode</span></span>
<span data-ttu-id="7eae2-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7eae2-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eae2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eae2-117">CommonParameters</span></span>
<span data-ttu-id="7eae2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eae2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eae2-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7eae2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eae2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7eae2-120">INPUTS</span></span>

### <span data-ttu-id="7eae2-121">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7eae2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7eae2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="7eae2-122">OUTPUTS</span></span>

### <span data-ttu-id="7eae2-123">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7eae2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7eae2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="7eae2-124">NOTES</span></span>

## <span data-ttu-id="7eae2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eae2-125">RELATED LINKS</span></span>

[<span data-ttu-id="7eae2-126">附加 AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7eae2-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7eae2-127">AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7eae2-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7eae2-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7eae2-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
