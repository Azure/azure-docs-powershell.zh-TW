---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625790"
---
# <span data-ttu-id="7afb0-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7afb0-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7afb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7afb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7afb0-103">從應用程式閘道 (s) 取得自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="7afb0-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7afb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="7afb0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7afb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="7afb0-105">DESCRIPTION</span></span>
<span data-ttu-id="7afb0-106">**AzureRmApplicationGatewayCustomError** Cmdlet 會從應用程式閘道)  (s 中取得自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="7afb0-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="7afb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="7afb0-107">EXAMPLES</span></span>

### <span data-ttu-id="7afb0-108">範例1：在應用程式閘道中取得自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="7afb0-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="7afb0-109">這個命令會從應用程式閘道 $appgw 取得並傳回 HTTP 狀態碼502的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="7afb0-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="7afb0-110">範例2：取得應用程式閘道中所有自訂錯誤的清單</span><span class="sxs-lookup"><span data-stu-id="7afb0-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="7afb0-111">這個命令會從應用程式閘道 $appgw 取得並傳回所有自訂錯誤的清單。</span><span class="sxs-lookup"><span data-stu-id="7afb0-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="7afb0-112">參數</span><span class="sxs-lookup"><span data-stu-id="7afb0-112">PARAMETERS</span></span>

### <span data-ttu-id="7afb0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7afb0-113">-ApplicationGateway</span></span>
<span data-ttu-id="7afb0-114">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="7afb0-114">The Application Gateway</span></span>

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

### <span data-ttu-id="7afb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afb0-115">-DefaultProfile</span></span>
<span data-ttu-id="7afb0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7afb0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afb0-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7afb0-117">-StatusCode</span></span>
<span data-ttu-id="7afb0-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7afb0-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7afb0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afb0-119">CommonParameters</span></span>
<span data-ttu-id="7afb0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7afb0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afb0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7afb0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afb0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7afb0-122">INPUTS</span></span>

### <span data-ttu-id="7afb0-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7afb0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7afb0-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7afb0-124">OUTPUTS</span></span>

### <span data-ttu-id="7afb0-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7afb0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7afb0-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7afb0-126">NOTES</span></span>

## <span data-ttu-id="7afb0-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7afb0-127">RELATED LINKS</span></span>