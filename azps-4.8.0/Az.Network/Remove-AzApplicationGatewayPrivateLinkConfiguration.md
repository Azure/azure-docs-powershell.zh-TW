---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970892"
---
# <span data-ttu-id="a4b61-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b61-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a4b61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4b61-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b61-103">從應用程式閘道移除 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a4b61-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="a4b61-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4b61-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b61-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4b61-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b61-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會從 Azure 應用程式閘道中移除 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a4b61-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="a4b61-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4b61-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b61-108">範例1：移除應用程式閘道 PrivateLink 設定</span><span class="sxs-lookup"><span data-stu-id="a4b61-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="a4b61-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a4b61-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a4b61-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 privateLinkConfig01 的 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a4b61-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a4b61-111">參數</span><span class="sxs-lookup"><span data-stu-id="a4b61-111">PARAMETERS</span></span>

### <span data-ttu-id="a4b61-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4b61-112">-ApplicationGateway</span></span>
<span data-ttu-id="a4b61-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4b61-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b61-114">-DefaultProfile</span></span>
<span data-ttu-id="a4b61-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4b61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b61-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4b61-116">-Name</span></span>
<span data-ttu-id="a4b61-117">應用程式閘道 privateLink 設定的名稱</span><span class="sxs-lookup"><span data-stu-id="a4b61-117">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b61-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b61-118">CommonParameters</span></span>
<span data-ttu-id="a4b61-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4b61-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b61-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4b61-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b61-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a4b61-121">INPUTS</span></span>

### <span data-ttu-id="a4b61-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a4b61-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4b61-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a4b61-123">OUTPUTS</span></span>

### <span data-ttu-id="a4b61-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a4b61-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4b61-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a4b61-125">NOTES</span></span>

## <span data-ttu-id="a4b61-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4b61-126">RELATED LINKS</span></span>

[<span data-ttu-id="a4b61-127">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b61-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a4b61-128">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b61-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a4b61-129">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b61-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a4b61-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b61-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)