---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802397"
---
# <span data-ttu-id="34f16-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="34f16-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="34f16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34f16-102">SYNOPSIS</span></span>
<span data-ttu-id="34f16-103">從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="34f16-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34f16-104">句法</span><span class="sxs-lookup"><span data-stu-id="34f16-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f16-105">說明</span><span class="sxs-lookup"><span data-stu-id="34f16-105">DESCRIPTION</span></span>
<span data-ttu-id="34f16-106">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="34f16-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="34f16-107">示例</span><span class="sxs-lookup"><span data-stu-id="34f16-107">EXAMPLES</span></span>

### <span data-ttu-id="34f16-108">範例1</span><span class="sxs-lookup"><span data-stu-id="34f16-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="34f16-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="34f16-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="34f16-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道取得名為 Redirect01 的重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="34f16-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="34f16-111">參數</span><span class="sxs-lookup"><span data-stu-id="34f16-111">PARAMETERS</span></span>

### <span data-ttu-id="34f16-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34f16-112">-ApplicationGateway</span></span>
<span data-ttu-id="34f16-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34f16-113">The applicationGateway</span></span>

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

### <span data-ttu-id="34f16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f16-114">-DefaultProfile</span></span>
<span data-ttu-id="34f16-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34f16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f16-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="34f16-116">-Name</span></span>
<span data-ttu-id="34f16-117">要求路由規則的名稱</span><span class="sxs-lookup"><span data-stu-id="34f16-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="34f16-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f16-118">CommonParameters</span></span>
<span data-ttu-id="34f16-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34f16-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f16-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34f16-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f16-121">輸入</span><span class="sxs-lookup"><span data-stu-id="34f16-121">INPUTS</span></span>

### <span data-ttu-id="34f16-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34f16-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34f16-123">輸出</span><span class="sxs-lookup"><span data-stu-id="34f16-123">OUTPUTS</span></span>

### <span data-ttu-id="34f16-124">PSApplicationGatewayRedirectConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34f16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="34f16-125">[System.object]. IEnumerable "1 [PSApplicationGatewayRedirectConfiguration，4.1.0.0，network，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="34f16-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="34f16-126">筆記</span><span class="sxs-lookup"><span data-stu-id="34f16-126">NOTES</span></span>

## <span data-ttu-id="34f16-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="34f16-127">RELATED LINKS</span></span>

