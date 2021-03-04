---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913505"
---
# <span data-ttu-id="0f9e2-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0f9e2-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0f9e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9e2-103">獲得後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0f9e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f9e2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f9e2-105">描述</span><span class="sxs-lookup"><span data-stu-id="0f9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="0f9e2-106">**Get-AzApplicationGatewayConnectionDraining Cmdlet** 會取得後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0f9e2-107">例子</span><span class="sxs-lookup"><span data-stu-id="0f9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="0f9e2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0f9e2-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="0f9e2-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0f9e2-110">第二個命令會獲得名為 Settings01 的後端 HTTP 設定，$AppGw將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0f9e2-111">最後一個命令會從後端 HTTP 設定中將連接耗用設定$Settings並儲存在$ConnectionDraining變數中。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="0f9e2-112">參數</span><span class="sxs-lookup"><span data-stu-id="0f9e2-112">PARAMETERS</span></span>

### <span data-ttu-id="0f9e2-113">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="0f9e2-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0f9e2-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="0f9e2-114">The backend http settings</span></span>

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

### <span data-ttu-id="0f9e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9e2-115">-DefaultProfile</span></span>
<span data-ttu-id="0f9e2-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f9e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9e2-117">CommonParameters</span></span>
<span data-ttu-id="0f9e2-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f9e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9e2-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f9e2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9e2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0f9e2-120">INPUTS</span></span>

### <span data-ttu-id="0f9e2-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0f9e2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0f9e2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0f9e2-122">OUTPUTS</span></span>

### <span data-ttu-id="0f9e2-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0f9e2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0f9e2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0f9e2-124">NOTES</span></span>

## <span data-ttu-id="0f9e2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f9e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="0f9e2-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f9e2-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0f9e2-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0f9e2-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0f9e2-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0f9e2-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0f9e2-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0f9e2-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0f9e2-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0f9e2-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
