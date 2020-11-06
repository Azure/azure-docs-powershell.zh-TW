---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 81928913565c6e95f3768ccd5c05e8baa2c14b74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457259"
---
# <span data-ttu-id="32105-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="32105-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="32105-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32105-102">SYNOPSIS</span></span>
<span data-ttu-id="32105-103">從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="32105-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32105-104">句法</span><span class="sxs-lookup"><span data-stu-id="32105-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32105-105">說明</span><span class="sxs-lookup"><span data-stu-id="32105-105">DESCRIPTION</span></span>
<span data-ttu-id="32105-106">Remove-AzureRmApplicationGatewaySslPolicy Cmdlet 會從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="32105-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="32105-107">示例</span><span class="sxs-lookup"><span data-stu-id="32105-107">EXAMPLES</span></span>

### <span data-ttu-id="32105-108">範例1：從應用程式閘道移除 SSL 原則</span><span class="sxs-lookup"><span data-stu-id="32105-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="32105-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道中移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="32105-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="32105-110">參數</span><span class="sxs-lookup"><span data-stu-id="32105-110">PARAMETERS</span></span>

### <span data-ttu-id="32105-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32105-111">-ApplicationGateway</span></span>
<span data-ttu-id="32105-112">指定此 Cmdlet 移除 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="32105-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="32105-113">-Force</span><span class="sxs-lookup"><span data-stu-id="32105-113">-Force</span></span>
<span data-ttu-id="32105-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="32105-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32105-115">-確認</span><span class="sxs-lookup"><span data-stu-id="32105-115">-Confirm</span></span>
<span data-ttu-id="32105-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32105-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32105-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32105-117">-WhatIf</span></span>
<span data-ttu-id="32105-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32105-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32105-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32105-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32105-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32105-120">-DefaultProfile</span></span>
<span data-ttu-id="32105-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32105-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32105-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32105-122">CommonParameters</span></span>
<span data-ttu-id="32105-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32105-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32105-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32105-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32105-125">輸入</span><span class="sxs-lookup"><span data-stu-id="32105-125">INPUTS</span></span>

### <span data-ttu-id="32105-126">System.object</span><span class="sxs-lookup"><span data-stu-id="32105-126">System.String</span></span>

## <span data-ttu-id="32105-127">輸出</span><span class="sxs-lookup"><span data-stu-id="32105-127">OUTPUTS</span></span>

### <span data-ttu-id="32105-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32105-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="32105-129">筆記</span><span class="sxs-lookup"><span data-stu-id="32105-129">NOTES</span></span>
<span data-ttu-id="32105-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="32105-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="32105-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="32105-131">RELATED LINKS</span></span>

[<span data-ttu-id="32105-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="32105-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="32105-133">新-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="32105-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="32105-134">AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="32105-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

