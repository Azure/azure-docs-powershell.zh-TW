---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 0bc3d62ad690ab8bed961045ce46448af8700bd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909574"
---
# <span data-ttu-id="c6d32-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="c6d32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6d32-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d32-103">新增私人連結組配置至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c6d32-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c6d32-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6d32-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6d32-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6d32-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d32-106">**Add-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會新增私人連結組配置至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c6d32-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c6d32-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6d32-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d32-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6d32-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="c6d32-109">第一個命令會建立 privateLinkIpConfiguration，並儲存在$PrivateLinkIpConfiguration變數中。</span><span class="sxs-lookup"><span data-stu-id="c6d32-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="c6d32-110">第二個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c6d32-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c6d32-111">第三個命令會新增名為 privateLinkConfig01 的私人連結組$AppGw</span><span class="sxs-lookup"><span data-stu-id="c6d32-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="c6d32-112">參數</span><span class="sxs-lookup"><span data-stu-id="c6d32-112">PARAMETERS</span></span>

### <span data-ttu-id="c6d32-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6d32-113">-ApplicationGateway</span></span>
<span data-ttu-id="c6d32-114">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="c6d32-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c6d32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d32-115">-DefaultProfile</span></span>
<span data-ttu-id="c6d32-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6d32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6d32-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-117">-IpConfiguration</span></span>
<span data-ttu-id="c6d32-118">ipConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="c6d32-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d32-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6d32-119">-Name</span></span>
<span data-ttu-id="c6d32-120">privateLink 組組的名稱</span><span class="sxs-lookup"><span data-stu-id="c6d32-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="c6d32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d32-121">CommonParameters</span></span>
<span data-ttu-id="c6d32-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6d32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d32-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6d32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d32-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c6d32-124">INPUTS</span></span>

### <span data-ttu-id="c6d32-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6d32-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="c6d32-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c6d32-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="c6d32-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c6d32-127">OUTPUTS</span></span>

### <span data-ttu-id="c6d32-128">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6d32-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c6d32-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c6d32-129">NOTES</span></span>

## <span data-ttu-id="c6d32-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6d32-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6d32-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c6d32-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c6d32-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c6d32-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d32-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)