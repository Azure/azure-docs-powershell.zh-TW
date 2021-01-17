---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448934"
---
# <span data-ttu-id="429f3-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="429f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="429f3-102">SYNOPSIS</span></span>
<span data-ttu-id="429f3-103">更新應用程式閘道的 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="429f3-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="429f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="429f3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="429f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="429f3-105">DESCRIPTION</span></span>
<span data-ttu-id="429f3-106">**AzApplicationGatewaySslProfile** Cmdlet 會更新 Azure 應用程式閘道的 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="429f3-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="429f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="429f3-107">EXAMPLES</span></span>

### <span data-ttu-id="429f3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="429f3-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="429f3-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="429f3-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="429f3-110">第二個命令會更新 $AppGw 變數中應用程式閘道的 ssl 設定檔，以更新用戶端授權設定至儲存在 $newclientconfig 中的新值。</span><span class="sxs-lookup"><span data-stu-id="429f3-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="429f3-111">參數</span><span class="sxs-lookup"><span data-stu-id="429f3-111">PARAMETERS</span></span>

### <span data-ttu-id="429f3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="429f3-112">-ApplicationGateway</span></span>
<span data-ttu-id="429f3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="429f3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="429f3-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="429f3-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="429f3-115">用戶端驗證設定設定</span><span class="sxs-lookup"><span data-stu-id="429f3-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-116">-DefaultProfile</span></span>
<span data-ttu-id="429f3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="429f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="429f3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="429f3-118">-Name</span></span>
<span data-ttu-id="429f3-119">SSL 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="429f3-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="429f3-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="429f3-120">-SslPolicy</span></span>
<span data-ttu-id="429f3-121">SSL 原則</span><span class="sxs-lookup"><span data-stu-id="429f3-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f3-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="429f3-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="429f3-123">受信任的用戶端 CA 憑證鏈</span><span class="sxs-lookup"><span data-stu-id="429f3-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429f3-124">CommonParameters</span></span>
<span data-ttu-id="429f3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="429f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429f3-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="429f3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429f3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="429f3-127">INPUTS</span></span>

### <span data-ttu-id="429f3-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="429f3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="429f3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="429f3-129">OUTPUTS</span></span>

### <span data-ttu-id="429f3-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="429f3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="429f3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="429f3-131">NOTES</span></span>

## <span data-ttu-id="429f3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="429f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="429f3-133">附加 AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="429f3-134">新-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="429f3-135">AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="429f3-136">移除-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="429f3-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)