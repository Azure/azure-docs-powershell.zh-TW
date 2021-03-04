---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: b5910352c8abcfb880a1007a3f2246ff7c12d9f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915358"
---
# <span data-ttu-id="74e60-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="74e60-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="74e60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74e60-102">SYNOPSIS</span></span>
<span data-ttu-id="74e60-103">獲得應用程式閘道後端健康狀態。</span><span class="sxs-lookup"><span data-stu-id="74e60-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="74e60-104">語法</span><span class="sxs-lookup"><span data-stu-id="74e60-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74e60-105">描述</span><span class="sxs-lookup"><span data-stu-id="74e60-105">DESCRIPTION</span></span>
<span data-ttu-id="74e60-106">Cmdlet Get-AzApplicationGatewayBackendHealth應用程式閘道後端健康狀態。</span><span class="sxs-lookup"><span data-stu-id="74e60-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="74e60-107">例子</span><span class="sxs-lookup"><span data-stu-id="74e60-107">EXAMPLES</span></span>

### <span data-ttu-id="74e60-108">範例 1：在沒有展開資源的情況下，獲得後端健康狀態。</span><span class="sxs-lookup"><span data-stu-id="74e60-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="74e60-109">此命令會獲得名為 ApplicationGateway01 之應用程式閘道的後端健康狀態，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $BackendHealth 變數中。</span><span class="sxs-lookup"><span data-stu-id="74e60-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="74e60-110">範例 2：使用展開的資源獲得後端健康狀態。</span><span class="sxs-lookup"><span data-stu-id="74e60-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="74e60-111">此命令會使用名為 ApplicationGateway01 的應用程式閘道的展開資源 () ，獲得後端健康狀態資料，該應用程式閘道屬於名為 ResourceGroup01 的資源群組，並儲存在 $BackendHealth 變數中。</span><span class="sxs-lookup"><span data-stu-id="74e60-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="74e60-112">參數</span><span class="sxs-lookup"><span data-stu-id="74e60-112">PARAMETERS</span></span>

### <span data-ttu-id="74e60-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74e60-113">-AsJob</span></span>
<span data-ttu-id="74e60-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74e60-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74e60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e60-115">-DefaultProfile</span></span>
<span data-ttu-id="74e60-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74e60-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74e60-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="74e60-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e60-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="74e60-118">-Name</span></span>
<span data-ttu-id="74e60-119">指定此 Cmdlet 所獲得之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="74e60-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e60-120">-ResourceGroupName</span></span>
<span data-ttu-id="74e60-121">指定包含應用程式閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="74e60-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e60-122">CommonParameters</span></span>
<span data-ttu-id="74e60-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74e60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e60-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74e60-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e60-125">輸入</span><span class="sxs-lookup"><span data-stu-id="74e60-125">INPUTS</span></span>

### <span data-ttu-id="74e60-126">System.String</span><span class="sxs-lookup"><span data-stu-id="74e60-126">System.String</span></span>

## <span data-ttu-id="74e60-127">輸出</span><span class="sxs-lookup"><span data-stu-id="74e60-127">OUTPUTS</span></span>

### <span data-ttu-id="74e60-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="74e60-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="74e60-129">筆記</span><span class="sxs-lookup"><span data-stu-id="74e60-129">NOTES</span></span>
<span data-ttu-id="74e60-130">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="74e60-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74e60-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="74e60-131">RELATED LINKS</span></span>

[<span data-ttu-id="74e60-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74e60-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

