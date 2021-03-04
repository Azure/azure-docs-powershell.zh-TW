---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 84a9ccb86f9fd1d4995ad52e913059181c0b887e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905869"
---
# <span data-ttu-id="3804a-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3804a-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="3804a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3804a-102">SYNOPSIS</span></span>
<span data-ttu-id="3804a-103">修改後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="3804a-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="3804a-104">語法</span><span class="sxs-lookup"><span data-stu-id="3804a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3804a-105">描述</span><span class="sxs-lookup"><span data-stu-id="3804a-105">DESCRIPTION</span></span>
<span data-ttu-id="3804a-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會修改後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="3804a-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="3804a-107">例子</span><span class="sxs-lookup"><span data-stu-id="3804a-107">EXAMPLES</span></span>

### <span data-ttu-id="3804a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3804a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="3804a-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="3804a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3804a-110">第二個命令會獲得名為 Settings01 的後端 HTTP 設定，$AppGw將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="3804a-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="3804a-111">最後一個命令將 Enabled to False 和 DrainTimeoutInSec 設定為 3600，來修改儲存在 $Settings 中的後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="3804a-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="3804a-112">參數</span><span class="sxs-lookup"><span data-stu-id="3804a-112">PARAMETERS</span></span>

### <span data-ttu-id="3804a-113">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="3804a-113">-BackendHttpSettings</span></span>
<span data-ttu-id="3804a-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="3804a-114">The backend http settings</span></span>

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

### <span data-ttu-id="3804a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3804a-115">-DefaultProfile</span></span>
<span data-ttu-id="3804a-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3804a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3804a-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="3804a-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="3804a-118">連接漏掉的秒數為使用中。</span><span class="sxs-lookup"><span data-stu-id="3804a-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="3804a-119">可接受的值為 1 秒到 3600 秒。</span><span class="sxs-lookup"><span data-stu-id="3804a-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="3804a-120">-已啟用</span><span class="sxs-lookup"><span data-stu-id="3804a-120">-Enabled</span></span>
<span data-ttu-id="3804a-121">是否已啟用連接耗用。</span><span class="sxs-lookup"><span data-stu-id="3804a-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="3804a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3804a-122">CommonParameters</span></span>
<span data-ttu-id="3804a-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3804a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3804a-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3804a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3804a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3804a-125">INPUTS</span></span>

### <span data-ttu-id="3804a-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3804a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="3804a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3804a-127">OUTPUTS</span></span>

### <span data-ttu-id="3804a-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3804a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="3804a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3804a-129">NOTES</span></span>

## <span data-ttu-id="3804a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3804a-130">RELATED LINKS</span></span>

[<span data-ttu-id="3804a-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3804a-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="3804a-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3804a-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="3804a-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3804a-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="3804a-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3804a-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="3804a-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3804a-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

