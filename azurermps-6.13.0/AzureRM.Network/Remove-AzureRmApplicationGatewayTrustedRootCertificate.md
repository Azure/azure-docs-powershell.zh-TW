---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448326"
---
# <span data-ttu-id="84fc7-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="84fc7-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="84fc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="84fc7-103">從應用程式閘道移除受信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="84fc7-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84fc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="84fc7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84fc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="84fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="84fc7-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet 會從現有的應用程式閘道中移除受信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="84fc7-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="84fc7-107">示例</span><span class="sxs-lookup"><span data-stu-id="84fc7-107">EXAMPLES</span></span>

### <span data-ttu-id="84fc7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84fc7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="84fc7-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="84fc7-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="84fc7-110">第二個命令會從儲存在 $gw 的應用程式閘道中，移除名為 myRootCA 的根信任證書。</span><span class="sxs-lookup"><span data-stu-id="84fc7-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="84fc7-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="84fc7-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="84fc7-112">參數</span><span class="sxs-lookup"><span data-stu-id="84fc7-112">PARAMETERS</span></span>

### <span data-ttu-id="84fc7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84fc7-113">-ApplicationGateway</span></span>
<span data-ttu-id="84fc7-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84fc7-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84fc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fc7-115">-DefaultProfile</span></span>
<span data-ttu-id="84fc7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84fc7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84fc7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="84fc7-117">-Name</span></span>
<span data-ttu-id="84fc7-118">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="84fc7-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="84fc7-119">-Confirm</span></span>
<span data-ttu-id="84fc7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84fc7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84fc7-121">-WhatIf</span></span>
<span data-ttu-id="84fc7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84fc7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84fc7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84fc7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fc7-124">CommonParameters</span></span>
<span data-ttu-id="84fc7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84fc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fc7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84fc7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fc7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="84fc7-127">INPUTS</span></span>

### <span data-ttu-id="84fc7-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84fc7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84fc7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="84fc7-129">OUTPUTS</span></span>

### <span data-ttu-id="84fc7-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84fc7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84fc7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="84fc7-131">NOTES</span></span>

## <span data-ttu-id="84fc7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="84fc7-132">RELATED LINKS</span></span>
