---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446957"
---
# <span data-ttu-id="146ba-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="146ba-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="146ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="146ba-102">SYNOPSIS</span></span>
<span data-ttu-id="146ba-103">取得應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="146ba-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="146ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="146ba-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="146ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="146ba-105">DESCRIPTION</span></span>
<span data-ttu-id="146ba-106">**AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet 會取得應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="146ba-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="146ba-107">示例</span><span class="sxs-lookup"><span data-stu-id="146ba-107">EXAMPLES</span></span>

### <span data-ttu-id="146ba-108">範例1</span><span class="sxs-lookup"><span data-stu-id="146ba-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="146ba-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="146ba-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="146ba-110">第二個命令會從 applicationg 閘道提取自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="146ba-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="146ba-111">參數</span><span class="sxs-lookup"><span data-stu-id="146ba-111">PARAMETERS</span></span>

### <span data-ttu-id="146ba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="146ba-112">-ApplicationGateway</span></span>
<span data-ttu-id="146ba-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="146ba-113">The applicationGateway</span></span>

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

### <span data-ttu-id="146ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146ba-114">-DefaultProfile</span></span>
<span data-ttu-id="146ba-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="146ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="146ba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146ba-116">CommonParameters</span></span>
<span data-ttu-id="146ba-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="146ba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146ba-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="146ba-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146ba-119">輸入</span><span class="sxs-lookup"><span data-stu-id="146ba-119">INPUTS</span></span>

### <span data-ttu-id="146ba-120">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="146ba-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="146ba-121">輸出</span><span class="sxs-lookup"><span data-stu-id="146ba-121">OUTPUTS</span></span>

### <span data-ttu-id="146ba-122">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="146ba-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="146ba-123">筆記</span><span class="sxs-lookup"><span data-stu-id="146ba-123">NOTES</span></span>

## <span data-ttu-id="146ba-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="146ba-124">RELATED LINKS</span></span>
