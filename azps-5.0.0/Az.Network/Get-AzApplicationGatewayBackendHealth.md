---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139805"
---
# <span data-ttu-id="b01f4-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="b01f4-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="b01f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b01f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b01f4-103">取得應用程式閘道後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="b01f4-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="b01f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b01f4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b01f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b01f4-105">DESCRIPTION</span></span>
<span data-ttu-id="b01f4-106">Get-AzApplicationGatewayBackendHealth Cmdlet 會取得應用程式閘道後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="b01f4-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="b01f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="b01f4-107">EXAMPLES</span></span>

### <span data-ttu-id="b01f4-108">範例1：在沒有展開資源的情況下，取得後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="b01f4-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="b01f4-109">這個命令會取得屬於名為 ResourceGroup01 之資源群組的應用程式閘道的後端健康情況，並將它儲存在 $BackendHealth 變數中。</span><span class="sxs-lookup"><span data-stu-id="b01f4-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="b01f4-110">範例2：取得已展開資源的後端健康情況。</span><span class="sxs-lookup"><span data-stu-id="b01f4-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="b01f4-111">這個命令會使用 ApplicationGateway01 名為 ResourceGroup01 的資源群組，並將其儲存在 $BackendHealth 變數中的) 應用程式閘道的展開的資源，來取得後端健康狀態 (。</span><span class="sxs-lookup"><span data-stu-id="b01f4-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="b01f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="b01f4-112">PARAMETERS</span></span>

### <span data-ttu-id="b01f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b01f4-113">-AsJob</span></span>
<span data-ttu-id="b01f4-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b01f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b01f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01f4-115">-DefaultProfile</span></span>
<span data-ttu-id="b01f4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b01f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01f4-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b01f4-117">-ExpandResource</span></span>
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

### <span data-ttu-id="b01f4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b01f4-118">-Name</span></span>
<span data-ttu-id="b01f4-119">指定此 Cmdlet 所取得之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="b01f4-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b01f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="b01f4-121">指定包含應用程式閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b01f4-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="b01f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01f4-122">CommonParameters</span></span>
<span data-ttu-id="b01f4-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b01f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01f4-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b01f4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01f4-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b01f4-125">INPUTS</span></span>

### <span data-ttu-id="b01f4-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b01f4-126">System.String</span></span>

## <span data-ttu-id="b01f4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b01f4-127">OUTPUTS</span></span>

### <span data-ttu-id="b01f4-128">PSApplicationGatewayBackendHealth 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b01f4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="b01f4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b01f4-129">NOTES</span></span>
<span data-ttu-id="b01f4-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="b01f4-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b01f4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b01f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="b01f4-132">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01f4-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

