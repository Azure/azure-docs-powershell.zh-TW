---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138703"
---
# <span data-ttu-id="66828-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="66828-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="66828-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66828-102">SYNOPSIS</span></span>
<span data-ttu-id="66828-103">移除後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="66828-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="66828-104">句法</span><span class="sxs-lookup"><span data-stu-id="66828-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66828-105">說明</span><span class="sxs-lookup"><span data-stu-id="66828-105">DESCRIPTION</span></span>
<span data-ttu-id="66828-106">**AzApplicationGatewayConnectionDraining** Cmdlet 會移除後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="66828-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="66828-107">示例</span><span class="sxs-lookup"><span data-stu-id="66828-107">EXAMPLES</span></span>

### <span data-ttu-id="66828-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66828-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="66828-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="66828-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66828-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="66828-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="66828-111">最後一個命令會移除 $Settings 中儲存後端 HTTP 設定的連接排出設定。</span><span class="sxs-lookup"><span data-stu-id="66828-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="66828-112">參數</span><span class="sxs-lookup"><span data-stu-id="66828-112">PARAMETERS</span></span>

### <span data-ttu-id="66828-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="66828-113">-BackendHttpSettings</span></span>
<span data-ttu-id="66828-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="66828-114">The backend http settings</span></span>

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

### <span data-ttu-id="66828-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66828-115">-DefaultProfile</span></span>
<span data-ttu-id="66828-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66828-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66828-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66828-117">CommonParameters</span></span>
<span data-ttu-id="66828-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66828-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66828-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66828-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66828-120">輸入</span><span class="sxs-lookup"><span data-stu-id="66828-120">INPUTS</span></span>

### <span data-ttu-id="66828-121">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66828-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="66828-122">輸出</span><span class="sxs-lookup"><span data-stu-id="66828-122">OUTPUTS</span></span>

### <span data-ttu-id="66828-123">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66828-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="66828-124">筆記</span><span class="sxs-lookup"><span data-stu-id="66828-124">NOTES</span></span>

## <span data-ttu-id="66828-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="66828-125">RELATED LINKS</span></span>

[<span data-ttu-id="66828-126">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66828-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="66828-127">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="66828-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="66828-128">AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="66828-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="66828-129">新-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="66828-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="66828-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="66828-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
