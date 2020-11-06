---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 421bc74fb110aa48ff72388462e5496d9ceb1434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449010"
---
# <span data-ttu-id="4f90f-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4f90f-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4f90f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f90f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f90f-103">修改後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="4f90f-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f90f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f90f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f90f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f90f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f90f-106">AzureRmApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改後端 HTTP 設定物件的連接排出 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="4f90f-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4f90f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f90f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f90f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4f90f-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="4f90f-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4f90f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4f90f-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="4f90f-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="4f90f-111">最後一個命令會透過設定為 False 並 DrainTimeoutInSec 至3600，來修改儲存在 $Settings 中的後端 HTTP 設定物件的連接排出設定。</span><span class="sxs-lookup"><span data-stu-id="4f90f-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="4f90f-112">參數</span><span class="sxs-lookup"><span data-stu-id="4f90f-112">PARAMETERS</span></span>

### <span data-ttu-id="4f90f-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4f90f-113">-BackendHttpSettings</span></span>
<span data-ttu-id="4f90f-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="4f90f-114">The backend http settings</span></span>

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

### <span data-ttu-id="4f90f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f90f-115">-DefaultProfile</span></span>
<span data-ttu-id="4f90f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f90f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f90f-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="4f90f-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="4f90f-118">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="4f90f-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="4f90f-119">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="4f90f-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="4f90f-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="4f90f-120">-Enabled</span></span>
<span data-ttu-id="4f90f-121">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="4f90f-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="4f90f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f90f-122">CommonParameters</span></span>
<span data-ttu-id="4f90f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f90f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f90f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f90f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f90f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4f90f-125">INPUTS</span></span>

### <span data-ttu-id="4f90f-126">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f90f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="4f90f-127">參數： BackendHttpSettings (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4f90f-127">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="4f90f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4f90f-128">OUTPUTS</span></span>

### <span data-ttu-id="4f90f-129">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f90f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4f90f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4f90f-130">NOTES</span></span>

## <span data-ttu-id="4f90f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f90f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f90f-132">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f90f-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="4f90f-133">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4f90f-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="4f90f-134">AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4f90f-134">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4f90f-135">新-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4f90f-135">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4f90f-136">移除-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4f90f-136">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

