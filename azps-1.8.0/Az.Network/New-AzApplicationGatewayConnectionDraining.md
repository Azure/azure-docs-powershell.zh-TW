---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621873"
---
# <span data-ttu-id="388f3-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="388f3-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="388f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="388f3-102">SYNOPSIS</span></span>
<span data-ttu-id="388f3-103">針對後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="388f3-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="388f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="388f3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="388f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="388f3-105">DESCRIPTION</span></span>
<span data-ttu-id="388f3-106">**新的-AzApplicationGatewayConnectionDraining** Cmdlet 會為後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="388f3-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="388f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="388f3-107">EXAMPLES</span></span>

### <span data-ttu-id="388f3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="388f3-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="388f3-109">此命令會建立新的連接排出設定，並將 [Enabled] 設定為 True 並將 DrainTimeoutInSec 設定為42秒，並將其儲存在 $connectionDraining 中。</span><span class="sxs-lookup"><span data-stu-id="388f3-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="388f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="388f3-110">PARAMETERS</span></span>

### <span data-ttu-id="388f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388f3-111">-DefaultProfile</span></span>
<span data-ttu-id="388f3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="388f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="388f3-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="388f3-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="388f3-114">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="388f3-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="388f3-115">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="388f3-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="388f3-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="388f3-116">-Enabled</span></span>
<span data-ttu-id="388f3-117">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="388f3-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388f3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388f3-118">CommonParameters</span></span>
<span data-ttu-id="388f3-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="388f3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388f3-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="388f3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388f3-121">輸入</span><span class="sxs-lookup"><span data-stu-id="388f3-121">INPUTS</span></span>

### <span data-ttu-id="388f3-122">所有</span><span class="sxs-lookup"><span data-stu-id="388f3-122">None</span></span>

## <span data-ttu-id="388f3-123">輸出</span><span class="sxs-lookup"><span data-stu-id="388f3-123">OUTPUTS</span></span>

### <span data-ttu-id="388f3-124">PSApplicationGatewayConnectionDraining 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="388f3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="388f3-125">筆記</span><span class="sxs-lookup"><span data-stu-id="388f3-125">NOTES</span></span>

## <span data-ttu-id="388f3-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="388f3-126">RELATED LINKS</span></span>

[<span data-ttu-id="388f3-127">AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="388f3-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="388f3-128">移除-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="388f3-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="388f3-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="388f3-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

