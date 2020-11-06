---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e50917224ef791dbc85c24ceb79cfc7ce05f7d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622106"
---
# <span data-ttu-id="a8858-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a8858-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="a8858-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8858-102">SYNOPSIS</span></span>
<span data-ttu-id="a8858-103">取得後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="a8858-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="a8858-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8858-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8858-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8858-105">DESCRIPTION</span></span>
<span data-ttu-id="a8858-106">**AzApplicationGatewayConnectionDraining** Cmdlet 會取得後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="a8858-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="a8858-107">示例</span><span class="sxs-lookup"><span data-stu-id="a8858-107">EXAMPLES</span></span>

### <span data-ttu-id="a8858-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a8858-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="a8858-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a8858-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a8858-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="a8858-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="a8858-111">最後一個命令會從後端 HTTP 設定中取得連接排出配置 $Settings 並將它儲存在 $ConnectionDraining 變數中。</span><span class="sxs-lookup"><span data-stu-id="a8858-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="a8858-112">參數</span><span class="sxs-lookup"><span data-stu-id="a8858-112">PARAMETERS</span></span>

### <span data-ttu-id="a8858-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a8858-113">-BackendHttpSettings</span></span>
<span data-ttu-id="a8858-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="a8858-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8858-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8858-115">-DefaultProfile</span></span>
<span data-ttu-id="a8858-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8858-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8858-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8858-117">CommonParameters</span></span>
<span data-ttu-id="a8858-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8858-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8858-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a8858-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8858-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a8858-120">INPUTS</span></span>

### <span data-ttu-id="a8858-121">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a8858-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a8858-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a8858-122">OUTPUTS</span></span>

### <span data-ttu-id="a8858-123">PSApplicationGatewayConnectionDraining 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a8858-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="a8858-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a8858-124">NOTES</span></span>

## <span data-ttu-id="a8858-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8858-125">RELATED LINKS</span></span>

[<span data-ttu-id="a8858-126">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8858-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="a8858-127">AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a8858-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="a8858-128">新-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a8858-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a8858-129">移除-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a8858-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a8858-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a8858-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
