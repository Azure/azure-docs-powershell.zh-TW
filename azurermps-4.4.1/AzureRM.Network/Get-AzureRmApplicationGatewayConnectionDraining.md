---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 78c3a151f066d8ff05e92798ebad822943816af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446751"
---
# <span data-ttu-id="4e98a-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4e98a-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4e98a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e98a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e98a-103">取得後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="4e98a-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e98a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e98a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e98a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e98a-105">DESCRIPTION</span></span>
<span data-ttu-id="4e98a-106">**AzureRmApplicationGatewayConnectionDraining** Cmdlet 會取得後端 HTTP 設定物件的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="4e98a-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4e98a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e98a-107">EXAMPLES</span></span>

### <span data-ttu-id="4e98a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e98a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="4e98a-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4e98a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4e98a-110">第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="4e98a-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="4e98a-111">最後一個命令會從後端 HTTP 設定中取得連接排出配置 $Settings 並將它儲存在 $ConnectionDraining 變數中。</span><span class="sxs-lookup"><span data-stu-id="4e98a-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="4e98a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e98a-112">PARAMETERS</span></span>

### <span data-ttu-id="4e98a-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e98a-113">-BackendHttpSettings</span></span>
<span data-ttu-id="4e98a-114">後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="4e98a-114">The backend http settings</span></span>

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

### <span data-ttu-id="4e98a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e98a-115">-DefaultProfile</span></span>
<span data-ttu-id="4e98a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e98a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e98a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e98a-117">CommonParameters</span></span>
<span data-ttu-id="4e98a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e98a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e98a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e98a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e98a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4e98a-120">INPUTS</span></span>

### <span data-ttu-id="4e98a-121">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e98a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4e98a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4e98a-122">OUTPUTS</span></span>

### <span data-ttu-id="4e98a-123">PSApplicationGatewayConnectionDraining 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e98a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4e98a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4e98a-124">NOTES</span></span>

## <span data-ttu-id="4e98a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e98a-125">RELATED LINKS</span></span>

[<span data-ttu-id="4e98a-126">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e98a-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="4e98a-127">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e98a-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="4e98a-128">新-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4e98a-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4e98a-129">移除-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4e98a-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4e98a-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4e98a-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
