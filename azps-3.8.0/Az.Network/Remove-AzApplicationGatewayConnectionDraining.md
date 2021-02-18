---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 4b0eb6188f75b71e3e56107138b6d5e2f9fc7b93
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406068"
---
# <span data-ttu-id="fc356-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fc356-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="fc356-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc356-102">SYNOPSIS</span></span>
<span data-ttu-id="fc356-103">移除後端 HTTP 設定物件的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="fc356-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fc356-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc356-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc356-105">描述</span><span class="sxs-lookup"><span data-stu-id="fc356-105">DESCRIPTION</span></span>
<span data-ttu-id="fc356-106">**Remove-AzApplicationGatewayConnectionDraining Cmdlet** 會移除後端 HTTP 設定物件的連接消耗設定。</span><span class="sxs-lookup"><span data-stu-id="fc356-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fc356-107">例子</span><span class="sxs-lookup"><span data-stu-id="fc356-107">EXAMPLES</span></span>

### <span data-ttu-id="fc356-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fc356-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="fc356-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="fc356-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fc356-110">第二個命令會獲得名為 Settings01 的後端 HTTP 設定，$AppGw將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="fc356-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="fc356-111">最後一個命令會移除儲存在 $Settings 中的後端 HTTP 設定之連接消耗$Settings。</span><span class="sxs-lookup"><span data-stu-id="fc356-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="fc356-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc356-112">PARAMETERS</span></span>

### <span data-ttu-id="fc356-113">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="fc356-113">-BackendHttpSettings</span></span>
<span data-ttu-id="fc356-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="fc356-114">The backend http settings</span></span>

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

### <span data-ttu-id="fc356-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc356-115">-DefaultProfile</span></span>
<span data-ttu-id="fc356-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc356-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc356-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc356-117">CommonParameters</span></span>
<span data-ttu-id="fc356-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc356-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc356-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fc356-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc356-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fc356-120">INPUTS</span></span>

### <span data-ttu-id="fc356-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fc356-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fc356-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fc356-122">OUTPUTS</span></span>

### <span data-ttu-id="fc356-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fc356-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fc356-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fc356-124">NOTES</span></span>

## <span data-ttu-id="fc356-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc356-125">RELATED LINKS</span></span>

[<span data-ttu-id="fc356-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc356-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="fc356-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fc356-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fc356-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fc356-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fc356-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fc356-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

