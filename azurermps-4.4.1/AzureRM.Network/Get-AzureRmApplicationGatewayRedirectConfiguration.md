---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623653"
---
# <span data-ttu-id="66c4d-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="66c4d-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="66c4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="66c4d-103">從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="66c4d-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66c4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="66c4d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="66c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="66c4d-106">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="66c4d-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="66c4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="66c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="66c4d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66c4d-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="66c4d-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="66c4d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="66c4d-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道取得名為 Redirect01 的重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="66c4d-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="66c4d-111">參數</span><span class="sxs-lookup"><span data-stu-id="66c4d-111">PARAMETERS</span></span>

### <span data-ttu-id="66c4d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66c4d-112">-ApplicationGateway</span></span>
<span data-ttu-id="66c4d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66c4d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="66c4d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="66c4d-114">-Name</span></span>
<span data-ttu-id="66c4d-115">要求路由規則的名稱</span><span class="sxs-lookup"><span data-stu-id="66c4d-115">The name of the request routing rule</span></span>

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

### <span data-ttu-id="66c4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c4d-116">-DefaultProfile</span></span>
<span data-ttu-id="66c4d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66c4d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c4d-118">CommonParameters</span></span>
<span data-ttu-id="66c4d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66c4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c4d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66c4d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c4d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="66c4d-121">INPUTS</span></span>

### <span data-ttu-id="66c4d-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66c4d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66c4d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="66c4d-123">OUTPUTS</span></span>

### <span data-ttu-id="66c4d-124">PSApplicationGatewayRedirectConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66c4d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="66c4d-125">[System.object]. IEnumerable "1 [PSApplicationGatewayRedirectConfiguration，4.1.0.0，network，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="66c4d-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="66c4d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="66c4d-126">NOTES</span></span>

## <span data-ttu-id="66c4d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="66c4d-127">RELATED LINKS</span></span>

