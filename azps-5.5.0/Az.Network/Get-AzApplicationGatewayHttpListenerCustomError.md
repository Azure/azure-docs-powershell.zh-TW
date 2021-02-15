---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131403"
---
# <span data-ttu-id="e3382-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e3382-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="e3382-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3382-102">SYNOPSIS</span></span>
<span data-ttu-id="e3382-103">從應用程式閘道的 HTTP 攔截器) 取得自訂錯誤 (s。</span><span class="sxs-lookup"><span data-stu-id="e3382-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="e3382-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3382-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3382-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3382-105">DESCRIPTION</span></span>
<span data-ttu-id="e3382-106">AzApplicationGatewayCustomError Cmdlet 會從應用程式閘道的 HTTP 攔截器) ， **取得** 自訂錯誤 (s。</span><span class="sxs-lookup"><span data-stu-id="e3382-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="e3382-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3382-107">EXAMPLES</span></span>

### <span data-ttu-id="e3382-108">範例1：在 HTTP 偵聽程式中取得自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="e3382-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="e3382-109">這個命令會從 HTTP 偵聽程式 $listener 01 中取得並傳回 HTTP 狀態碼502的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3382-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="e3382-110">範例2：取得 HTTP 偵聽程式中所有自訂錯誤的清單</span><span class="sxs-lookup"><span data-stu-id="e3382-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="e3382-111">這個命令會從 HTTP 偵聽程式 $listener 01 中取得並傳回所有自訂錯誤的清單。</span><span class="sxs-lookup"><span data-stu-id="e3382-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="e3382-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3382-112">PARAMETERS</span></span>

### <span data-ttu-id="e3382-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3382-113">-DefaultProfile</span></span>
<span data-ttu-id="e3382-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3382-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3382-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e3382-115">-HttpListener</span></span>
<span data-ttu-id="e3382-116">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="e3382-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="e3382-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e3382-117">-StatusCode</span></span>
<span data-ttu-id="e3382-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="e3382-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e3382-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3382-119">CommonParameters</span></span>
<span data-ttu-id="e3382-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3382-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3382-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3382-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3382-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e3382-122">INPUTS</span></span>

### <span data-ttu-id="e3382-123">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3382-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e3382-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e3382-124">OUTPUTS</span></span>

### <span data-ttu-id="e3382-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3382-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e3382-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e3382-126">NOTES</span></span>

## <span data-ttu-id="e3382-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3382-127">RELATED LINKS</span></span>

[<span data-ttu-id="e3382-128">附加 AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e3382-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e3382-129">移除-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e3382-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e3382-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e3382-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
