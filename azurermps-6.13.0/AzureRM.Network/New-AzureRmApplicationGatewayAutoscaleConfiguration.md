---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453671"
---
# <span data-ttu-id="5c775-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c775-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5c775-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c775-102">SYNOPSIS</span></span>
<span data-ttu-id="5c775-103">建立應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="5c775-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c775-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c775-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c775-105">說明</span><span class="sxs-lookup"><span data-stu-id="5c775-105">DESCRIPTION</span></span>
<span data-ttu-id="5c775-106">**新的-AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet 會針對 Azure 應用程式閘道建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="5c775-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="5c775-107">示例</span><span class="sxs-lookup"><span data-stu-id="5c775-107">EXAMPLES</span></span>

### <span data-ttu-id="5c775-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5c775-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="5c775-109">第一個命令會建立含最小容量3的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="5c775-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="5c775-110">第二個命令會建立具有自動縮放設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5c775-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="5c775-111">參數</span><span class="sxs-lookup"><span data-stu-id="5c775-111">PARAMETERS</span></span>

### <span data-ttu-id="5c775-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c775-112">-DefaultProfile</span></span>
<span data-ttu-id="5c775-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c775-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c775-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="5c775-114">-MinCapacity</span></span>
<span data-ttu-id="5c775-115">應用程式閘道總可使用的最小容量單位（並收取費用）。</span><span class="sxs-lookup"><span data-stu-id="5c775-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="5c775-116">-確認</span><span class="sxs-lookup"><span data-stu-id="5c775-116">-Confirm</span></span>
<span data-ttu-id="5c775-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c775-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c775-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c775-118">-WhatIf</span></span>
<span data-ttu-id="5c775-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c775-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c775-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c775-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c775-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c775-121">CommonParameters</span></span>
<span data-ttu-id="5c775-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c775-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c775-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c775-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c775-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5c775-124">INPUTS</span></span>

### <span data-ttu-id="5c775-125">所有</span><span class="sxs-lookup"><span data-stu-id="5c775-125">None</span></span>

## <span data-ttu-id="5c775-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5c775-126">OUTPUTS</span></span>

### <span data-ttu-id="5c775-127">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5c775-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5c775-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5c775-128">NOTES</span></span>

## <span data-ttu-id="5c775-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c775-129">RELATED LINKS</span></span>
