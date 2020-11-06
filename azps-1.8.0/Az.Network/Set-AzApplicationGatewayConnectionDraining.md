---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: d04dc0c3d9d446941870f30578f50d5ecd795009
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621511"
---
# <span data-ttu-id="a5f6d-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a5f6d-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="a5f6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f6d-103">修改後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="a5f6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5f6d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5f6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f6d-106">AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改後端 HTTP 設定物件的連接排出 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="a5f6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5f6d-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f6d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a5f6d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="a5f6d-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a5f6d-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="a5f6d-111">最後一個命令會透過設定為 False 並 DrainTimeoutInSec 至3600，來修改儲存在 $Settings 中的後端 HTTP 設定物件的連接排出設定。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="a5f6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="a5f6d-112">PARAMETERS</span></span>

### <span data-ttu-id="a5f6d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5f6d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="a5f6d-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="a5f6d-114">The backend http settings</span></span>

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

### <span data-ttu-id="a5f6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f6d-115">-DefaultProfile</span></span>
<span data-ttu-id="a5f6d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f6d-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="a5f6d-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="a5f6d-118">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="a5f6d-119">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f6d-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="a5f6d-120">-Enabled</span></span>
<span data-ttu-id="a5f6d-121">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f6d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f6d-122">CommonParameters</span></span>
<span data-ttu-id="a5f6d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f6d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5f6d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f6d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a5f6d-125">INPUTS</span></span>

### <span data-ttu-id="a5f6d-126">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a5f6d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a5f6d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a5f6d-127">OUTPUTS</span></span>

### <span data-ttu-id="a5f6d-128">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a5f6d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a5f6d-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a5f6d-129">NOTES</span></span>

## <span data-ttu-id="a5f6d-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5f6d-130">RELATED LINKS</span></span>

[<span data-ttu-id="a5f6d-131">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5f6d-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="a5f6d-132">AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5f6d-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="a5f6d-133">AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a5f6d-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a5f6d-134">新-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a5f6d-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a5f6d-135">移除-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a5f6d-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

