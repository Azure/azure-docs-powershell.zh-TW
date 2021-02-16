---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135774"
---
# <span data-ttu-id="a87d7-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87d7-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a87d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a87d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a87d7-103">從應用程式閘道移除 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a87d7-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="a87d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a87d7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a87d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="a87d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a87d7-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會從 Azure 應用程式閘道中移除 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a87d7-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="a87d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="a87d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a87d7-108">範例1：移除應用程式閘道 PrivateLink 設定</span><span class="sxs-lookup"><span data-stu-id="a87d7-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="a87d7-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a87d7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a87d7-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 privateLinkConfig01 的 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="a87d7-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a87d7-111">參數</span><span class="sxs-lookup"><span data-stu-id="a87d7-111">PARAMETERS</span></span>

### <span data-ttu-id="a87d7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a87d7-112">-ApplicationGateway</span></span>
<span data-ttu-id="a87d7-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a87d7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a87d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87d7-114">-DefaultProfile</span></span>
<span data-ttu-id="a87d7-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a87d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a87d7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a87d7-116">-Name</span></span>
<span data-ttu-id="a87d7-117">應用程式閘道 privateLink 設定的名稱</span><span class="sxs-lookup"><span data-stu-id="a87d7-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="a87d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87d7-118">CommonParameters</span></span>
<span data-ttu-id="a87d7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a87d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87d7-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a87d7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87d7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a87d7-121">INPUTS</span></span>

### <span data-ttu-id="a87d7-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a87d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a87d7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a87d7-123">OUTPUTS</span></span>

### <span data-ttu-id="a87d7-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a87d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a87d7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a87d7-125">NOTES</span></span>

## <span data-ttu-id="a87d7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a87d7-126">RELATED LINKS</span></span>

[<span data-ttu-id="a87d7-127">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87d7-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a87d7-128">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87d7-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a87d7-129">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87d7-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a87d7-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87d7-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)