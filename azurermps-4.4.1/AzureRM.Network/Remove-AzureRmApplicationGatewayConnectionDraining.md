---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 12667316df99e19fbc0535a2b5e3fca3082d4484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446716"
---
# <span data-ttu-id="ec2c3-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec2c3-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ec2c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2c3-103">移除後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec2c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec2c3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec2c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2c3-106">**AzureRmApplicationGatewayConnectionDraining** Cmdlet 會移除後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ec2c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec2c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ec2c3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ec2c3-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ec2c3-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec2c3-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ec2c3-111">最後一個命令會移除 $Settings 中儲存後端 HTTP 設定的連接排出設定。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="ec2c3-112">參數</span><span class="sxs-lookup"><span data-stu-id="ec2c3-112">PARAMETERS</span></span>

### <span data-ttu-id="ec2c3-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec2c3-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ec2c3-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="ec2c3-114">The backend http settings</span></span>

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

### <span data-ttu-id="ec2c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c3-115">-DefaultProfile</span></span>
<span data-ttu-id="ec2c3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec2c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2c3-117">CommonParameters</span></span>
<span data-ttu-id="ec2c3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2c3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec2c3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2c3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ec2c3-120">INPUTS</span></span>

### <span data-ttu-id="ec2c3-121">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec2c3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ec2c3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ec2c3-122">OUTPUTS</span></span>

### <span data-ttu-id="ec2c3-123">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec2c3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ec2c3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ec2c3-124">NOTES</span></span>

## <span data-ttu-id="ec2c3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec2c3-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec2c3-126">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec2c3-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ec2c3-127">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec2c3-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="ec2c3-128">AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec2c3-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ec2c3-129">新-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec2c3-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ec2c3-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec2c3-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

