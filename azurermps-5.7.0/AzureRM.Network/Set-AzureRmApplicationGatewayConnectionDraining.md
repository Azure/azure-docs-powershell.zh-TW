---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3fe3d07a40f81c22fba39aee0db2eb0a2da6e788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455363"
---
# <span data-ttu-id="1ec96-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1ec96-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="1ec96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ec96-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec96-103">修改後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="1ec96-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec96-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ec96-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec96-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ec96-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec96-106">AzureRmApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 會修改後端 HTTP 設定物件的連接排出 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="1ec96-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="1ec96-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ec96-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec96-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1ec96-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="1ec96-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1ec96-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ec96-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="1ec96-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="1ec96-111">最後一個命令會透過設定為 False 並 DrainTimeoutInSec 至3600，來修改儲存在 $Settings 中的後端 HTTP 設定物件的連接排出設定。</span><span class="sxs-lookup"><span data-stu-id="1ec96-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="1ec96-112">參數</span><span class="sxs-lookup"><span data-stu-id="1ec96-112">PARAMETERS</span></span>

### <span data-ttu-id="1ec96-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1ec96-113">-BackendHttpSettings</span></span>
<span data-ttu-id="1ec96-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="1ec96-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec96-115">-DefaultProfile</span></span>
<span data-ttu-id="1ec96-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec96-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="1ec96-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="1ec96-118">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="1ec96-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="1ec96-119">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="1ec96-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec96-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="1ec96-120">-Enabled</span></span>
<span data-ttu-id="1ec96-121">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="1ec96-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec96-122">CommonParameters</span></span>
<span data-ttu-id="1ec96-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ec96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec96-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ec96-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec96-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec96-125">INPUTS</span></span>

### <span data-ttu-id="1ec96-126">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ec96-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1ec96-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec96-127">OUTPUTS</span></span>

### <span data-ttu-id="1ec96-128">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ec96-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1ec96-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec96-129">NOTES</span></span>

## <span data-ttu-id="1ec96-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec96-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ec96-131">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ec96-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="1ec96-132">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1ec96-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="1ec96-133">AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1ec96-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="1ec96-134">新-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1ec96-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="1ec96-135">移除-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1ec96-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

